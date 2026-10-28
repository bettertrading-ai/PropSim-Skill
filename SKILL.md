---
name: propsim
description: Simulates prop firm accounts from a daily trade series and the firm rules in this repository's `data/` files. Use when asked which risk/RR passes an evaluation cheapest, which funded setup has the best EV or clears payout rules easiest, or how to rank/allocate across several accounts.
---

# PropSim v3.1 — Answer Questions Within the User's Framework

> **Disclaimer:** Simulation output is an estimate, not financial advice; prop firm rules change, always use the current firm rules data.

PropSim simulates prop firm evaluation and funded accounts. The only input the user brings is a daily trade series from their own backtest process. Firm rules and fees come only from the JSON files in this repository's `data/` folder, never from memory, old reports or marketing prices. PropSim does not run backtests.

## Where the rules come from

- `data/index.json` lists the firms. Top-level keys: `dataset`, `snapshot_date`, `firm_count`, `totals`, `firms`, `notes`. Each `firms[]` entry has `slug`, `name`, `file`, `file_bytes`, `plans`, `rules`, `sources`, `unknown_rules`, `unknown_share`, `rules_by_value_state`, `latest_checked_at`, `last_checked`.
- `data/<slug>.json` is one file per firm; take `<slug>` from `firms[].slug` in `data/index.json`. Paths are relative to the repository root.
- A firm file has the top-level keys `firm`, `slug`, `snapshot_date`, `latest_checked_at`, `counts`, `free_tier_map`, `plans`, `rules`, `sources`. `plans[]` holds the plan-level fields, `rules[]` holds the rule records, and the top-level `sources[]` is a source register.
- Read `data/index.json` first, then only the JSON file(s) for the firm(s) you are simulating. Never read the whole `data/` folder (the full set is about 43 MB; one firm file can be several MB, so read the file with a JSON parser, not as text).

## Data fields

Rule record fields: `record_id`, `plan_id`, `product`, `account_size`, `dll_option`, `eval_drawdown`, `funded_drawdown`, `stage`, `metric`, `value`, `value_type`, `value_state`, `unit`, `operator`, `rule_event`, `version`, `cohort`, `availability`, `applicability`, `notes`, `original_value` (with `original_unit`, `original_value_type`, `original_value_present`), `canonical_plan_ids`, `sources`, `source_urls`, `source_locator`, `source_as_of`, `checked_at`, `source_missing`, `checked_at_missing`.

Each item of a rule's `sources[]` has `source_id`, `url` and `checked_at`.

Plan-level fields: `plan_id`, `product`, `account_size`, `dll_option`, `eval_drawdown`, `funded_drawdown`, `availability`, `cohort`, `version`, `plan_notes`.

`value` is stored as in the snapshot; a structured value is a JSON-encoded string. `stage` can hold several values joined by `;`. A `value` may be a string even for a quantity that is normally a number, for example a tiered profit split given as text with a `notes` field explaining the tiers. Do not parse such a string as a number: report the string and its `notes` as given.

The metric `max_loss_limit` in a firm's `free_tier_map` is the MLL amount in USD (the unit is given in the `unit` field). The `profit_split` entry is the trader's split.

The meaning of `product`, `account_size`, `dll_option`, `eval_drawdown`, `funded_drawdown`, `stage`, `value_type`, `unit`, `operator`, `rule_event`, `version`, `cohort`, `availability`, `applicability`, `original_value*`, `canonical_plan_ids`, `source_locator`, `source_as_of`, `source_missing` and `checked_at_missing` is not documented in the data. Report these fields as given and do not interpret them. If a simulation needs one of them to choose between plans, cohorts or versions and the data does not say which applies, ask the user which plan / version to use, and state the choice in the report.

Payout, fee, activation and reset rules are told apart by the value of `metric`; metric names differ per firm (see §3.2).

`value_state` is one of: VERIFIED, VERIFIED_PUBLIC_CARD, DERIVED, PUBLIC_ADVERTISEMENT, AMBIGUOUS, CONFLICT, UNKNOWN, NONE, NOT_APPLICABLE, NOT_STATED, NOT_PUBLISHED, NOT_PUBLICLY_VERIFIED, NO_FIXED_LIMIT, EXPLICIT_UNLIMITED, UNVERIFIED, USER_ACCOUNT_UNKNOWN, DOCUMENT_NOT_RETRIEVED. How each is handled is in §1.2.

---

## 0. Purpose

