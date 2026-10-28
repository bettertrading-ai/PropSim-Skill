# PropSim-Skill rules data (bettertrading.ai) - data files

Snapshot date: **2026-10-27**. Local export, not yet published. Firms: 12. Plans: 186. Rule records: 26,505 (UNKNOWN: 9,151, 34.5%; share = UNKNOWN / all rule records). Figures are computed from the exported files (source: kv_seed.json snapshot of 2026-10-27).

## Files

| File | Content |
|---|---|
| `data/index.json` | Firm list, plan/rule/source counts, value-state counts per firm, UNKNOWN share, latest check date, file size. |
| `data/<slug>.json` | One file per firm, minified JSON, all rule records of that firm. |
| `SHA256SUMS.txt` | SHA-256 of every file in this export. |
| `DATA_DICTIONARY.md` | Fields, metrics and enumerated values observed in the data. |

## Per-firm file schema

Top level keys of `data/<slug>.json`:

- `firm` (display name), `slug`
- `snapshot_date` - date of this snapshot (2026-10-27)
- `latest_checked_at` - latest `checked_at` among the firm's rule records
- `counts` - `plans`, `rules`, `sources`, `rules_by_value_state`
- `free_tier_map` - mapping of free-tier headline fields to (stage, metric) pairs
- `plans[]` - one entry per plan configuration: `plan_id`, `product`, `account_size`, `dll_option`, `eval_drawdown`, `funded_drawdown`, `availability`, `cohort`, `version`, `model_id`, `plan_notes`, `plan_record`, `current_price_snapshot`, `price_snapshot_missing`, `superseded_snapshots`, `free_tier`
- `rules[]` - one entry per rule record (see below)
- `sources[]` - source register: `record_id`, `source_ids`, `source_urls`, `source_records[]` (`source_id`, `title`, `url`, `checked_at`, `publication_text`, `short_quote`, `notes`, `aliases`), `source_locator`, `source_as_of`, `notes`

### Rule record

`record_id`, `plan_id`, `product`, `account_size`, `dll_option`, `eval_drawdown`, `funded_drawdown`, `stage`, `metric`, **`value`**, `value_type`, **`value_state`**, `unit`, `operator`, `rule_event`, `version`, `cohort`, `availability`, `applicability`, `notes`, `original_value*`, `canonical_plan_ids`, **`sources[]`** (`source_id`, `url`, `checked_at`), **`source_urls[]`**, **`checked_at`**, `source_missing`, `checked_at_missing`, `source_locator`, `source_as_of`.

`value` is stored exactly as in the snapshot. When it is a structured value it is a JSON-encoded string. `notes`, `applicability` and `source_locator` are free text from the data maintainers. The data does not define them formally.

## Value states

Every rule record has one `value_state`. These descriptions follow the state names and the notes found in the data. The data itself carries no formal definitions.

| value_state | Meaning |
|---|---|
| `VERIFIED` | Value was read from an official source and recorded as verified. |
| `DERIVED` | Value derived from other recorded values or rules (for example a computed threshold). |
| `PUBLIC_ADVERTISEMENT` | Value comes from a public advertisement or banner (for example a promo code). It is not confirmed as a standing rule. |
| `AMBIGUOUS` | Sources can be read in more than one way; no reading was selected. |
| `CONFLICT` | Sources disagree; the disagreement was not reconciled. |
| **`UNKNOWN`** | **Not confirmed. No value was found or confirmed in a checked source. Nothing is guessed, estimated or filled in: a missing value (`null`) under UNKNOWN is not zero and not "none".** |
| `NONE` | The source states that there is no such requirement or limit (for example "no separate minimum trading-day requirement"). |

The snapshot also contains other states: `VERIFIED_PUBLIC_CARD`, `NOT_APPLICABLE`, `NOT_STATED`, `NOT_PUBLISHED`, `NOT_PUBLICLY_VERIFIED`, `NO_FIXED_LIMIT`, `EXPLICIT_UNLIMITED`, `UNVERIFIED`, `USER_ACCOUNT_UNKNOWN`, `DOCUMENT_NOT_RETRIEVED`. Counts are in `data/index.json`.

## Important caveats

- **UNKNOWN means not confirmed.** Treat UNKNOWN as "we do not know", never as a default or a zero.
- A rule value applies to the plan, cohort and version named on the record. Check `checked_at` and the source URL before relying on it.
- Every remaining rule record is a firm rule. Records that only described how the data set is built, and records that depended on a non-public statement, are not part of this export.

## What was removed from the source snapshot

Non-public identifiers, file names and hashes, the maintainers' issue list and lifecycle event list, change references, and working-note sentences in free-text fields. Also removed from the rule list: 815 data-set-description records and 103 records whose source was a non-public user statement (918 rule records in total, from 27,423). In 46 remaining rule values, person names and internal issue ids were replaced by neutral wording. No other rule value, value state, unit or operator was changed.