PropSim's job is to **answer the questions in the user's framework**, not to simulate every rule for its own sake.

- **Stage 1 Eval**: which ATR multiple × RR × per-trade risk **passes the evaluation for the least money**?
- **Stage 2 Funded**: (A) which RR has the **best EV**? (B) which RR **most easily clears the firm's payout rules**? When the account is eligible for payout, should it **withdraw now or keep building buffer**?

Principle: an approximate probability is enough to decide. The process has three layers:

1. **Quick method (§3, §4) = first-round screening.** Every grid cell must be run.
2. **Rolling pipeline (§5) = validate the shortlist**: connect eval and funded into one continuous pipeline, started on every day of the real daily series in turn, to answer "how much is actually received per month, and how bad can it get".
3. **Full event-driven simulation (§7)**: use it only for path events the pipeline cannot handle either.

Your backtest process produces the trade series; the firm rules come from the `data/` files; PropSim chooses the risk and the allocation.

---

## 1. Hard Rules (every report must follow them)

1. **Firm rules and fees come only from the JSON files in this repository's `data/` folder** (see "Where the rules come from"); each firm file is the current version. Never hard-code, never guess, never use chat memory, old reports or marketing prices from outside the data files. Log each field's origin and state with `record_id` and `value_state`, and report `value_state` exactly as it is; never interpret it. Where a rule has sources, record the `url` and `checked_at` of the source with the most recent `checked_at` (and say that this is the rule used). A value with no source URL and checked date (`source_missing` or `checked_at_missing` set, or no `sources[]` entry) must be labelled "source missing" in the report and must never be treated as VERIFIED, whatever its `value_state` says.
2. **A missing value is BLOCKED, and the report must name the field.** The cost of a BLOCKED fee is always expressed as a break-even sensitivity (§5.5); a value is never assumed. Example: `BLOCKED: FirmX record_id xxx, metric = <metric value>, value_state = UNKNOWN`. UNKNOWN must never become 0, infinity, or "typical practice". UNKNOWN is common in the current data, so BLOCKED reports are expected. If only one question is affected, only that question is BLOCKED and the others are answered as usual. How each `value_state` is handled:
   - VERIFIED and VERIFIED_PUBLIC_CARD count as verified. Nothing else does.
   - DERIVED is labelled "derived", not verified.
   - PUBLIC_ADVERTISEMENT is an advertised price: use it only for the fee it describes, and label it "advertised".
   - NONE, NOT_APPLICABLE, NO_FIXED_LIMIT and EXPLICIT_UNLIMITED are reported as they are, with the note "meaning not confirmed". They are not BLOCKED automatically and are never turned into 0 or infinity.
   - UNKNOWN, AMBIGUOUS, CONFLICT, and every other state (NOT_STATED, NOT_PUBLISHED, NOT_PUBLICLY_VERIFIED, UNVERIFIED, USER_ACCOUNT_UNKNOWN, DOCUMENT_NOT_RETRIEVED, or a state not listed) are unconfirmed: not verified, never filled with a number or an estimate. They go into the BLOCKED / needs-confirmation list.
   - Near the top of the report, state each simulated firm's share of UNKNOWN rules: count of `rules[]` with `value_state` UNKNOWN ÷ count of all `rules[]` of that firm. Compute it from the firm file when cheap, and use `unknown_share` in `data/index.json` only as a cross-check.
3. **Costs**: deduct commission + slippage on every trade (round turn × qty). Breach checks must include the costs too. If the fill price already includes slippage, do not deduct it again.
4. **No look-ahead**: the signal uses only closed bars and enters at the open of the next bar. If the stop and the target are both hit in the same bar, treat it as a stop-loss. On an opening gap, exit at the opening price. The stop-loss logic must be the same as in the live execution system.
5. **The grid is locked in advance**: before the run, write down all cells and record **N = total number of cells** (including risk variants). No adding cells after seeing results. Every cell tried must be reported, not only the winning ones.
6. **Report IS / OOS separately**: choose using IS only, look at OOS once; FULL is descriptive only. Parameters chosen after looking at the whole period must not be presented as OOS results.
7. **Optional audit format — first line of the report (recommended when results will be reviewed by someone else; you may drop it).** Write the result on the first line: if nothing is violated, write only `FOLLOWED` (no need to expand); if anything is violated, list the VIOLATED items. Items to check: rule source, costs, no look-ahead (closed bar), locked grid N, baseline reproduction, pipeline validation (§5.6), and for every code file used its file name + the first 8 characters of its SHA-256.
8. **Optional audit format — SHA-256 list (recommended when results will be reviewed by someone else; you may drop it).** List the hashes of: the code, the firm JSON file(s) used, the data file, the user's trade file, and the final report (output charts and CSVs need not be listed).

---

## 2. Input: Daily Trade Series

Produced by your backtest process (one per grid cell), one row per day:

`date, qty, gross, net, worst_open_loss_usd, mfe_usd, exit_type(TP/SL/EOD/none), planned_risk_usd, skipped_reason`

`worst_open_loss_usd` is rebuilt from 1m bars and is used to judge intraday breaches. Days without a trade must be kept and marked `none`; they must not be deleted.
For trades held overnight, mark exit_type as overnight, and worst_open_loss must be computed across days.

---

## 3. Stage 1 Eval — Quick Method (default)

### 3.1 Strategy statistics per cell (no firm rules involved)

- Daily win rate (trading days with net > 0 ÷ days with a trade), average win / average loss
- Daily PnL distribution: **P5 / P25 / median / P75 / P95**
- Win-streak / loss-streak distribution: longest, average, P(streak ≥ 1…5)
- Exit type %: **TP / SL / EOD**, plus the number of skipped days

### 3.2 Exam fields to read from the firm rules (`data/` files)

The simulation needs these quantities: profit target, MLL, trail reference (EOD / intraday), lock basis, breach basis and comparator (< or ≤), consistency value and formula, min days, contract limit (mini/micro ratio), DLL (whether present, soft or hard, amount), purchase price, monthly fee or one-off, reset price, activation fee. Account size is `account_size`; the stage a rule applies to is `stage`; the value is `value` with its `unit`.

**Finding the metric names.** Metric names differ per firm; do not assume one name works for all firms. For each simulated firm:

1. Read the firm file's `free_tier_map`. It gives the firm's own (stage, metric) pairs for `profit_target`, `max_loss_limit` and `profit_split`, and, where present, for `price_metrics` (`reference`, `coupon`, `reset`).
2. For the other quantities, list the distinct (`stage`, `metric`) pairs in the firm's `rules[]`, pick the metric whose name matches the quantity (use the examples below as search hints), and check its `unit` and `value_state`.
3. If no metric clearly matches, or several firms' or plans' metrics could match, the quantity is not found: BLOCKED (name the quantity), or ask the user. Never pick a metric by guess.

Examples, check the firm file (metric names seen in the data; a name existing for one firm does not mean it exists for another):

| Quantity | Example metric names |
| :---- | :---- |
| profit target | `profit_target`, `profit_target_usd` |
| MLL amount | `max_drawdown_amount`, `mll_amount`, `max_loss_amount`, `max_drawdown`, `trailing_drawdown_amount` |
| trail reference | `trail_reference`, `drawdown_type`, `drawdown_basis`, `intraday_trail_basis`, `eod_trail_basis` |
| lock basis | `mll_lock_floor`, `mll_lock_trigger`, `locked_mll_balance`, `mll_lock_trigger_eod_balance` |
| breach basis / comparator | `breach_observation_basis`, `touch_is_breach`, `mll_breach_balance_comparison`, `breach_balance_boundary` |
| consistency | `consistency_max_best_day_ratio`, `consistency`, `consistency_formula`, `consistency_denominator`, `payout_consistency` |
| min days | `minimum_trading_days`, `min_trading_days`, `min_trading_days_eval` |
| contract limit | `max_mini_contracts`, `max_micro_contracts`, `max_contracts`, `max_contracts_mini`, `mixed_contract_conversion` |
| DLL amount / present / type | `dll_amount`, `daily_loss_limit_amount`, `daily_loss_limit_usd`; `dll_enabled`, `daily_loss_limit_exists`; `dll_type`, `dll_breach_effect` |
| purchase price | `purchase_price`, `eval_list_price_single`, `evaluation_fee_one_time_usd`, `entry_fee_usd`, `advertised_reference_price` (advertised) |
| monthly vs one-off / funded platform fee | `billing_model`, `billing_cycle`, `subscription_fee_monthly`, `platform_fee` |
| reset price | `reset_price`, `reset_fee`, `reset_fee_usd`, `eval_reset_fee`, `reset_price_current` |
| activation fee | `activation_fee`, `activation_fee_usd`, `pa_activation_fee_amount` |
| payout eligibility days | `minimum_qualifying_profit_days`, `qualifying_days`, `qualifying_winning_days` |
| payout daily profit threshold | `minimum_profit_per_winning_day`, `minimum_day_profit` |
| cycle profit | `cycle_profit_required`, `cycle_profit_test`, `payout_net_profit_since_previous` |
| buffer | `payout_buffer_balance`, `payout_buffer_profit`, `payout_buffer_required`, `buffer_balance` |
| split | `trader_split`, `payout_split`, `trader_profit_split`, `profit_split`, `trader_profit_split_pct` |
| cap | `payout_cap`, `payout_cap_per_request`, `per_request_cap`, `payout_maximum`, `lifetime_cap`, `max_withdrawal_usd` |
| payout fee | `payout_processor_fee`, `payout_processing_fee`, `payout_fee` |

A split value may be a tiered string (see "Data fields"): if the simulation needs a number and the value is a tiered string, ask the user or mark it BLOCKED. In the table above, `max_loss_limit` in `free_tier_map` is the MLL amount in USD (see `unit`). There is no clear example metric for the payout waiting period. Every quantity must record its `record_id` and `value_state` (and its source `url` and `checked_at`, §1.1). **If any one is missing, or its `value_state` is unconfirmed (§1.2) → BLOCKED (name the field).**

### 3.3 Walk the history day by day (rolling attempts)

An attempt starts on the first day of the segment:

  Each day: if there is a trade → if balance − worst_open_loss − cost ≤ MLL line (or use < as the firm rules say) → blowup

        EOD: balance += net; update the MLL line (trail / lock) as the firm rules say

        if balance ≥ max(target, best_day/consistency) and days ≥ min_days → pass

  After a pass or a blowup, a new attempt starts on the next trading day; the last unfinished attempt is dropped.

RR and per-trade risk stay fixed throughout (no "shrink the target to just enough", and no reducing size near the MLL), unless the grid explicitly treats it as a variant.

**Report separately for each cell, each firm, and IS/OOS/FULL:**

- **pass rate per attempt** = passes ÷ (passes + blowups)
- **blowups per pass**
- **days per pass** (trading days used by the successful attempt)
- **fee cost per pass**: purchase / monthly fee (rebilled by calendar day) + reset for each blowup + activation, averaged over each pass chain
- Robustness check: open an independent attempt on every day and compute P(pass). This number must not be treated as an independent sample for computing a CI.

### 3.4 Grid and cell selection

- Grid: **ATR multiple × RR × per-trade risk** (coarse grid, free parameters ≤ 3 — default, adjust to your data), locked, record N.
- Choose the cell with the **lowest cost per pass** using **IS** only; OOS is used only to validate the chosen cell and takes no part in the choice. Each cell has only 10–40 passes; treat differences smaller than about ±$40 per pass or ±5 percentage points as noise (both thresholds are defaults, adjust to your data).
- Also list the trade-off between the user's preferences (for example most exits should be TP/SL, not too many EOD) and cost; the user makes the final decision.

---

## 4. Stage 2 Funded — Two Goals

Firms differ a lot (how payout is calculated, buffer, eligible days, consistency, split, cap, how the MLL changes after payout). **The agent must use that firm's rules from its `data/` file and work out for itself how that firm achieves A and B.** Before the run, write 3–5 lines of "this firm's plan": which fields decide payout eligibility, how a payout will affect balance / floor, and which fields are missing. A mechanism not supported by the firm rules must never be invented. Find the payout quantities (eligibility days and threshold, cycle profit, buffer, waiting period, split, cap, payout fee) the same way as in §3.2. A split given as a tiered string must not be parsed as a number (ask the user or BLOCKED).

### Goal A — choose the RR with the best EV

- Using the same daily series, walk day by day from the funded starting state (initialise balance / floor from the firm rules; the exam numbers must not be copied over) until blowup or horizon H.
- **EV per funded account** = E[payout actually received × split − payout fee] − funded fees (activation, monthly fee, etc.). Also report P(blowup) and P(≥1 payout received).
- Compare RR by RR (and risk); report IS/OOS at the same time.

### Goal B — choose the RR that most easily clears the payout rules

- Read the payout eligibility conditions from the firm rules (for example eligible profit days and threshold, cycle profit, consistency, minimum buffer, waiting period).
- For each RR report: **P(reaching first payout eligibility before blowup)**, how many trading days it takes to become eligible (median / P75), and which condition usually blocks it.
- The best RR for A and B can differ. Report both, and state clearly how the trade-off is made.

### When eligible: withdraw vs keep building buffer

At every first-eligible time point (take all eligible points that occurred in history), compare two paths using the same horizon:

- **P (withdraw now)**: compute how much can be withdrawn as the firm rules say, how balance / floor / cycle change after withdrawal, then keep walking.
- **K (keep building)**: keep trading and withdraw only once the buffer reaches the level defined by the firm rules or specified by the user (K can have 2–3 buffer levels as variants).
- For each path report: E[cash received], P(blowup), P(receiving money ≥1 time), days to the first payout.
- Write the conclusion as one sentence: "This firm, this RR: withdraw now / build to $X first, because …".

---

## 5. Rolling Pipeline — Validate the Shortlist

**Not used for screening.** After the quick method picks a shortlist for each firm × segment (usually 3–6 cells, together with the baseline specified by the user), validate it with this method. The shortlist and the pipeline parameters must be locked before the run and counted in N.

### 5.1 Definitions

- **Cycle**: starting from the start day, run eval attempts (reset on blowup, charge fees as the firm rules say) until pass → open one funded account and run it under the specified payout policy (baseline: withdraw the maximum as soon as eligible; the K levels of "withdraw vs build" are variants) until blowup / stall / end of data. **The next cycle starts on the first trading day after the funded account ends.**
- **Same parameter set** (ATR × RR × risk) is used for eval and funded throughout; it must not be one set for eval and another for funded, unless the grid explicitly treats it as a variant.
- **Every cash flow must be dated**: exam purchase / monthly fee (rebilled by calendar day), reset, activation, payout × split, payout fee. All numbers come from the firm's `data/` file.
- **Path**: from start day s, cycles follow one another until the end of the segment.
- **Rolling starts**: open one path on **every trading day** in the segment, as long as at least 63 trading days remain (`MIN_REMAIN = 63`, a locked parameter; default, adjust to your data).
- **Real daily series only**: never assume days are independent, never stitch an eval × funded expectation together with formulas.
- A cycle not finished at the end of the data is marked censored: its cash flows are still counted in the path, but it is not counted in the cycle statistics.

### 5.2 Metrics to report per cell (each firm × IS/OOS/FULL)

| Metric | Definition |
| :---- | :---- |
| **mean / median $/month** | For each path: net ÷ number of trading days × 21; take the mean and median over all rolling starts |
| **P(month ≤ 0)** | Among the complete calendar months of all paths (pooled), the share with monthly income ≤ 0 |
| **worst month / 5th-pct month** | The lowest value / 5th percentile of the pooled calendar months |
| **pipeline max drawdown** | Peak-to-trough of the cumulative pipeline cash on each path; report the median and the max |
| **mean / median net per cycle** | Net of the completed (non-censored) cycles over all rolling starts |
| **n independent cycles** | Number of completed, non-overlapping cycles on the day-0 path (the first start day) |

Optional: p10 $/month, P(path ≤ 0), P(cycle ≤ 0), p95 month, P(merge day-0).

### 5.3 Number of independent cycles (report column)

- Every result table **must have an `n independent cycles` column**.
- **Cells with < 10 must be marked ⚠** (for example `4 ⚠`) (the threshold of 10 is a default, adjust to your data).
- Reason: with one signal per day, paths from different start days merge as soon as they hit the same breach / pass, so the number of rolling starts (for example 650; example only, adjust to your data) is not the number of independent samples; the number of independent samples is n independent cycles.

### 5.4 Ranking

- **Primary ranking: median $/month**; **secondary ranking: 5th-pct month** (used when there is a tie or the gap is smaller than noise).
- Also list the **mean $/month ranking** (and the older quick-method EV formula ranking, if there is one), **state explicitly which cells rank differently by mean and by median**, and by how much.
- If the 5th-pct criterion picks a different risk level (for example all pick $1k), also report the 5th-pct first place within the same risk level, and hand the trade-off to the user.

### 5.5 BLOCKED fees → break-even sensitivity

- Never assume a value. For every BLOCKED fee, name the field (example: `BLOCKED: FirmX funded platform fee X/month (record_id xxx)`), then report:
  - exposure: funded account-months per month (monthly-fee type) or payouts per month (per-payout-fee type)
  - adjusted mean = mean − fee × exposure
  - **break-even fee** = mean ÷ exposure
  - ranking flip point: first place vs second place; if exposure₁ > exposure₂, flip fee = (mean₁ − mean₂) ÷ (exposure₁ − exposure₂); otherwise write "no fee ≥ 0 will flip it".

### 5.6 Validation

- The day-0 path must reproduce the earlier pipeline result for the same parameters (example: a reference run, median |diff| $X, max |diff| $Y); differences must be explained (for example an older version left out fees at the end of the data).
- The report must state which quick-method conclusions the pipeline confirmed and which rankings it changed.

---

## 6. Multi-account Ranking / Rotation

The question answered: with N accounts in hand (can span firms, eval and funded mixed), and one strategy signal, how is it allocated each day? This includes which account takes the trade, how large, and which ATR multiple and RR to use. This section answers only the allocation question and does not change the strategy conditions; the strategy conditions come from your backtest process.
Rules:

1. The ranking key and tie-break must be locked before the run. The default ranking key is buffer (account balance minus MLL line). Other ranking keys (for example profit progress, distance to payout) may only be grid variants and are counted in N.
2. No look-ahead. Before each day's open, rank using only the account state after the previous day's close.
3. The rank-to-parameter table is part of the grid. For example, how many ATR multiples, RR and per-trade risk each of ranks 1 to 5 uses; the whole table is locked before running. Report the number of free parameters. The per-trade risk cap is set by the user.
4. A fixed-parameter baseline is required. With the same accounts and the same signal, every account uses the same parameter set with no ranking, as the comparison. If the ranking does not beat the baseline, do not adopt it.
5. Cross-account conflicts. The same signal goes in the same direction on all accounts. If an account already holds an opposite-direction position, the handling may only come from the firm rules in the `data/` files; if the firm rules do not say, it is BLOCKED and must never be invented.
6. Account state is updated daily. Each account updates its MLL line, passes, blows up, and is paid out under its own firm's rules. When an account passes or blows up, the time and cost of bringing in a new account must be dated, and the numbers come from the firm rules in the `data/` files.
7. Same as §5: use the real daily series, with a rolling start every day.
8. Contract quantity and stop-loss are decided by PropSim. Quantity is back-computed from per-trade risk, ATR and stop distance, rounded and capped; the stop distance is determined by the ATR multiple. If this stop differs from the one the trade list originally used, first ask your backtest process to rerun the trade list with the same stop before it can go into PropSim; never substitute the old stop's PnL multiplied by quantity.

Metrics that must be reported (IS / OOS / FULL, side by side with the baseline):

* Portfolio level: median $/month, 5th-pct month, P(month ≤ 0), pipeline max drawdown, n independent cycles (mark ⚠ if fewer than 10; default, adjust to your data).
* Account level: number of blowups per account, number of payouts, share of same-day blowups.
* Improvement brought by the ranking: ranked version minus baseline, stating the size of the difference compared with noise.

Validation: if the live execution system has the same ranking rules, replay the backtest trades with the live logic and reconcile trade by trade; only 0 mismatches counts as passing.

---

## 7. When to Use the Full Detailed Simulation

**Must not be used for screening.** Use it only in the following cases, to confirm 1–3 cells of the shortlist:

- The rules involve path events that neither the quick method nor the pipeline can handle: soft DLL pause, payout request / approval / receipt timing, scaling tiers, shared risk across multiple accounts;
- The gap between the top pipeline cells is smaller than noise, and the worst_open_loss approximation could change the ranking;
- Before real money is put at risk, confirm with the user.

---

## 8. Report Format (the shorter the better)

1. First line `FOLLOWED`, or the VIOLATED list (§1.7; optional audit format)
2. Near the top: each simulated firm's share of UNKNOWN rules (§1.2), and the plan / version used when the user chose one (see "Data fields")
3. One paragraph of conclusion: answer the user's question, which cell to choose, why, and how confident
4. Firm rules used (from the `data/` files): field, value, record_id, value_state, source `url` and `checked_at` (or "source missing"); BLOCKED / needs-confirmation list
5. Result tables: §3.1 statistics, §3.3 Eval metrics (IS/OOS/FULL), §4 Funded A/B/payout decision
6. Shortlist pipeline table (§5.2, including the n independent cycles column and ⚠), ranking comparison (§5.4), BLOCKED break-even table (§5.5)
7. Caveats: cost assumptions, approximations, records with an unconfirmed value_state (§1.2), and values labelled "source missing"
8. SHA-256: code, the firm JSON file(s) used, data file, trade file, final report (§1.8; optional audit format)

Only three statuses are used: **OK** (required rules present, method followed) / **CONDITIONAL** (stated assumptions apply) / **BLOCKED** (which field is missing).
