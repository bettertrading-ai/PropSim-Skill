# Data dictionary (evidence-based, generated from the exported data)

Source: `data/<slug>.json` of this export, snapshot 2026-10-27 (12 firms, 186 plans, 26,505 rule records). Everything below is counted from the files. No meanings are guessed: where the data does not explain a field or value, the entry says "meaning not documented in the data".

## 1. Metrics by stage

Stage is the `stage` field of the rule record as observed (a few records carry combined stages such as `FUNDED;PAYOUT`). Columns: records, number of firms having the metric in that stage, most frequent `unit` / `value_type` / `operator` (with counts), one example value (truncated, from the export). The meaning of each metric: meaning not documented in the data, unless the metric name and notes make it self-explanatory.

Distinct `metric` values overall: **1861**. Distinct stage values: **42**.

### Stage `PURCHASE` - 4,677 records, 360 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `checkout_total` | 136 | 7 | USD_PRESUMED_UNCONFIRMED (48), USD (45), enum (36) | null (136) | unknown (54), UNKNOWN (38), EQ (36) | (null) |
| `billing_model` | 129 | 11 | text (97), enum (32) | string (120), null (9) | EQ (120), UNKNOWN (9) | one_time_fee |
| `advertised_reference_price` | 123 | 6 | USD_PRESUMED_UNCONFIRMED (72), USD (31), DOLLAR_SYMBOL_ONLY (20) | number (96), object (20), null (7) | EQ (97), AS_STATED (19), unknown (7) | 120 |
| `advertised_coupon_price` | 116 | 5 | USD_PRESUMED_UNCONFIRMED (68), USD (28), DOLLAR_SYMBOL_ONLY (20) | number (93), object (16), null (7) | EQ (109), unknown (7) | 90 |
| `legal_entity` | 92 | 9 | text (53), enum (39) | string (53), object (30), null (9) | EQ (53), AS_STATED (30), UNKNOWN (9) | Bulenox LLC |
| `advertised_coupon_code` | 84 | 5 | enum (63), text (21) | string (84) | EQ (63), AS_STATED (21) | BOTH50 |
| `reset_price` | 64 | 4 | USD_PRESUMED_UNCONFIRMED (34), USD (22), text (8) | null (27), number (23), object (14) | EQ (31), = (16), unknown (8) | 109 |
| `purchase_currency_code` | 57 | 2 | enum (36), ISO_currency (16), unknown (5) | null (57) | EQ (36), UNKNOWN (21) | (null) |
| `advertised_reset_price` | 52 | 1 | USD_PRESUMED_UNCONFIRMED (48), enum (4) | number (48), null (4) | EQ (52) | 50 |
| `refund_eligibility` | 52 | 4 | text (26), boolean (24), enum (2) | string (27), boolean (25) | AS_STATED (26), EQ (24), = (2) | no refunds once an account has been created and the service accessed |
| `nominal_account_size` | 51 | 4 | USD (46), DOLLAR_SYMBOL_ONLY (5) | number (51) | EQ (51) | 50000 |
| `chargeback_policy` | 46 | 4 | text (46) | null (27), string (19) | unknown (27), EQ (19) | chargeback_bars_future_purchases |
| `taxes` | 46 | 4 | USD_PRESUMED_UNCONFIRMED (24), text (13), enum (9) | null (40), string (6) | AS_STATED (30), UNKNOWN (9), unknown (7) | fee is inclusive of VAT/sales tax that FTMO must pay or withhold |
| `governing_law` | 45 | 5 | enum (34), text (11) | object (24), string (12), null (9) | AS_STATED (30), UNKNOWN (9), EQ (5) | Czech law; Czech courts (without prejudice to out-of-court consumer di… |
| `minimum_age` | 45 | 5 | text (24), enum (9), years (7) | string (24), null (14), number (7) | AS_STATED (24), UNKNOWN (14), >= (7) | 18 |
| `account_environment` | 44 | 4 | enum (39), text (5) | string (35), null (9) | AS_STATED (30), UNKNOWN (9), EQ (5) | SIMULATED_EVAL_AND_SIM_FUNDED_THEN_LIVE_BY_INVITATION |
| `activation_fee` | 39 | 3 | USD_PRESUMED_UNCONFIRMED (24), USD (15) | number (39) | EQ (39) | 0 |
| `payment_methods` | 39 | 4 | text (33), enum (6) | array (20), null (13), string (6) | AS_STATED (26), unknown (7), EQ (6) | ["Credit Card","Debit Card","PayPal","Crypto"] |
| `purchase_currency` | 39 | 3 | enum (39) | null (33), string (6) | AS_STATED (24), UNKNOWN (9), EQ (6) | USD |
| `platform_fee` | 38 | 3 | USD (24), enum (9), unknown (5) | number (24), null (14) | AS_STATED (24), UNKNOWN (14) | 0 |
| `refund_policy` | 36 | 3 | text (36) | string (21), null (15) | EQ (21), UNKNOWN (15) | no_refunds |
| `currency` | 35 | 2 | text (20), enum (15) | string (20), null (15) | EQ (20), unknown (15) | USD |
| `kyc_requirement` | 33 | 2 | text (24), enum (9) | object (24), null (9) | AS_STATED (24), UNKNOWN (9) | {"identity_verification":{"provider":"Sumsub (KYC and AML screening; A… |
| `reference_price` | 33 | 2 | USD_PRESUMED_UNCONFIRMED (24), USD (9) | number (24), null (9) | EQ (24), unresolved (9) | 145 |
| `unresolved_contract_cohort` | 32 | 1 | enum (32) | null (32) | AS_STATED (32) | (null) |
| `purchase_price` | 30 | 1 | USD (16), USD_PRESUMED_UNCONFIRMED (14) | null (30) | = (16), UNKNOWN (10), AS_STATED (4) | (null) |
| `restricted_countries` | 30 | 2 | enum (30) | object (30) | AS_STATED (30) | {"natural_persons_only":true,"excluded_nationals_and_residents":["Iran… |
| `unresolved__purchase__extra_fees` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__purchase__payment_restrictions` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__purchase__sale_eligibility` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `coupon_code` | 29 | 2 | text (29) | string (24), null (5) | EQ (20), unresolved (5), AS_STATED (4) | BULENOX |
| `max_funded_accounts` | 29 | 2 | count (29) | number (29) | <= (29) | 5 |
| `platforms` | 28 | 2 | text (28) | string (28) | EQ (28) | Rithmic, Tradovate, WealthCharts |
| `restricted_jurisdictions` | 26 | 3 | text (20), array (5), enum (1) | array (26) | AS_STATED (20), EQ (5), excluded (1) | ["Afghanistan","Albania","Angola","Armenia","Azerbaijan","Bahamas","Ba… |
| `chargeback_consequence` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | permanent ban and forfeiture of all accounts/profits |
| `commission_round_trip_es` | 24 | 1 | USD_PRESUMED_UNCONFIRMED per contract round trip (24) | number (24) | EQ (24) | 5.76 |
| `commission_round_trip_mnq` | 24 | 1 | USD_PRESUMED_UNCONFIRMED per contract round trip (24) | number (24) | EQ (24) | 1.82 |
| `duplicate_accounts_allowed` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | false |
| `market_data_fee_nonpro` | 24 | 1 | USD_PRESUMED_UNCONFIRMED (24) | number (24) | EQ (24) | 0 |
| `market_data_fee_professional_if_nonpro_unsigned` | 24 | 1 | USD_per_month (24) | number (24) | EQ (24) | 300 |
| `refund_exceptions` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | none, except an unapplied promo code corrected via support |
| `time_limited_promo` | 24 | 1 | enum (24) | object (24) | AS_STATED (24) | {"code":"GEMS","discount_ratio":0.3,"banner_as_displayed":"GET 30% OFF… |
| `activation_deadline` | 22 | 3 | enum (9), text (8), unknown (5) | null (22) | UNKNOWN (14), unknown (8) | (null) |
| `taxes_and_mandatory_extras` | 21 | 2 | USD (16), unknown (5) | null (21) | EQ (16), UNKNOWN (5) | (null) |
| `account_size_definition` | 20 | 1 | text (20) | string (20) | EQ (20) | nominal_label |
| `age_and_kyc` | 20 | 1 | text (20) | null (20) | unknown (20) | (null) |
| `bundle_discount` | 20 | 1 | ratio (20) | null (12), number (8) | EQ (10), none (10) | 0.05 |
| `data_fee_nonprofessional_usd` | 20 | 1 | USD (20) | number (20) | EQ (20) | 0 |
| `data_fee_professional_usd_per_month` | 20 | 1 | USD (20) | null (20) | EQ (20) | (null) |
| `entry_fee_usd` | 20 | 1 | USD (20) | number (20) | EQ (20) | 115 |
| `exchanges` | 20 | 1 | text (20) | array (20) | EQ (20) | ["CME","CBOT","NYMEX","COMEX"] |
| `public_pricing_listing` | 20 | 1 | text (20) | string (16), null (4) | EQ (20) | listed |
| `risk_model_choice_locked` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | true |
| `rithmic_declaration_locked` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | true |
| `sales_tax_policy` | 20 | 1 | text (20) | string (20) | AS_STATED (20) | sales tax will be added to the sales price of purchases as deemed requ… |
| `third_party_api_software_fee_usd_per_month` | 20 | 1 | USD (20) | number (20) | EQ (20) | 100 |
| `unresolved__purchase__activation_deadline` | 20 | 3 | enum (20) | null (20) | UNKNOWN (20) | (null) |
| `checkout_total_usd` | 18 | 1 | USD (18) | null (18) | unresolved (18) | (null) |
| `evaluation_fee_one_time_usd` | 18 | 1 | USD (18) | null (15), number (3) | unresolved (15), EQ (3) | 140 |
| `plan_card_listed_on_official_page` | 18 | 1 | boolean (18) | boolean (14), null (4) | EQ (14), unresolved (4) | true |
| `account_agreement_verified` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | false |
| `account_cohort_verified` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | false |
| `account_size_meaning` | 16 | 2 | enum (9), text (7) | null (16) | UNKNOWN (9), unknown (7) | (null) |
| `advertised_coupon_banner` | 16 | 1 | text (16) | string (16) | AS_STATED (16) | BULENOX - applies the best available discount to Qualification, Fast T… |
| `advertised_discount_amount` | 16 | 1 | USD (16) | null (16) | unknown (16) | (null) |
| `after_trade_refundable` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | false |
| `billing_mode` | 16 | 1 | enum (16) | string (16) | EQ (16) | ONE_TIME |
| `billing_type` | 16 | 1 | enum (16) | string (16) | = (16) | one_time |
| `configuration_change_allowed` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | false |
| `configuration_change_path` | 16 | 1 | enum (16) | string (16) | = (16) | new purchase |
| `configurator_addon_price_labels` | 16 | 1 | USD_PRESUMED_UNCONFIRMED (16) | object (16) | AS_STATED (16) | {"25K":{"consistency_50_addon_label_when_dll_on":"+$4.90","consistency… |
| `configurator_consistency_addon_label` | 16 | 1 | USD_PRESUMED_UNCONFIRMED (16) | null (8), number (8) | none (8), AS_STATED (8) | 4.9 |
| `configurator_on_demand_payouts_toggle` | 16 | 1 | enum (16) | string (16) | AS_STATED (16) | ON |
| `consistency_option_price_effect` | 16 | 1 | enum (16) | object (16) | AS_STATED (16) | {"40_PERCENT_STANDARD":"Lowest price","50_PERCENT_ADDON":"Added at che… |
| `coupon_eligibility` | 16 | 2 | enum (9), text (7) | null (16) | unresolved (9), unknown (7) | (null) |
| `coupon_line_price_single` | 16 | 1 | USD (16) | number (16) | AS_STATED (16) | 49 |
| `eval_list_price_five_pack` | 16 | 1 | USD (16) | number (14), null (2) | EQ (14), none (2) | 2250 |
| `eval_list_price_single` | 16 | 1 | USD (16) | number (16) | EQ (16) | 490 |
| `max_evaluation_purchases_per_30d` | 16 | 1 | count (16) | number (16) | <= (16) | 15 |
| `max_resets_per_eval_per_30d` | 16 | 1 | count (16) | number (16) | <= (16) | 10 |
| `monthly_rebilling` | 16 | 1 | boolean (16) | boolean (16) | = (16) | false |
| `price_order` | 16 | 1 | enum (16) | string (16) | = (16) | DLL ON + Intraday lowest; DLL OFF + EOD highest; other two intermediat… |
| `store_catalogue_price` | 16 | 1 | USD (16) | object (16) | AS_STATED (16) | {"25K":{"purchase":65,"reset":45},"50K":{"purchase":115,"reset":80},"1… |
| `struck_list_price` | 16 | 1 | USD (16) | null (16) | unknown (16) | (null) |
| `unresolved__purchase__purchasable_configuration` | 16 | 3 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `age_requirement` | 15 | 1 | years (15) | number (15) | GE (15) | 18 |
| `billing_cycle` | 15 | 1 | text (15) | string (15) | EQ (15) | renews_every_30_days_until_review_or_cancel |
| `cancel_subscription` | 15 | 1 | text (15) | string (15) | EQ (15) | dashboard_manage_subscriptions_cancel_button_processed_immediately_bus… |
| `geographic_restrictions` | 15 | 1 | text (15) | string (15) | EQ (15) | certain geographic restrictions apply; eligibility shown on sign-up pa… |
| `legal_entity_address` | 15 | 1 | text (15) | string (15) | EQ (15) | 1007 N. Orange St. 4th Floor, Wilmington, Delaware 19801 |
| `legal_entity_name` | 15 | 1 | text (15) | null (15) | UNKNOWN (15) | (null) |
| `level2_market_depth_addon_price` | 15 | 1 | USD (15) | null (15) | unknown (15) | (null) |
| `max_evaluation_accounts` | 15 | 1 | count (15) | number (15) | EQ (15) | 3 |
| `payment_card_name_policy` | 15 | 1 | text (15) | string (15) | EQ (15) | card_must_be_registered_under_user_name |
| `plan_sale_status` | 15 | 1 | text (15) | string (14), null (1) | EQ (14), unresolved (1) | LISTED_IN_PLAN_PICKER |
| `priceslash_addon_price` | 15 | 1 | USD (15) | null (15) | unknown (15) | (null) |
| `promo_price_code` | 15 | 1 | enum (15) | null (15) | none (10), unknown (5) | (null) |
| `purchasable_configs` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `rebill_amount` | 15 | 3 | enum (9), unknown (5), USD (1) | null (14), number (1) | UNKNOWN (14), EQ (1) | 95 |
| `registration_accounts_per_user` | 15 | 1 | accounts (15) | number (15) | EQ (15) | 1 |
| `rithmic_id_policy` | 15 | 1 | text (15) | string (15) | EQ (15) | one_rithmic_id_per_email_no_multi_email |
| `subscription_fee_monthly` | 15 | 1 | USD (15) | number (10), null (5) | EQ (10), UNKNOWN (5) | 65 |
| `support_availability` | 15 | 1 | text (15) | string (15) | EQ (15) | 24_7_phone_chat_email |
| `supported_platforms` | 15 | 1 | text (15) | string (15) | EQ (15) | 20plus_ninjatrader_free |
| `allowed_products` | 14 | 2 | text (14) | string (8), null (6) | EQ (8), UNKNOWN (6) | CME futures (ES, NQ, YM, RTY, 6A/6B/6C/6E/6J/6S/6N, HE/LE/GF, ZC/ZW/ZS… |
| `cancel_anytime` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `configuration_catalogue` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `coupon_line_price_five_pack` | 14 | 1 | USD (14) | number (14) | AS_STATED (14) | 225 |
| `data_fee` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `double_down_deal_addon_from` | 14 | 1 | USD (14) | number (14) | EQ (14) | 47 |
| `funded_activation_monthly` | 14 | 1 | USD (14) | number (14) | EQ (14) | 87 |
| `funded_activation_onetime` | 14 | 1 | USD (14) | number (9), string (5) | EQ (14) | 177 |
| `kyc_required` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `max_active_dtf_accounts` | 14 | 1 | accounts (14) | number (14) | EQ (14) | 5 |
| `max_active_elite_simfunded_accounts` | 14 | 1 | accounts (14) | number (14) | EQ (14) | 20 |
| `minimum_age_years` | 14 | 1 | years (14) | number (14) | GE (14) | 18 |
| `professional_market_data_fee` | 14 | 1 | USD (14) | number (14) | EQ (14) | 128 |
| `promo_discount_active` | 14 | 1 | promo (14) | boolean (14) | EQ (14) | true |
| `rebill_date` | 14 | 2 | enum (9), text (5) | null (9), string (5) | UNKNOWN (9), EQ (5) | same calendar day of original first subscription account purchase |
| `refund_restrictions` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `rise_restricted_countries` | 14 | 1 | country_list (14) | array (14) | EQ (14) | ["Afghanistan","Central African Republic","Congo (Brazzaville)","Cuba"… |
| `us_territories_unsupported` | 14 | 1 | territory_list (14) | array (14) | EQ (14) | ["Guam","Puerto Rico","United States Virgin Islands"] |
| `billing` | 12 | 1 | enum (12) | string (12) | = (12) | One-time; no automatic rebilling |
| `unresolved__purchase__chargeback` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `advertised_coupon_discount_ratio` | 11 | 1 | ratio (11) | number (11) | EQ (11) | 0.4 |
| `advertised_first_eval_discount_ratio` | 11 | 1 | ratio (11) | number (11) | EQ (11) | 0.5 |
| `advertised_promo_end_date` | 11 | 1 | date (11) | null (11) | EQ (11) | (null) |
| `subscription_cancellation` | 11 | 2 | text (6), unknown (5) | string (6), null (5) | AS_STATED (6), UNKNOWN (5) | cancel anytime in Client Area; stops future billing; access until end … |
| `availability` | 10 | 1 | enum (10) | null (10) | unknown (10) | (null) |
| `data_fees` | 10 | 1 | text (10) | string (10) | EQ (10) | none |
| `eval_reset_fee` | 10 | 1 | USD (10) | number (10) | EQ (10) | 47 |
| `free_trial_days` | 10 | 1 | days (10) | number (10) | EQ (10) | 7 |
| `unresolved__purchase__reset_timing` | 10 | 2 | enum (10) | null (10) | UNKNOWN (10) | (null) |
| `advertised_coupon_discount_first_month` | 9 | 1 | ratio (9) | number (9) | EQ (9) | 0.9 |
| `advertised_coupon_discount_later_months` | 9 | 1 | ratio (9) | object (9) | EQ (9) | {"month_2":0.8,"month_3_plus":0.7} |
| `advertised_coupon_expiry` | 9 | 1 | text (9) | string (9) | before_expiry (9) | Oct 31 11:59 PM ET (year not displayed) |
| `chargeback` | 9 | 1 | enum (9) | string (9) | AS_STATED (9) | dispute_or_chargeback_breaches_terms; possible termination of active a… |
| `coupon_expiry` | 9 | 1 | enum (9) | null (9) | N/A (9) | (null) |
| `coupon_price` | 9 | 1 | USD (9) | null (9) | unresolved (9) | (null) |
| `duplicate_accounts` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `extras` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `max_accounts` | 9 | 1 | object (9) | object (9) | AS_STATED (9) | {"challenge_phase1_accounts":"UNLIMITED","performance_accounts_max":3,… |
| `one_day_to_pass_addon_price` | 9 | 1 | USD (9) | null (9) | unknown (9) | (null) |
| `payment_restrictions` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `public_or_invited_eligibility` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `rebill_cancel` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `refund` | 9 | 1 | enum (9) | null (9) | unresolved (9) | (null) |
| `reset_available` | 9 | 2 | boolean (9) | boolean (9) | EQ (9) | true |
| `reset_fee` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `reset_timing` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `residence_restrictions` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `supported_countries` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `trading_commission` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `charge_currency` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `configurator_dll_off_addon_label` | 8 | 1 | USD_PRESUMED_UNCONFIRMED (8) | number (8) | AS_STATED (8) | 14.7 |
| `consistency_addon_price` | 8 | 1 | USD_PRESUMED_UNCONFIRMED (8) | number (8) | EQ (8) | 40 |
| `consistency_addon_selected` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | true |
| `coupon_labelled_card_prices_select_plan_page` | 8 | 1 | enum (8) | object (8) | AS_STATED (8) | {"code":"JUNE","where":"/select-plan (and /select-plan-paid-daily for … |
| `coverage_gap__000` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__001` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__002` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__003` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__004` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__005` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__006` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__007` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__008` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__009` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__010` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__011` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__012` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__013` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__014` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__015` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `eval_fee_refundable` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | false |
| `eval_rebill_exists` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | false |
| `five_pack_availability_no_activation_fee` | 8 | 1 | enum (8) | object (8) | AS_STATED (8) | {"INTRADAY":{"25K":true,"50K":true,"100K":true,"150K":true},"EOD":{"25… |
| `five_pack_availability_standard` | 8 | 1 | enum (8) | object (8) | AS_STATED (8) | {"INTRADAY":{"25K":true,"50K":true,"100K":true,"150K":true},"EOD":{"25… |
| `legacy_accounts_available` | 8 | 1 | boolean (8) | null (8) | unresolved (8) | (null) |
| `list_price_includes_promo` | 8 | 1 | boolean (8) | null (8) | unresolved (8) | (null) |
| `max_evaluation_accounts_per_user` | 8 | 1 | count (8) | null (8) | EQ (8) | (null) |
| `max_payout_displayed_select_plan_vs_homepage` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `platform_dependent_price` | 8 | 1 | USD (8) | null (8) | unresolved (8) | (null) |
| `pricing_one_time_fee` | 8 | 1 | USD (8) | null (8) | EQ (8) | (null) |
| `promo_code_advertised` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | SAVENOW |
| `promo_discount_advertised` | 8 | 1 | ratio (8) | number (8) | AS_STATED (8) | 0.9 |
| `promo_validity` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | banner countdown showed about 1 day 21 hours remaining at read time; e… |
| `reset_eligibility_timing` | 8 | 1 | text (8) | null (8) | unknown (8) | (null) |
| `reset_values_displayed_select_plan_page` | 8 | 1 | enum (8) | object (8) | AS_STATED (8) | {"by_size":{"25K":{"struck":75,"lower_value":65},"50K":{"single_value"… |
| `single_login_policy` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | true |
| `tax_and_extra_fees_at_checkout` | 8 | 1 | USD (8) | null (8) | unresolved (8) | (null) |
| `account_holder_exclusivity` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | true |
| `activation_fee_charged_at_purchase` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | false |
| `advertised_coupon_discount` | 7 | 1 | ratio (7) | number (7) | EQ (7) | 0.5 |
| `advertised_from_price` | 7 | 1 | USD (7) | number (7) | EQ (7) | 75 |
| `advertised_reset_discount` | 7 | 1 | ratio (7) | number (7) | EQ (7) | 0.5 |
| `commission_blackarrow_per_side_table` | 7 | 1 | USD (7) | object (7) | EQ (7) | {"ES":2.04,"NQ":2.04,"MYM":0.93,"M2K":0.93,"UB":2.01,"ZN":1.46,"GC":2.… |
| `commission_change_notice` | 7 | 1 | text (7) | string (7) | EQ (7) | liable_to_change_without_warning |
| `commission_micro_per_side_range` | 7 | 1 | USD (7) | object (7) | EQ (7) | {"min": 0.82, "max": 1.2, "unit": "USD"} |
| `commission_model` | 7 | 1 | text (7) | string (7) | EQ (7) | live_commissions_mirror_partners |
| `commission_rithmic_per_side_table` | 7 | 1 | USD (7) | object (7) | EQ (7) | {"ES": 2.04, "NQ": 2.04, "MYM": 0.93, "M2K": 0.93, "UB": 2.01, "ZN": 1… |
| `commission_tradovate_per_side_table` | 7 | 1 | USD (7) | object (7) | EQ (7) | {"ES":2.88,"NQ":2.88,"MYM":0.95,"M2K":0.95,"ZB":2.37,"ZN":2.3,"GC":3.1… |
| `coupon_end_date` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `currency_code` | 7 | 1 | text (7) | null (7) | UNKNOWN (7) | (null) |
| `data_fees_eval_nonprofessional` | 7 | 1 | text (7) | string (7) | EQ (7) | included_in_subscription |
| `data_fees_eval_professional_ninjatrader_per_exchange_month` | 7 | 1 | USD (7) | number (7) | EQ (7) | 156 |
| `data_fees_eval_professional_rithmic_per_exchange_month` | 7 | 1 | USD (7) | number (7) | EQ (7) | 140 |
| `eligibility_exclusions` | 7 | 1 | text (7) | array (7) | EQ (7) | ["felony_conviction", "nfa_disciplined", "cftc_disciplined", "outstand… |
| `eligibility_min_age` | 7 | 1 | years (7) | number (7) | GTE (7) | 18 |
| `eval_monthly_price` | 7 | 1 | USD (7) | null (7) | UNKNOWN (7) | (null) |
| `evaluation_environment` | 7 | 1 | text (7) | string (7) | EQ (7) | simulated_virtual_realtime_data |
| `failed_billing_cancel_after_attempts` | 7 | 1 | count (7) | number (7) | EQ (7) | 3 |
| `market_depth_dom_fee` | 7 | 1 | text (7) | string (7) | EQ (7) | additional_monthly_fee_required |
| `max_concurrent_eval_accounts` | 7 | 1 | count (7) | number (7) | EQ (7) | 5 |
| `platforms_available` | 7 | 1 | text (7) | array (7) | EQ (7) | ["BlackArrow","DeepCharts","Finamark","NinjaTrader","Rithmic","Trading… |
| `platforms_futures` | 7 | 1 | text (7) | string (7) | EQ (7) | Tradovate |
| `platforms_help_article_list` | 7 | 1 | text (7) | object (7) | EQ (7) | {"marked_free":["NinjaTrader","Finamark","R\|Trader","R\|Trader Pro","… |
| `pricing_one_time` | 7 | 1 | USD (7) | null (7) | EQ (7) | (null) |
| `purchase_price_platform_axis` | 7 | 1 | text (7) | object (7) | EQ (7) | {"platforms_compared":["Rithmic","NinjaTrader","BlackArrow","dxFeed x … |
| `rebill_reminder_days_before` | 7 | 1 | days (7) | number (7) | EQ (7) | 3 |
| `reset_billing_effect` | 7 | 1 | text (7) | string (7) | EQ (7) | no_billing_restart_reverts_balance_clears_fails |
| `reset_howto` | 7 | 1 | text (7) | string (7) | EQ (7) | dashboard_evaluation_tab_reset_button |
| `reset_price_current` | 7 | 1 | USD (7) | number (7) | EQ (7) | 100 |
| `reset_price_structure` | 7 | 1 | text (7) | string (7) | EQ (7) | dynamic_25_50k_fixed_100_200k |
| `sanctioned_countries_funding_blocked` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | true |
| `subscription_cancel_process` | 7 | 1 | text (7) | string (7) | EQ (7) | dashboard_double_confirm_forfeit |
| `subscription_price_monthly` | 7 | 1 | USD (7) | number (7) | EQ (7) | 150 |
| `subscription_rebill_cycle_days` | 7 | 1 | days (7) | number (7) | EQ (7) | 30 |
| `breach_handling_subscription` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | subscription stays active; new account on next billing date |
| `evaluation_account_creation_time` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | usually within one hour of payment; in most cases not more than 24 hou… |
| `evaluation_accounts_limit` | 6 | 1 | count (6) | null (6) | AS_STATED (6) | (null) |
| `exchange_fee_per_contract` | 6 | 1 | USD per contract (6) | null (6) | UNKNOWN (6) | (null) |
| `extra_fees_beyond_subscription` | 6 | 1 | enum (6) | null (6) | AS_STATED (6) | (null) |
| `ftmo_commission_per_side_micro` | 6 | 1 | USD per side per contract (6) | number (6) | EQ (6) | 0.2 |
| `ftmo_commission_per_side_mini` | 6 | 1 | USD per side per contract (6) | number (6) | EQ (6) | 0.5 |
| `kyc_requirements` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | natural person 18+; KYC/KYB; sanctions screening; US: SSN/W-9/bank pro… |
| `level1_market_data_included` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `level2_dom_purchasable` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `max_combines_per_profile` | 6 | 1 | count (6) | null (6) | EQ (6) | (null) |
| `max_sim_funded_accounts` | 6 | 1 | count (6) | number (6) | <= (6) | 3 |
| `min_age` | 6 | 1 | years (6) | number (6) | >= (6) | 18 |
| `monthly_price_rta_off` | 6 | 1 | USD (6) | number (6) | EQ (6) | 49 |
| `monthly_price_rta_on` | 6 | 1 | USD (6) | number (6) | EQ (6) | 49 |
| `multiple_registrations_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `nfa_fee_per_contract` | 6 | 1 | USD per contract (6) | null (6) | UNKNOWN (6) | (null) |
| `no_transfer_between_evaluations` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `not_eligible_if_live_account_held` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `payment_failure_access_paused` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `payment_failure_after_grace` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | account is closed |
| `payment_failure_grace_period_hours` | 6 | 1 | hours (6) | number (6) | EQ (6) | 48 |
| `payment_owner` | 6 | 2 | unknown (5), enum (1) | null (5), string (1) | UNKNOWN (5), = (1) | Authorized personal payment method |
| `platform_included_in_subscription` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `price_change_notice_days` | 6 | 1 | days (6) | number (6) | >= (6) | 14 |
| `promo_combinability` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | benefits/promo codes not combinable unless stated |
| `rebill_interval` | 6 | 1 | calendar_days (6) | number (6) | EQ (6) | 30 |
| `reference_price_monthly` | 6 | 1 | USD per month (6) | number (6) | EQ (6) | 119 |
| `refund_window_days` | 6 | 1 | days (6) | number (6) | <= (6) | 28 |
| `renewal_retry_count` | 6 | 1 | attempts (6) | number (6) | EQ (6) | 2 |
| `reset_changes_billing_cycle` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `reset_credit_on_rebill` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `reset_price_with_rta` | 6 | 1 | USD (6) | object (6) | EQ (6) | {"50000":85,"100000":129,"150000":199} |
| `reset_purchase_requires_3ds` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `restricted_countries_exist` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `sale_eligibility` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | natural persons only; available globally except listed exceptions |
| `subscription_cancellable` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `subscription_pausable` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `unresolved__purchase__account_environment` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__activation_fee` | 6 | 1 | USD (6) | object (6) | EQ (6) | {"TOPSTEP_COMBINE_50K_STD":149,"TOPSTEP_COMBINE_100K_STD":149,"TOPSTEP… |
| `unresolved__purchase__commission_cost` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__coupon_code` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__coupon_eligibility` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__coupon_expiry` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__data_fee` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__duplicate_accounts` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__governing_law` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__kyc_requirements` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__nominal_account_size` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__platform_fee` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__purchase_currency` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__rebill_amount` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__reference_price` | 6 | 1 | USD (6) | object (6) | EQ (6) | {"TOPSTEP_COMBINE_50K_STD":49,"TOPSTEP_COMBINE_50K_NAF":95,"TOPSTEP_CO… |
| `unresolved__purchase__refund_restrictions` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__reset_price` | 6 | 1 | USD (6) | object (6) | EQ (6) | {"TOPSTEP_COMBINE_50K_STD":49,"TOPSTEP_COMBINE_50K_NAF":95,"TOPSTEP_CO… |
| `unresolved__purchase__restricted_countries` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__purchase__taxes` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `us_citizenship_required` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `add_on_fee` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `advertised_coupon_applies` | 5 | 1 | text (5) | null (5) | unknown (5) | (null) |
| `available_data_feeds` | 5 | 1 | array (5) | array (5) | EQ (5) | ["Rithmic","CQG"] |
| `kyc_outcomes` | 5 | 1 | array (5) | array (5) | EQ (5) | ["approved","manual review","approved but retry flag","rejected"] |
| `plan_availability` | 5 | 1 | text (5) | null (5) | unknown (5) | (null) |
| `platform_license_table` | 5 | 1 | object (5) | object (5) | EQ (5) | {"columns":["platform","free_during_test","data_feed"],"rows":[["Tradi… |
| `platform_switch_same_feed_allowed` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | true |
| `pricing_monthly` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | null (5) | UNKNOWN (5) | (null) |
| `promotion_eligibility` | 5 | 1 | text (5) | string (5) | AS_STATED (5) | every Test account created with the code; unlimited code use; Test acc… |
| `promotion_expiry` | 5 | 1 | enum (5) | null (5) | N/A (5) | (null) |
| `purchase_eligibility` | 5 | 1 | text (5) | string (5) | EQ (5) | email confirmed and KYC completed before first Test purchase/trading |
| `refund_deduction` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | number (5) | EQ (5) | 75 |
| `refund_request_window` | 5 | 1 | hours (5) | number (5) | EQ (5) | 72 |
| `registered_email_limit` | 5 | 1 | count (5) | number (5) | EQ (5) | 1 |
| `rule_break_no_auto_cancel` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | true |
| `subscription_auto_cancel_on_pass` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | true |
| `test_account_fixed_limit` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `test_credentials_typical_latency` | 5 | 1 | text (5) | string (5) | EQ (5) | a few minutes after purchase; contact support if absent after1hour |
| `used_or_traded_refund_eligible` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `verification_documents` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `access` | 4 | 1 | enum (4) | string (4) | = (4) | Risk-team invitation; email notification; no application timeline |
| `checkout_total_price` | 4 | 1 | text (4) | null (4) | unknown (4) | (null) |
| `configuration_addons_available` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | false |
| `coupon_discount_and_eligibility` | 4 | 1 | text (4) | null (4) | unknown (4) | (null) |
| `coupon_validity_period` | 4 | 1 | text (4) | null (4) | unknown (4) | (null) |
| `evaluation_stage_exists` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | false |
| `gm_free_reset_on_rebill` | 4 | 1 | boolean (4) | null (4) | unknown (4) | (null) |
| `new_purchase_while_live` | 4 | 1 | enum (4) | boolean (4) | prohibited (4) | false |
| `no_evaluation` | 4 | 1 | enum (4) | boolean (4) | AS_STATED (4) | true |
| `pricing_standard_path_monthly` | 4 | 1 | USD (4) | object (3), number (1) | EQ (4) | {"50000":49,"100000":99,"150000":199} |
| `struck_through_list_price` | 4 | 1 | text (4) | null (4) | unknown (4) | (null) |
| `unresolved_checkout_total` | 4 | 1 | enum (4) | null (4) | AS_STATED (4) | (null) |
| `account_size_usd` | 3 | 1 | USD (3) | null (3) | unresolved (3) | (null) |
| `dtf_onetime_price_card` | 3 | 1 | USD (3) | number (3) | EQ (3) | 747 |
| `dtf_onetime_price_floor_advertised` | 3 | 1 | USD (3) | null (3) | unknown (3) | (null) |
| `dtf_reset_fee` | 3 | 1 | USD (3) | number (3) | EQ (3) | 200 |
| `responsible_trading_dll_discount_monthly` | 3 | 1 | USD (3) | object (3) | EQ (3) | {"50000":10,"100000":20,"150000":30} |
| `studio_plans_exist` | 3 | 1 | boolean (3) | boolean (3) | EQ (3) | true |
| `studio_purchasable_today` | 3 | 1 | boolean (3) | null (3) | unresolved (3) | (null) |
| `tcp_free_reset_on_rebill` | 3 | 1 | boolean (3) | boolean (3) | EQ (3) | true |
| `tradeshield_addon_price` | 3 | 1 | USD (3) | null (3) | unknown (3) | (null) |
| `eval_monthly_price_advertised` | 2 | 1 | USD (2) | null (2) | unknown (2) | (null) |
| `eval_monthly_price_card` | 2 | 1 | USD (2) | number (1), null (1) | EQ (1), unresolved (1) | 147 |
| `eval_onetime_price_card` | 2 | 1 | USD (2) | number (2) | EQ (2) | 57 |
| `eval_reset_available` | 2 | 1 | boolean (2) | boolean (2) | EQ (2) | false |
| `fasttrack_purchase_limit` | 2 | 1 | accounts (2) | number (2) | EQ (2) | 1 |
| `funded_activation_fasttrack_first_month` | 2 | 1 | boolean (2) | boolean (2) | EQ (2) | true |
| `advertised_limited_time_savings` | 1 | 1 | USD_PRESUMED_UNCONFIRMED (1) | object (1) | EQ (1) | {"list_price":146,"price_before_savings":105.2,"savings_label":"LIMITE… |
| `card_brands` | 1 | 1 | enum (1) | array (1) | = (1) | ["Visa","Mastercard","American Express","Discover","Diners Club","Maes… |
| `claim_time_limit` | 1 | 1 | year (1) | number (1) | <= (1) | 1 |
| `commission_round_trip_usd_cl` | 1 | 1 | USD (1) | number (1) | EQ (1) | 4.92 |
| `commission_round_trip_usd_es` | 1 | 1 | USD (1) | number (1) | EQ (1) | 4.68 |
| `commission_round_trip_usd_gc` | 1 | 1 | USD (1) | number (1) | EQ (1) | 5.12 |
| `commission_round_trip_usd_mcl` | 1 | 1 | USD (1) | number (1) | EQ (1) | 1.16 |
| `commission_round_trip_usd_mes` | 1 | 1 | USD (1) | number (1) | EQ (1) | 1.9 |
| `commission_round_trip_usd_mgc` | 1 | 1 | USD (1) | number (1) | EQ (1) | 2.2 |
| `commission_round_trip_usd_mnq` | 1 | 1 | USD (1) | number (1) | EQ (1) | 1.9 |
| `commission_round_trip_usd_nq` | 1 | 1 | USD (1) | number (1) | EQ (1) | 4.68 |
| `compensation` | 1 | 1 | enum (1) | string (1) | = (1) | No obligation |
| `consequence` | 1 | 1 | enum (1) | string (1) | = (1) | Permanent ban; possible recovery of funds/costs |
| `environment` | 1 | 1 | text (1) | string (1) | EQ (1) | simulated |
| `evaluation_fees_refundable` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | false |
| `excluded_statuses` | 1 | 1 | enum (1) | array (1) | excluded (1) | ["Convicted felon","NFA discipline","CFTC discipline","Outstanding tra… |
| `legacy_page_coupon_line_price_monthly` | 1 | 1 | USD (1) | object (1) | AS_STATED (1) | {"25K":17.7,"50K":19.7,"100K":21.0,"150K":59.7,"250K":21.0,"300K":21.0… |
| `legacy_page_displayed_terms` | 1 | 1 | USD (1) | object (1) | AS_STATED (1) | {"trailing_threshold":{"25K":1500,"50K":2500,"100K":3000,"150K":5000,"… |
| `legacy_page_list_price_monthly` | 1 | 1 | USD (1) | object (1) | EQ (1) | {"25K":177,"50K":197,"100K":210,"150K":597,"250K":210,"300K":210} |
| `legacy_page_pa_fee` | 1 | 1 | USD (1) | object (1) | EQ (1) | {"25K":99,"50K":125,"100K":149,"150K":179,"250K":189,"300K":199} |
| `mbt_counts_as_mini` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `permitted_exchanges` | 1 | 1 | text (1) | string (1) | EQ (1) | CME Group (CME, CBOT, NYMEX, COMEX) |
| `profile_limit` | 1 | 1 | permanent profile (1) | number (1) | = (1) | 1 |
| `profile_type_changes` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `prohibited_instruments` | 1 | 1 | text (1) | string (1) | EQ (1) | equities, equity options, cryptocurrencies, CFDs, OTC |
| `rebill_amount_with_dll_at_purchase` | 1 | 1 | USD (1) | number (1) | EQ (1) | 85 |
| `registered_address` | 1 | 1 | text (1) | string (1) | EQ (1) | 108 Lakeland Ave, Dover, DE 19901 |

### Stage `PAYOUT` - 4,655 records, 366 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `unresolved_business_day_calendar` | 48 | 1 | enum (48) | null (48) | AS_STATED (48) | (null) |
| `payout_consistency` | 47 | 5 | ratio (22), enum (15), unknown (10) | null (25), number (22) | <= (18), unknown (15), UNKNOWN (10) | 0.35 |
| `trader_split` | 38 | 3 | ratio (38) | number (38) | EQ (30), = (8) | 0.9 |
| `payout_methods` | 36 | 3 | text (31), unknown (5) | null (25), string (11) | EQ (31), UNKNOWN (5) | Plaid (US bank), Routable (international), PayPal, Wise |
| `unresolved__payout__business_day_calendar` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__cancelled_state` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__delayed_state` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__failed_payment_state` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__first_cycle_start` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__fixed_fee` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__lifetime_cap` | 36 | 3 | enum (30), USD (6) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__max_payout_count` | 36 | 3 | enum (30), count (6) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__net_receipt` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__payout_count_increment` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__per_cycle_cap` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__request_cutoff` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__request_timezone` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__resubmit_state` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__variable_fee` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__payout__cumulative_profit` | 32 | 3 | enum (32) | null (32) | UNKNOWN (32) | (null) |
| `unresolved__payout__days_reset` | 32 | 3 | enum (32) | null (32) | UNKNOWN (32) | (null) |
| `unresolved__payout__denied_state` | 32 | 3 | enum (32) | null (32) | UNKNOWN (32) | (null) |
| `unresolved__payout__pending_buffer_risk` | 32 | 3 | enum (32) | null (32) | UNKNOWN (32) | (null) |
| `unresolved__payout__remaining_balance` | 32 | 3 | enum (32) | null (32) | UNKNOWN (32) | (null) |
| `unresolved_cycle_pending_attribution` | 32 | 1 | enum (32) | null (32) | AS_STATED (32) | (null) |
| `unresolved_denied_request_reversal` | 32 | 1 | enum (32) | null (32) | AS_STATED (32) | (null) |
| `minimum_request` | 30 | 2 | USD (30) | number (30) | >= (22), EQ (8) | 20 |
| `unresolved__payout__net_fee_basis` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__payout__cycle_reset` | 28 | 3 | enum (28) | null (28) | UNKNOWN (28) | (null) |
| `unresolved__payout__payout_count_tiers` | 28 | 3 | enum (28) | null (28) | UNKNOWN (28) | (null) |
| `unresolved__payout__request_cancel` | 28 | 3 | enum (28) | null (28) | UNKNOWN (28) | (null) |
| `unresolved_payout_debit_basis` | 28 | 1 | enum (28) | null (28) | AS_STATED (28) | (null) |
| `qualifying_days` | 27 | 3 | days (18), enum (9) | number (18), null (9) | >= (18), UNKNOWN (9) | 4 |
| `payout_buffer_balance` | 26 | 3 | USD (16), DOLLAR_SYMBOL_ONLY (5), unknown (5) | number (21), null (5) | >= (8), = (8), EQ (5) | 26100 |
| `consistency_reset_after_approved_payout` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | true |
| `payout_approval_max_time` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | Company may take up to the end of the next payout cycle to approve, re… |
| `payout_frequency` | 24 | 3 | text (24) | string (24) | AS_STATED (14), EQ (10) | every 4 days |
| `payout_cap_denominator` | 22 | 2 | enum (15), text (7) | null (22) | unknown (22) | (null) |
| `payout_count_ladder` | 22 | 2 | enum (15), text (7) | null (22) | unknown (22) | (null) |
| `payout_count_tiers` | 22 | 2 | text (12), unknown (10) | null (22) | unknown (12), UNKNOWN (10) | (null) |
| `per_request_cap` | 22 | 2 | USD (22) | number (22) | <= (22) | 2500 |
| `trade_after_request` | 22 | 3 | boolean (14), event (8) | boolean (14), string (8) | AS_STATED (8), = (8), EQ (6) | true |
| `unresolved__payout__account_debit_basis` | 22 | 2 | enum (22) | null (22) | UNKNOWN (22) | (null) |
| `payout_deduction_timing` | 21 | 3 | text (13), timing (8) | null (13), string (8) | = (8), unknown (7), unresolved (6) | minutes_after_approval |
| `consistency_max_single_day_pct` | 20 | 1 | ratio (20) | number (12), null (8) | <= (20) | 0.4 |
| `denied_cancelled_state_recovery` | 20 | 1 | text (20) | null (20) | unknown (20) | (null) |
| `max_open_requests` | 20 | 1 | count (20) | number (20) | <= (20) | 1 |
| `max_withdrawal_usd` | 20 | 1 | USD (20) | number (12), null (8) | <= (20) | 750 |
| `min_trading_days_per_payout` | 20 | 1 | days (20) | number (12), null (8) | >= (20) | 10 |
| `min_withdrawal_usd` | 20 | 1 | USD (20) | number (16), null (4) | >= (20) | 500 |
| `net_profit_required` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | true |
| `payout_processing_fee` | 20 | 1 | USD (20) | number (20) | EQ (20) | 0 |
| `payout_request_forms` | 20 | 1 | text (20) | string (20) | EQ (20) | request via personal profile on Bulenox.com: Submit New Ticket with 'W… |
| `payout_schedule` | 20 | 1 | text (20) | null (20) | EQ (20) | (null) |
| `profit_split_after_ratio` | 20 | 1 | ratio (20) | number (20) | EQ (20) | 0.9 |
| `profit_split_first_10000_usd` | 20 | 1 | ratio (20) | null (16), number (4) | EQ (20) | 0.9 |
| `request_cancel_pending_trading` | 20 | 1 | text (20) | null (20) | unknown (20) | (null) |
| `safety_threshold_reserve_usd` | 20 | 1 | USD (20) | number (12), null (8) | >= (20) | 1100 |
| `str_release_on_termination` | 20 | 1 | text (20) | string (20) | EQ (20) | 20% of net STR if <45 active trading days; 50% if 46-100; 80% if >100;… |
| `trader_tax_status` | 20 | 1 | text (20) | null (20) | EQ (20) | (null) |
| `unresolved__payout__buffer_formula` | 20 | 3 | enum (20) | null (20) | UNKNOWN (20) | (null) |
| `unresolved__payout__pending_trading` | 20 | 1 | enum (20) | null (20) | UNKNOWN (20) | (null) |
| `account_debit_basis` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `business_day_calendar` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `cancelled_request_state` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `cumulative_profit_required` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `cycle_profit_required` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `denied_request_state` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `failed_payment_state` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `first_cycle_start` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `lifetime_cap` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `minimum_profit_per_winning_day` | 19 | 3 | USD (14), enum (5) | number (10), null (9) | >= (10), UNKNOWN (5), AS_STATED (4) | 150 |
| `pending_trading_allowed` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `request_cutoff` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `cap_denominator` | 18 | 2 | unknown (10), text (8) | null (18) | UNKNOWN (10), unknown (8) | (null) |
| `minimum_day_profit` | 18 | 2 | USD (18) | number (18) | >= (14), > (4) | 150 |
| `minimum_qualifying_profit_days` | 18 | 2 | trading_days (8), days (5), unknown (5) | number (13), null (5) | >= (8), EQ (5), UNKNOWN (5) | 5 |
| `payout_buffer_profit` | 18 | 2 | USD (8), DOLLAR_SYMBOL_ONLY (5), unknown (5) | number (13), null (5) | = (8), EQ (5), UNKNOWN (5) | 1100 |
| `payout_processing_business_days` | 18 | 1 | business_days (18) | object (18) | RANGE (18) | {"min":1,"max":3} |
| `payout_processor_fee` | 18 | 1 | USD (18) | number (18) | EQ (18) | 30 |
| `payout_request_min` | 18 | 2 | unknown (10), USD (8) | null (10), number (8) | UNKNOWN (10), >= (8) | 500 |
| `payout_cadence` | 17 | 1 | text (17) | string (17) | EQ (17) | daily |
| `payout_min_usd` | 17 | 1 | USD (17) | number (15), null (2) | GE (17) | 500 |
| `request_cancel_allowed` | 17 | 2 | enum (9), boolean (8) | null (9), boolean (8) | UNKNOWN (9), EQ (8) | false |
| `trader_profit_split_pct` | 17 | 1 | ratio (17) | number (17) | EQ (17) | 0.9 |
| `later_cycle_net_profit_positive` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | true |
| `payment_timing` | 16 | 1 | text (16) | null (12), string (4) | AS_STATED (16) | within 24 hours after processing |
| `payout_approval_timing` | 16 | 2 | enum (15), text (1) | null (15), string (1) | unknown (15), EQ (1) | instant_or_6_12_business_hours |
| `payout_payment_methods` | 16 | 1 | enum (16) | array (16) | AS_STATED (16) | ["Rise","Plane"] |
| `payout_receipt_timing` | 16 | 1 | text (16) | null (16) | UNKNOWN (16) | (null) |
| `post_payout_retained_balance` | 16 | 2 | enum (9), text (7) | null (16) | UNKNOWN (9), unknown (7) | (null) |
| `unresolved__payout__balance_deduction` | 16 | 1 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `unresolved__payout__fraction_denominator` | 16 | 1 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `first_10k_allowance_reset` | 15 | 1 | text (15) | null (15) | UNKNOWN (15) | (null) |
| `forced_withdrawal_right` | 15 | 1 | boolean (15) | boolean (15) | EQ (15) | true |
| `payout_balance_deduction_timing` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_count_increment` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_cycle` | 15 | 1 | text (15) | null (15) | UNKNOWN (15) | (null) |
| `payout_deduction_basis` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_denied_state` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_floor_lock_timing` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_pending_trading` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_post_request_buffer` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_profit_basis` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_qualifying_days` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_request_edit_cancel` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `payout_trading_vs_calendar_days` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `profit_split` | 15 | 1 | ratio (15) | string (15) | EQ (15) | 90pct_after_first_10k_at_100pct |
| `withdrawal_minimum` | 15 | 1 | USD (15) | number (15) | GE (15) | 1000 |
| `withdrawal_rail_bank_wire` | 15 | 1 | text (15) | string (15) | EQ (15) | 1_to_3_business_days |
| `withdrawal_rail_crypto` | 15 | 1 | text (15) | string (15) | EQ (15) | max_1_per_week_max_3000_up_to_14bd_5pct_fee |
| `withdrawal_request_method` | 15 | 1 | text (15) | string (15) | EQ (15) | email_funding_provider_same_day_mon_fri |
| `withdrawal_split_example` | 15 | 1 | text (15) | string (15) | EQ (15) | 90_10_on_4000_example |
| `withdrawal_threshold` | 15 | 1 | USD (15) | number (15) | GE (15) | 1500 |
| `atd_criteria` | 14 | 1 | USD (14) | string (14) | GE (14) | 250_and_30pct |
| `atd_need_not_be_consecutive` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `atd_required_per_cycle` | 14 | 1 | days (14) | string (11), number (3) | EQ (14) | 8_then_10 |
| `balance_deduction_timing` | 14 | 2 | enum (14) | string (14) | EQ (14) | AT_REQUEST |
| `cannot_withdraw_from_safety_net` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `live_elite_discretionary_promotion` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `live_elite_trigger_cumulative` | 14 | 1 | USD (14) | number (14) | EQ (14) | 25000 |
| `must_request_full_cycle_max_before_advancing` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `payout_buffer` | 14 | 2 | USD (9), enum (5) | null (9), number (5) | >= (5), UNKNOWN (5), AS_STATED (4) | 2000 |
| `payout_cycle_max_plan_page` | 14 | 1 | USD (14) | number (14) | EQ (14) | 3000 |
| `payout_cycle_minimum` | 14 | 1 | USD (14) | number (14) | EQ (14) | 100 |
| `payout_cycle_reset_event` | 14 | 2 | event (8), text (6) | string (14) | = (8), AS_STATED (6) | approved_payout |
| `payout_method_rise` | 14 | 1 | text (14) | string (14) | EQ (14) | rise_ach_or_crypto |
| `payout_window` | 14 | 2 | schedule (8), text (6) | string (14) | = (8), EQ (6) | any_day_when_eligible |
| `reward_approval_timing` | 14 | 1 | text (14) | string (14) | EQ (14) | approved_daily_mon_fri_from_3pm_et |
| `same_day_payout_approval` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `sim_lifetime_cap_across_reentries` | 14 | 1 | USD (14) | number (14) | EQ (14) | 150000 |
| `sim_payout_cap_per_trader` | 14 | 1 | USD (14) | number (14) | EQ (14) | 25000 |
| `sim_profit_split` | 14 | 1 | ratio (14) | string (14) | EQ (14) | up_to_100pct |
| `sim_rewards_processed_twice_weekly` | 14 | 1 | text (14) | string (14) | EQ (14) | mondays_and_wednesdays |
| `unresolved__payout__day_calendar` | 14 | 2 | enum (14) | null (14) | UNKNOWN (14) | (null) |
| `unresolved__payout__gross_request` | 14 | 2 | enum (14) | null (14) | UNKNOWN (14) | (null) |
| `unresolved__payout__later_cycle_start` | 14 | 2 | enum (14) | null (14) | UNKNOWN (14) | (null) |
| `unresolved__payout__payment_timing` | 14 | 2 | enum (14) | null (14) | UNKNOWN (14) | (null) |
| `unresolved__payout__receipt_timing` | 14 | 2 | enum (14) | null (14) | UNKNOWN (14) | (null) |
| `maximum_sim_payout_count` | 13 | 1 | count (8), enum (5) | number (8), null (5) | <= (8), UNKNOWN (5) | 5 |
| `cycle_goal_new_profit` | 12 | 1 | text (12) | null (12) | unknown (12) | (null) |
| `payout_buffer_usd` | 12 | 1 | USD (12) | number (10), null (2) | GE (12) | 2100 |
| `payout_cap` | 12 | 1 | USD (11), enum (1) | number (11), null (1) | <= (11), UNKNOWN (1) | 2000 |
| `payout_max_fourth_onward_rule` | 12 | 1 | text (12) | string (12) | AS_STATED (12) | from the fourth payout the requested amount must be less than 50% of t… |
| `payout_split` | 12 | 1 | ratio (12) | number (12) | EQ (12) | 0.9 |
| `unresolved__payout__floor_lock_event` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__payout__minimum_day_profit` | 12 | 1 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `account_deduction_trigger` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `closed_pro_buffer_trader_share` | 10 | 1 | ratio (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 0.5 |
| `consistency_reset_event` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `cycle_reset_event` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `dashboard_balance_refresh` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | 20:00–21:00 EST; not real time |
| `days_reset_event` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `delayed_payment_state` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `first_withdrawal_tax_form_required` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | true |
| `fixed_payout_window` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | false |
| `manual_review_scope` | 10 | 1 | array (5), unknown (5) | array (5), null (5) | EQ (5), UNKNOWN (5) | ["all Rithmic accounts","cancelled PRO","disabled PRO"] |
| `maximum_payout_count` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `minimum_remaining_balance` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `mll_payout_lock_event` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `net_profit_fee_basis` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `net_receipt_formula` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `payout_approval_time` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `payout_buffer_comparison` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | balance >= published buffer-zone balance |
| `payout_buffer_required` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | true |
| `payout_count_increment_event` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `payout_fixed_cap` | 10 | 1 | boolean (10) | boolean (10) | EQ (10) | false |
| `payout_gross_amount_formula` | 10 | 1 | text (5), unknown (5) | null (10) | unresolved (5), UNKNOWN (5) | (null) |
| `payout_minimum` | 10 | 2 | USD (10) | number (10) | >= (6), AS_STATED (4) | 500 |
| `paypal_extra_fee_possible` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | true |
| `pending_buffer_breach` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `pending_trading` | 10 | 2 | text (10) | string (10) | AS_STATED (10) | trader can resume trading immediately while payout is pending approval |
| `per_cycle_cap` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `pro_payout_day_one` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | true |
| `pro_split` | 10 | 1 | ratio (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 0.8 |
| `pro_to_wallet_firm_share` | 10 | 1 | ratio (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 0.2 |
| `qualifying_day_minimum` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `request_cancellable` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `request_requires_flat` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | true |
| `request_requires_no_working_orders` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | true |
| `retry_state` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `subsequent_cycle_start` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `timezone_dst` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `trading_day_calendar` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `unresolved__payout__buffer_amount` | 10 | 2 | enum (10) | null (10) | UNKNOWN (10) | (null) |
| `us_bank_receipt_possible_delay` | 10 | 1 | business_days (5), unknown (5) | array (5), null (5) | EQ (5), UNKNOWN (5) | [1,2] |
| `wallet_approval_time_max` | 10 | 1 | business_hours (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 12 |
| `wallet_fee_above_threshold` | 10 | 1 | DOLLAR_SYMBOL_ONLY (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 0 |
| `wallet_fee_deduction_event` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | at wallet request |
| `wallet_fee_low_request` | 10 | 1 | DOLLAR_SYMBOL_ONLY (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 50 |
| `wallet_fee_threshold` | 10 | 1 | DOLLAR_SYMBOL_ONLY (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 250 |
| `wise_paypal_processing_max` | 10 | 1 | business_hours (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 12 |
| `approval_trigger` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `balance_deduction_trigger` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `buffer_formula` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `calendar_day_definition` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `consistency_denominator` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `consistency_numerator` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `consistency_reset_trigger` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `count_increment_trigger` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `cycle_cap` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `cycle_profit_reset_trigger` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `delayed_payment` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `disbursement_trigger` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `first_payout_qualifying_days_exempt` | 9 | 1 | enum (5), boolean (4) | null (5), boolean (4) | UNKNOWN (5), EQ (4) | true |
| `fixed_fee` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `floor_lock_trigger` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `later_cycle_start` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `net_receipt` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `payout_minimum_gross` | 9 | 1 | enum (5), USD (4) | null (5), number (4) | UNKNOWN (5), >= (4) | 125 |
| `payout_minimum_net` | 9 | 1 | enum (5), USD (4) | null (5), number (4) | UNKNOWN (5), >= (4) | 100 |
| `payout_tiers` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `payout_trader_share` | 9 | 1 | enum (5), ratio (4) | null (5), number (4) | UNKNOWN (5), EQ (4) | 0.8 |
| `pending_buffer_loss_consequence` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `percentage_cap_denominator` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `previous_cycle_profit_withdrawable` | 9 | 1 | boolean (9) | boolean (9) | EQ (9) | false |
| `profit_after_commission` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `reapplication` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `receipt_trigger` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `request_timezone` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `request_window` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `trader_profit_split` | 9 | 2 | ratio (9) | number (9) | EQ (5), AS_STATED (4) | 0.9 |
| `trading_day_definition` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `variable_fee` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `winning_days_reset_trigger` | 9 | 1 | enum (9) | null (5), string (4) | UNKNOWN (5), EQ (4) | payout_request |
| `approval_to_deduction` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | Once payout status is APPROVED, funds are immediately withdrawn from t… |
| `buffer_amount` | 8 | 1 | USD (8) | number (8) | >= (8) | 2100 |
| `buffer_balance_threshold` | 8 | 1 | USD (8) | number (8) | >= (8) | 52100 |
| `consistency_cycle_reset` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__047` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__048` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__049` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__050` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__051` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__052` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__053` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__054` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__055` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__056` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__057` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__058` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__059` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__060` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__061` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__062` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__063` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__064` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__065` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__066` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__067` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__068` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__069` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__070` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__071` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__072` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__073` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__074` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__075` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__076` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `first_payout_request_max` | 8 | 1 | USD (8) | number (8) | <= (8) | 1000 |
| `minimum_balance_for_500_request` | 8 | 1 | USD (8) | number (8) | >= (8) | 26600 |
| `minimum_balance_for_first_max_request` | 8 | 1 | USD (8) | number (8) | >= (8) | 27100 |
| `minimum_balance_for_subsequent_max_request` | 8 | 1 | USD (8) | number (8) | >= (8) | 27600 |
| `minimum_balance_required` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | false |
| `minimum_trading_days` | 8 | 2 | days (8) | null (4), number (4) | AS_STATED (4), >= (4) | 0 |
| `payout_count_increment_anchor` | 8 | 1 | enum (8) | string (8) | AS_STATED (8) | sequential approved payout |
| `payout_cycle_min_profit` | 8 | 1 | USD (8) | number (8) | >= (8) | 250 |
| `payout_disbursement_max` | 8 | 1 | business_days (8) | number (8) | <= (8) | 2 |
| `payout_fraction_of_total_profit` | 8 | 1 | ratio (8) | number (8) | <= (8) | 0.5 |
| `payout_request_edit_or_cancel` | 8 | 1 | boolean (8) | boolean (8) | = (8) | false |
| `per_request_cap_by_payout_count` | 8 | 1 | USD (8) | object (8) | <= (8) | {"1":1500,"2":2000,"3":2500} |
| `processing_time_outside_business_hours` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | Requests submitted outside normal business hours (Mon-Fri 8:00 a.m.-5:… |
| `request_amount_rule` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | up to 2× cycle profit |
| `separate_min_trading_days` | 8 | 1 | trading_days (8) | null (8) | unknown (8) | (null) |
| `separate_qualifying_profit_days` | 8 | 1 | days (8) | null (8) | unknown (8) | (null) |
| `sim_payout_count_limit` | 8 | 1 | payouts (8) | null (8) | <= (8) | (null) |
| `subsequent_payout_request_max` | 8 | 1 | USD (8) | number (8) | <= (8) | 1500 |
| `denied_cancelled_request_state` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `payout_count_increment_step` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `payout_cycle_reset` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `pending_request_trading` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `profit_split_tiers` | 7 | 1 | text (7) | object (7) | EQ (7) | {"basis": "single_withdrawal_size_not_accumulated", "TCP": {"25K": {"b… |
| `withdrawal_basis` | 7 | 1 | text (7) | string (7) | EQ (7) | profits_only_positive_performance |
| `withdrawal_fees` | 7 | 1 | text (7) | object (7) | EQ (7) | {"Rise_non_US": "$50 per withdrawal", "Rise_US": "1.5%", "Deel": "$50 … |
| `withdrawal_methods` | 7 | 1 | text (7) | array (7) | EQ (7) | ["Rise", "Deel", "Bayzat (on request, subject to approval)", "Direct c… |
| `withdrawal_minimum_net` | 7 | 1 | USD (7) | number (7) | GTE (7) | 100 |
| `withdrawal_request_deadline` | 7 | 1 | text (7) | string (7) | EQ (7) | email_by_2pm_CT_prior_friday |
| `withdrawal_restricted_regions` | 7 | 1 | text (7) | array (7) | EQ (7) | ["Iowa", "Minnesota", "South Carolina", "Guam", "Puerto Rico", "US Vir… |
| `withdrawal_schedule` | 7 | 1 | text (7) | string (7) | EQ (7) | weekly_wednesdays |
| `approval_time_business_days` | 6 | 1 | business_days (6) | object (6) | RANGE (6) | {"min":1,"max":3} |
| `approval_timing` | 6 | 1 | text (6) | null (6) | AS_STATED (6) | (null) |
| `claim_time_limit` | 6 | 1 | calendar_days (6) | number (6) | within (6) | 7 |
| `copy_connection_disabled_pending` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `disbursement_timing` | 6 | 1 | text (6) | null (6) | AS_STATED (6) | (null) |
| `invoice_confirmation_required` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `lifetime_payout_cap` | 6 | 1 | USD (6) | number (6) | <= (6) | 200000 |
| `minimum_trades_per_qualifying_day` | 6 | 1 | trades (6) | number (6) | >= (6) | 1 |
| `mll_after_payout` | 6 | 1 | USD (6) | number (6) | EQ (6) | 0 |
| `new_profit_min_fraction_of_request` | 6 | 1 | ratio (6) | number (6) | >= (6) | 0.5 |
| `payout_cap_consistency` | 6 | 1 | USD (6) | number (6) | <= (6) | 3000 |
| `payout_cap_doubled_with_dll` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `payout_cap_standard` | 6 | 1 | USD (6) | number (6) | <= (6) | 2000 |
| `payout_consistency_resets` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `payout_currency_and_methods` | 6 | 1 | enum (6) | object (6) | AS_STATED (6) | {"currency":"USD","methods":["Wise","Revolut bank wire","Visa Direct",… |
| `payout_fraction_of_profit` | 6 | 1 | ratio (6) | number (6) | <= (6) | 0.5 |
| `payout_max_per_cycle_usd` | 6 | 1 | USD (6) | null (6) | LE (6) | (null) |
| `payout_net_profit_since_previous` | 6 | 1 | USD (6) | number (6) | >= (6) | 0.01 |
| `payout_path_consistency_days` | 6 | 1 | days (6) | number (6) | >= (6) | 3 |
| `payout_path_standard_days` | 6 | 1 | days (6) | number (6) | >= (6) | 5 |
| `payout_positive_profit_required` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `payout_request_day_counts_next_cycle` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `payout_request_pct` | 6 | 1 | ratio (6) | number (6) | <= (6) | 0.5 |
| `positions_closed_on_request` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `qualifying_day_basis` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | closed P&L at end of trading day |
| `qualifying_day_lock_time` | 6 | 1 | text (6) | string (6) | at (6) | 16:00 CT |
| `receipt_timing` | 6 | 1 | text (6) | null (6) | AS_STATED (6) | (null) |
| `unresolved__payout__consistency_reset` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__payout__request_eligibility` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `consistency` | 5 | 1 | enum (5) | null (5) | UNKNOWN (5) | (null) |
| `min_net_profit_since_last_payout_usd` | 5 | 1 | USD (5) | number (5) | GE (5) | 500 |
| `mll_after_first_payout_usd` | 5 | 1 | USD (5) | number (5) | EQ (5) | 100 |
| `payout_account_name_match_required` | 5 | 1 | boolean (5) | boolean (5) | = (5) | true |
| `payout_eligible_profit_types` | 5 | 1 | array (5) | array (5) | AS_STATED (5) | ["trading profits","affiliate profits"] |
| `payout_llc_methods` | 5 | 1 | text (5) | string (5) | AS_STATED (5) | Wise (to a Wise account or from Wise to any US or international bank a… |
| `payout_max_per_request_usd` | 5 | 1 | USD (5) | number (3), null (2) | LE (5) | 1000 |
| `payout_name_mismatch_consequence` | 5 | 1 | text (5) | string (5) | AS_STATED (5) | Plaid: connection refused and payout not processed; Wise or PayPal: pa… |
| `qualifying_days_per_cycle` | 5 | 1 | days (5) | number (5) | GE (5) | 2 |
| `wallet_withdrawal_fee` | 5 | 1 | string (5) | string (5) | EQ (5) | $50 if <=$250, waived if >$250 |
| `current_max_payout_level` | 4 | 1 | payouts (4) | number (4) | AS_STATED (4) | 5 |
| `days_reset_after_payout` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | true |
| `ft_consistency_pct` | 4 | 1 | text (4) | string (4) | EQ (4) | 20% first payout / 25% second / 30% third onwards |
| `ft_cycle_new_profit_usd` | 4 | 1 | USD (4) | number (4) | >= (4) | 1000 |
| `ft_first_payout_goal_usd` | 4 | 1 | USD (4) | number (4) | >= (4) | 1500 |
| `ft_payout_floor_rule` | 4 | 1 | text (4) | string (4) | AS_STATED (4) | a payout may not bring the balance to or below the drawdown threshold |
| `ft_payout_max_first_three_usd` | 4 | 1 | USD (4) | number (4) | <= (4) | 1000 |
| `ft_payout_max_fourth_onward_usd` | 4 | 1 | USD (4) | number (4) | <= (4) | 1250 |
| `ft_same_day_processing` | 4 | 1 | text (4) | string (4) | EQ (4) | requests submitted before 12:01 pm CT Monday-Friday are ordinarily pro… |
| `minimum_balance_for_payout` | 4 | 1 | USD (4) | number (4) | >= (4) | 53000 |
| `mom_consistency_pct` | 4 | 1 | ratio (4) | number (4) | <= (4) | 0.35 |
| `mom_cycle_goal_usd` | 4 | 1 | USD (4) | number (4) | >= (4) | 1000 |
| `mom_day_threshold_usd` | 4 | 1 | USD (4) | number (4) | >= (4) | 100 |
| `mom_min_balance_usd` | 4 | 1 | USD (4) | number (4) | >= (4) | 26500 |
| `mom_min_request_usd` | 4 | 1 | USD (4) | number (4) | >= (4) | 500 |
| `mom_payout_caps_usd` | 4 | 1 | USD (4) | object (4) | <= (4) | {"first":1000,"second":1000,"third":1000,"fourth_onwards":1000} |
| `mom_qualifying_days` | 4 | 1 | text (4) | string (4) | EQ (4) | 5 qualifying profitable days per payout cycle; days need not be consec… |
| `mom_same_day_payout_processing` | 4 | 1 | text (4) | string (4) | AS_STATED (4) | payout requests on Momentum accounts are processed the same day (FAQ: … |
| `mom_str_usd` | 4 | 1 | USD (4) | number (4) | >= (4) | 1000 |
| `payout_cap_cycles_1_3` | 4 | 1 | USD (4) | number (4) | AS_STATED (4) | 1000 |
| `payout_cap_cycles_4_5` | 4 | 1 | USD (4) | number (4) | AS_STATED (4) | 1000 |
| `per_request_cap_payout_4_plus` | 4 | 1 | USD (4) | number (4) | EQ (4) | 3000 |
| `profit_goal_by_payout` | 4 | 1 | USD (4) | object (4) | >= (4) | {"1":3000,"2_plus":2000} |
| `profit_goal_first` | 4 | 1 | USD (4) | number (4) | AS_STATED (4) | 1500 |
| `profit_goal_subsequent` | 4 | 1 | USD (4) | number (4) | AS_STATED (4) | 1250 |
| `unresolved__payout__new_cycle_profit` | 4 | 1 | enum (4) | null (4) | UNKNOWN (4) | (null) |
| `unresolved__payout__request_window` | 4 | 1 | enum (4) | null (4) | UNKNOWN (4) | (null) |
| `dtf_first_payout_atd` | 3 | 1 | days (3) | number (3) | GE (3) | 5 |
| `payout_max_sim_funded_per_user_usd` | 3 | 1 | USD (3) | number (3) | LE (3) | 100000 |
| `pre_buffer_withdrawal_pct` | 3 | 1 | ratio (3) | number (3) | LE (3) | 0.6 |
| `fasttrack_consistency_at_reward` | 2 | 1 | text (2) | string (2) | EQ (2) | best_day_le_30pct_of_total_profit |
| `fasttrack_reward_cycle_amounts` | 2 | 1 | USD (2) | object (2) | EQ (2) | {"cycle_1":"100-500","cycle_2":"100-750","cycle_3":"100-1000","cap":22… |
| `method` | 2 | 1 | enum (2) | string (2) | = (2) | Plaid bank transfer |
| `payout_cycle_max_50k_scaling` | 2 | 1 | USD (2) | string (2) | EQ (2) | 100_to_1250_cycle1_toward_2000_later |
| `crypto_options` | 1 | 1 | enum (1) | array (1) | = (1) | ["BTC","ETH","LTC","USDT","USDC"] |
| `dtf_10k_cycle_max` | 1 | 1 | USD (1) | number (1) | EQ (1) | 1200 |
| `legacy_cohort_first_10k_trader_split` | 1 | 1 | ratio (1) | number (1) | EQ (1) | 1 |
| `payee` | 1 | 1 | enum (1) | string (1) | = (1) | Registered business |

### Stage `EVALUATION` - 3,558 records, 314 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `profit_target` | 134 | 10 | USD (129), DOLLAR_SYMBOL_ONLY (5) | number (131), null (3) | EQ (63), GE (31), >= (30) | 1500 |
| `evaluation_steps` | 69 | 6 | count (60), enum (9) | number (60), null (9) | EQ (60), UNKNOWN (9) | 1 |
| `minimum_trading_days` | 58 | 3 | days (42), distinct_session_count (16) | null (38), number (20) | >= (20), GE (16), = (16) | 3 |
| `initial_mll_balance` | 45 | 5 | USD (40), DOLLAR_SYMBOL_ONLY (5) | number (45) | EQ (37), = (8) | 48000 |
| `min_trading_days` | 44 | 5 | days (39), enum (5) | number (26), null (18) | >= (15), UNKNOWN (10), GE (10) | 0 |
| `evaluation_time_limit` | 41 | 4 | enum (16), text (15), days (10) | string (31), null (10) | EQ (31), AS_STATED (10) | NO_FIXED_PASS_DEADLINE |
| `consistency_formula` | 37 | 3 | text (21), enum (16) | string (37) | = (16), AS_STATED (16), EQ (5) | largest_single_day_profit / account_profit |
| `min_trading_days_eval` | 36 | 3 | days (36) | number (32), null (4) | GE (25), EQ (11) | 0 |
| `max_drawdown_amount` | 34 | 2 | USD (34) | number (34) | EQ (34) | 2000 |
| `minimum_holding_time` | 34 | 3 | text (20), enum (9), unknown (5) | null (34) | unknown (20), UNKNOWN (14) | (null) |
| `profit_target_usd` | 34 | 2 | USD (34) | number (34) | GE (18), >= (16) | 1000 |
| `daily_loss_limit` | 33 | 4 | text (15), USD (13), boolean (5) | null (15), number (7), object (6) | UNKNOWN (15), EQ (12), AS_STATED (6) | 550 |
| `max_contracts` | 33 | 4 | contracts (21), count (7), enum (5) | number (16), string (12), null (5) | EQ (12), <= (9), LTE (7) | 5 micro contracts |
| `max_contracts_mini` | 32 | 3 | contracts (32) | number (32) | <= (32) | 5 |
| `news_trading_allowed` | 32 | 4 | boolean (32) | boolean (32) | EQ (32) | true |
| `unresolved__evaluation__minimum_holding_time` | 32 | 3 | enum (32) | null (32) | UNKNOWN (32) | (null) |
| `unresolved__evaluation__qualifying_profit_day` | 32 | 3 | enum (32) | null (32) | UNKNOWN (32) | (null) |
| `drawdown_type` | 29 | 3 | text (21), type (8) | string (29) | EQ (21), = (8) | live_trailing_unrealized |
| `initial_floor` | 29 | 2 | text (20), enum (9) | null (29) | unknown (20), UNKNOWN (9) | (null) |
| `max_micro_contracts` | 29 | 2 | contracts (29) | number (29) | <= (24), EQ (5) | 20 |
| `pass_timing` | 26 | 2 | text (26) | string (26) | AS_STATED (26) | assessed after end of trading day |
| `unresolved__evaluation__commission_included` | 26 | 2 | enum (26) | null (26) | UNKNOWN (26) | (null) |
| `unresolved__evaluation__flat_time` | 26 | 2 | enum (26) | null (26) | UNKNOWN (26) | (null) |
| `unresolved__evaluation__news_product_exceptions` | 26 | 2 | enum (20), contracts (6) | null (20), object (6) | UNKNOWN (20), AS_STATED (6) | {"minis_no_new_opening_in_window":["ES","RTY","YM","NQ","NKD","GC","SI… |
| `unresolved__evaluation__news_window` | 26 | 2 | enum (20), text (6) | null (20), object (6) | UNKNOWN (20), within (6) | {"window_total_minutes":10,"minutes_before_release":5,"minutes_after_r… |
| `unresolved__evaluation__overnight_positions` | 26 | 2 | enum (26) | null (26) | UNKNOWN (26) | (null) |
| `unresolved__evaluation__weekend_positions` | 26 | 2 | enum (26) | null (26) | UNKNOWN (26) | (null) |
| `qualifying_profit_day` | 25 | 2 | text (16), enum (9) | null (25) | unknown (16), UNKNOWN (9) | (null) |
| `max_mini_contracts` | 24 | 1 | contracts (24) | number (24) | <= (24) | 2 |
| `reset_fee` | 23 | 2 | USD (23) | null (12), number (11) | EQ (11), unknown (8), UNKNOWN (4) | 50 |
| `consistency_cushion_formula` | 22 | 1 | enum (16), formula (6) | null (22) | = (16), UNKNOWN (6) | (null) |
| `consistency_max_best_day_ratio` | 22 | 2 | ratio (22) | number (22) | <= (22) | 0.4 |
| `consistency_rule` | 22 | 2 | text (22) | string (22) | GE (15), LT (7) | no_single_day_geq_30pct_of_total_pnl |
| `eval_inactivity` | 22 | 2 | enum (15), text (7) | null (22) | unknown (22) | (null) |
| `unresolved__evaluation__latest_completion` | 22 | 2 | enum (22) | null (22) | UNKNOWN (22) | (null) |
| `consistency_exceeded_consequence` | 21 | 2 | enum (16), text (5) | string (21) | = (16), EQ (5) | continue until compliant |
| `trading_day_definition` | 21 | 2 | text (21) | string (21) | EQ (21) | 5pm_ct_to_315pm_ct_next_day |
| `daily_loss_limit_amount` | 20 | 2 | USD (14), text (6) | string (11), null (6), number (3) | EQ (14), unknown (6) | NONE |
| `dll_amount_verified_card` | 20 | 1 | USD_PRESUMED_UNCONFIRMED (20) | number (8), null (8), object (4) | EQ (12), N/A (8) | {"LUCID_FLEX_25K_DLL_ON_CONS40":600,"LUCID_FLEX_50K_DLL_ON_CONS40":120… |
| `eval_drawdown_locks` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | false |
| `inactivity_rule` | 20 | 1 | text (20) | string (20) | AS_STATED (20) | at least 1 trade per week (Mon–Fri) |
| `touch_or_below` | 20 | 1 | text (20) | null (20) | unknown (20) | (null) |
| `dll_enabled` | 19 | 2 | boolean (19) | boolean (19) | EQ (19) | false |
| `eval_steps` | 19 | 2 | count (12), text (7) | number (12), null (7) | EQ (12), unknown (7) | 1 |
| `consistency_rule_eval_pct` | 18 | 1 | ratio (18) | null (9), number (9) | EQ (9), LE (9) | 0.5 |
| `consistency_rule_eval` | 17 | 2 | text (9), boolean (8) | string (9), boolean (8) | EQ (17) | false |
| `activation_fee_exists` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | true |
| `advertised_fastest_pass_days` | 16 | 1 | days (16) | number (16) | EQ (16) | 2 |
| `breached_reset_window` | 16 | 1 | calendar_days (16) | number (16) | < (16) | 30 |
| `consistency_cushion_example` | 16 | 1 | USD (16) | number (16) | = (16) | 650 |
| `consistency_cushion_exists` | 16 | 1 | boolean (16) | boolean (8), null (8) | EQ (8), UNKNOWN (8) | true |
| `earliest_advertised_pass` | 16 | 1 | days (16) | number (16) | = (16) | 2 |
| `evaluation_consistency` | 16 | 1 | ratio (16) | null (16) | unresolved (16) | (null) |
| `evaluation_news_scope` | 16 | 1 | enum (16) | null (16) | = (16) | (null) |
| `evaluation_reset_available` | 16 | 1 | boolean (16) | boolean (16) | = (16) | true |
| `maximum_days_to_pass` | 16 | 1 | days (16) | null (16) | = (16) | (null) |
| `minimum_qualifying_profit_days` | 16 | 1 | days (16) | null (16) | = (16) | (null) |
| `qualifying_winning_days` | 16 | 1 | days (16) | null (16) | GE (16) | (null) |
| `reset_retains_configuration` | 16 | 1 | boolean (16) | null (16) | = (16) | (null) |
| `upgrade_update_minutes` | 16 | 1 | minutes (16) | string (16) | RANGE (16) | 5–30 |
| `commission_eval` | 15 | 1 | USD (15) | number (15) | EQ (15) | 2.5 |
| `consistency_denominator` | 15 | 2 | enum (9), text (6) | null (15) | UNKNOWN (15) | (null) |
| `drawdown_type_eval` | 15 | 1 | text (15) | string (10), null (5) | EQ (11), unresolved (4) | EOD_TRAILING |
| `eval_qualifying_day` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `evaluation_environment` | 15 | 1 | text (15) | string (15) | EQ (15) | simulated_accounts |
| `max_contracts_mini_eval` | 15 | 1 | contracts (15) | number (14), null (1) | LE (14), EQ (1) | 2 |
| `max_loss_limit_eval_usd` | 15 | 1 | USD (15) | number (14), null (1) | UNKNOWN (14), EQ (1) | 1000 |
| `max_position_micros` | 15 | 1 | contracts (15) | number (15) | EQ (15) | 80 |
| `max_position_minis` | 15 | 1 | contracts (15) | number (15) | EQ (15) | 8 |
| `max_position_size` | 15 | 1 | count (15) | number (15) | LE (15) | 3 |
| `news_trading_evaluation` | 15 | 1 | text (15) | string (15) | EQ (15) | evaluation_traders_exempt_from_flat_rule |
| `overnight_weekend` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `pass_condition` | 15 | 2 | enum (9), text (6) | null (9), string (6) | UNKNOWN (9), AS_STATED (6) | balance exceeds initial capital by target with all positions closed; a… |
| `permitted_products` | 15 | 1 | symbols (15) | array (15) | EQ (15) | ["6A","6B","6C","6E","6N","6J","6S","CL","EMD","ES","GC","GE","GF","HE… |
| `permitted_times_rule` | 15 | 1 | text (15) | string (15) | EQ (15) | flat_by_315pm_ct_no_opens_315_5pm |
| `review_submission` | 15 | 1 | text (15) | string (15) | EQ (15) | email_support_after_objectives_review_le_3_days |
| `trailing_drawdown_amount` | 15 | 1 | USD (15) | number (15) | EQ (15) | 1500 |
| `trailing_drawdown_includes_fees` | 15 | 1 | boolean (15) | boolean (15) | EQ (15) | true |
| `trailing_drawdown_mechanics` | 15 | 1 | text (15) | string (15) | EQ (15) | trails_up_locks_at_start_breach_on_touch |
| `trailing_drawdown_monitor` | 15 | 1 | text (15) | string (15) | EQ (15) | rithmic_rtrader_pro_auto_liquidate_threshold |
| `automated_trading_allowed` | 14 | 2 | boolean (14) | boolean (14) | EQ (14) | false |
| `consistency_cycle` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `daily_loss_limit_trigger_consequence` | 14 | 1 | text (14) | null (14) | unknown (14) | (null) |
| `dll_type` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `evaluation_phases` | 14 | 1 | phases (14) | number (11), null (3) | EQ (11), UNKNOWN (3) | 1 |
| `floating_drawdown` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `max_contracts_micro_eval` | 14 | 1 | contracts (14) | number (14) | LE (14) | 20 |
| `micro_scaling` | 14 | 1 | text (14) | string (14) | EQ (14) | 1_mini_eq_10_micros |
| `overnight_hold_allowed` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | false |
| `pass_observation_time` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `scaling_plan` | 14 | 1 | text (14) | null (14) | unknown (14) | (null) |
| `tier1_news_eval` | 14 | 1 | text (14) | string (14) | EQ (14) | allowed |
| `weekend_holding` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `daily_loss_limit_exists` | 13 | 1 | boolean (13) | boolean (12), null (1) | EQ (13) | false |
| `eod_trail_basis` | 13 | 2 | enum (8), text (5) | string (13) | = (8), EQ (5) | session closing balance; unrealized P&L does not set trail |
| `flat_time_ct` | 13 | 2 | time_ct (6), time (4), text (3) | null (9), string (4) | UNKNOWN (6), EQ (4), unresolved (3) | 15:10 CT |
| `access_window_days` | 12 | 1 | days (12) | number (12) | EQ (12) | 30 |
| `consistency_to_pass` | 12 | 1 | text (12) | null (12) | EQ (12) | (null) |
| `dll_breach_effect` | 12 | 3 | unknown (5), event (4), text (3) | string (7), null (5) | UNKNOWN (5), = (4), AS_STATED (3) | HARD: evaluation unsuccessful |
| `max_drawdown_usd` | 12 | 1 | USD (12) | number (12) | EQ (12) | 1000 |
| `micro_conversion` | 12 | 1 | text (12) | string (12) | EQ (12) | 1 standard contract = 10 micro contracts; both may be traded simultane… |
| `min_trading_days_to_pass` | 12 | 1 | text (12) | string (12) | EQ (12) | none |
| `pass_review` | 12 | 1 | text (12) | string (12) | EQ (12) | account automatically submitted for review after reaching the profit t… |
| `reset_fee_usd` | 12 | 1 | USD (12) | number (12) | EQ (12) | 78 |
| `time_limit` | 12 | 2 | text (12) | null (12) | none (7), EQ (5) | (null) |
| `unresolved__evaluation__inactivity` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `current_highest_volume_contract_required` | 11 | 1 | boolean (11) | boolean (11) | EQ (11) | true |
| `daily_loss_limit_usd` | 11 | 2 | USD (11) | number (11) | EQ (6), GE (5) | 400 |
| `eval_weekly_trade_required` | 11 | 1 | boolean (11) | boolean (11) | EQ (11) | false |
| `flatten_before_close_minutes` | 11 | 1 | minutes (11) | number (10), string (1) | EQ (11) | 1 |
| `max_contracts_eval` | 11 | 2 | contracts (11) | number (11) | <= (8), LE (3) | 4 |
| `one_day_to_pass_addon` | 11 | 1 | boolean (11) | boolean (11) | EQ (11) | true |
| `unlimited_balance_resets` | 10 | 1 | text (10) | string (10) | AS_STATED (10) | unlimited |
| `commission_treatment` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `consistency_challenge` | 9 | 1 | enum (5), ratio (4) | null (5), number (4) | UNKNOWN (5), <= (4) | 0.4 |
| `consistency_numerator` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `daily_drawdown` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `dll_amount` | 9 | 2 | USD (9) | null (5), number (4) | N/A (4), EQ (4), unresolved (1) | 1250 |
| `dll_trigger_consequence` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `drawdown_basis` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `earliest_pass` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `eod_trailing_drawdown` | 9 | 1 | USD (9) | number (9) | EQ (9) | 1500 |
| `eval_reset_unlimited` | 9 | 1 | boolean (9) | boolean (9) | EQ (9) | true |
| `floor_locks_at_starting_balance` | 9 | 1 | boolean (9) | boolean (9) | EQ (9) | false |
| `hedging_prohibited` | 9 | 2 | boolean (9) | boolean (9) | EQ (9) | true |
| `mini_micro_conversion` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `news_instrument_exceptions` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `news_window` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `overnight_holding` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `session_calendar` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `time_zone_dst` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `trailing_update_time` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `unrealized_pnl_treatment` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `access_period_days` | 8 | 1 | days (8) | number (8) | EQ (8) | 30 |
| `account_environment` | 8 | 1 | type (8) | string (8) | = (8) | simulated |
| `breach_balance_boundary` | 8 | 1 | balance (8) | string (8) | <= (8) | MLL |
| `consistency_during_evaluation` | 8 | 1 | text (8) | null (8) | unknown (8) | (null) |
| `consistency_fraction` | 8 | 1 | ratio (8) | number (8) | LE (8) | 0.4 |
| `coverage_gap__016` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__017` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__018` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__019` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__020` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__021` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__022` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__023` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__024` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__025` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__026` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__027` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__028` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__029` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__030` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__031` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__032` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__033` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__034` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__035` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__036` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__037` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `daily_loss_limit_eval` | 8 | 1 | USD (4), text (4) | number (4), null (4) | EQ (8) | 500 |
| `dll_selected` | 8 | 1 | boolean (8) | boolean (8) | = (8) | true |
| `drawdown_type_and_basis` | 8 | 1 | text (8) | null (8) | unknown (8) | (null) |
| `earliest_advertised_pass_days` | 8 | 1 | days (8) | number (8) | = (8) | 1 |
| `earliest_pass_trading_days` | 8 | 1 | trading_days (8) | number (8) | >= (8) | 1 |
| `eod_breach_monitoring_basis` | 8 | 1 | enum (8) | null (8) | = (8) | (null) |
| `eval_expiry_time_et` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | 6:00 PM ET on Day 30 |
| `evaluation_deadline` | 8 | 1 | days (8) | null (8) | N/A (8) | (null) |
| `evaluation_trail_stop_by_platform` | 8 | 1 | enum (8) | object (8) | AS_STATED (8) | {"Rithmic":"threshold stops at target-profit balance","WealthCharts":"… |
| `flat_time_et` | 8 | 1 | text (8) | string (8) | EQ (8) | 4:59 PM ET |
| `initial_trail_balance` | 8 | 1 | USD (8) | number (8) | > (8) | 26100 |
| `locked_mll_balance` | 8 | 1 | USD (8) | number (8) | = (8) | 25100 |
| `max_drawdown` | 8 | 1 | USD (8) | number (8) | EQ (8) | 1000 |
| `max_loss_amount` | 8 | 1 | USD (8) | number (8) | = (8) | 1000 |
| `mini_micro_ratio` | 8 | 1 | text (8) | null (8) | unknown (8) | (null) |
| `number_of_steps` | 8 | 1 | text (8) | null (8) | unknown (8) | (null) |
| `pa_activation_window_days` | 8 | 1 | days (8) | number (8) | <= (8) | 7 |
| `pass_determination_and_review` | 8 | 1 | text (8) | null (8) | unknown (8) | (null) |
| `purchase_fee` | 8 | 1 | USD (8) | null (8) | unknown (8) | (null) |
| `rebilling` | 8 | 1 | boolean (8) | boolean (8) | = (8) | false |
| `reset_restores` | 8 | 1 | event (8) | string (8) | = (8) | starting_balance_and_risk_parameters |
| `separate_consistency_requirement` | 8 | 1 | ratio (8) | null (8) | N/A (8) | (null) |
| `starting_balance` | 8 | 1 | USD (8) | number (8) | = (8) | 25000 |
| `unrealized_and_commissions_in_drawdown` | 8 | 1 | text (8) | null (8) | unknown (8) | (null) |
| `approved_trading_times` | 7 | 1 | text (7) | object (7) | EQ (7) | {"session_start": "~5pm CT exchange open (asset/holiday dependent)", "… |
| `consistency_exceed_effect` | 7 | 1 | text (7) | string (7) | EQ (7) | not_a_fail_trade_more_until_below_30pct |
| `consistency_scope` | 7 | 1 | text (7) | string (7) | EQ (7) | evaluation_only |
| `dll_basis` | 7 | 1 | text (7) | string (7) | EQ (7) | pnl_incl_open_unrealized_closed_commissions_5pm_5pm_CT_resets_daily |
| `dll_breach` | 7 | 1 | text (7) | string (7) | TOUCH (7) | fail_if_pnl_ever_hits_limit_even_open |
| `drawdown_breach` | 7 | 1 | text (7) | string (7) | TOUCH_OR_BELOW (7) | fail_on_reach_or_dip_below_minimum_balance |
| `eod_floor_mechanics` | 7 | 1 | text (7) | string (7) | EQ (7) | floor_rises_1_per_1_profit_locks_at_starting_balance |
| `eod_processing_window` | 7 | 1 | text (7) | string (7) | EQ (7) | rithmic_4pm_5pm_CT_daily |
| `eval_drawdown_type` | 7 | 1 | text (7) | string (7) | EQ (7) | EOD |
| `eval_floating_dd` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `eval_max_duration` | 7 | 1 | text (7) | null (7) | UNKNOWN (7) | (null) |
| `eval_min_hold_time` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `ladder_exceed_eval_consequence` | 7 | 1 | text (7) | string (7) | EQ (7) | hard_fail_immediate_end_reset_required |
| `ladder_self_regulated_realtime` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | true |
| `max_drawdown_eod` | 7 | 1 | USD (7) | number (7) | EQ (7) | 1500 |
| `micro_contract_equivalence` | 7 | 1 | count (7) | object (7) | EQ (7) | {"micros_per_standard": 10, "symbols": ["MES", "MNQ", "MYM", "M2K", "M… |
| `min_profitable_days_derived` | 7 | 1 | days (7) | number (7) | GTE (7) | 4 |
| `news_trading` | 7 | 1 | text (7) | string (7) | EQ (7) | allowed_no_restrictions |
| `overnight_positions` | 7 | 1 | boolean (7) | string (7) | EQ (7) | prohibited |
| `pass_criteria` | 7 | 1 | text (7) | string (7) | EQ (7) | profit_target_plus_consistency_plus_all_risk_rules |
| `progression_ladder_tiers` | 7 | 1 | text (7) | array (7) | EQ (7) | [{"profit_usd": "0-1500", "max_contracts": 2}, {"profit_usd": "1501+",… |
| `tradable_assets` | 7 | 1 | text (7) | object (7) | EQ (7) | {"allowed": "all CME/CBOT/NYMEX/COMEX futures including micros", "proh… |
| `account_size_changeable` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `best_day_lock_time` | 6 | 1 | text (6) | string (6) | at (6) | 15:10 CT |
| `combine_profits_transfer` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `consistency_mechanics` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | best day closed P&L vs total profit; exceeding is not a breach, keep t… |
| `consistency_target_pct` | 6 | 1 | ratio (6) | number (6) | <= (6) | 0.55 |
| `drawdown_breach_boundary_eod` | 6 | 1 | text (6) | string (6) | EQ (6) | touch |
| `drawdown_eod_mechanics` | 6 | 1 | text (6) | string (6) | EQ (6) | moves only once a day at close on realised profit; breach -> account d… |
| `drawdown_trail_mechanics` | 6 | 1 | text (6) | string (6) | EQ (6) | follows current balance incl. open positions in real time; rises with … |
| `eval_drawdown_lock` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | locks permanently at initial simulated capital (until reset or new sub… |
| `flat_by_time_et` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | 4:10 p.m. ET or the relevant market close, whichever is sooner |
| `loss_resets_best_day` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `market_data_level1` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `max_loss_limit` | 6 | 1 | USD (6) | number (6) | EQ (6) | 2000 |
| `mll_lock_floor_basis` | 6 | 1 | text (6) | string (6) | EQ (6) | initial account balance |
| `news_trading_product_exceptions` | 6 | 1 | enum (6) | null (6) | AS_STATED (6) | (null) |
| `overnight_positions_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `trade_copier_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `unresolved__evaluation__balance_or_equity` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__evaluation__consistency_cycle` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__evaluation__consistency_numerator` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__evaluation__daily_loss_limit` | 6 | 1 | USD (6) | object (6) | AS_STATED (6) | {"dll_optional":true,"amount_if_selected_usd_by_size":{"50000":1000,"1… |
| `unresolved__evaluation__dll_fixed_or_scaled` | 6 | 1 | enum (6) | string (6) | EQ (6) | fixed |
| `unresolved__evaluation__earliest_completion` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__evaluation__evaluation_steps` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__evaluation__floating_drawdown` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__evaluation__high_water_reference` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__evaluation__pass_condition` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__evaluation__pass_timing` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `weekend_positions_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `auto_flat_time` | 5 | 1 | text (5) | string (5) | EQ (5) | 16:55 Eastern |
| `breach_observation_basis` | 5 | 1 | text (5) | string (5) | EQ (5) | realized and unrealized loss at any time |
| `carry_to_next_trading_day` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `commission_in_drawdown` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `consistency_pct` | 5 | 1 | ratio (5) | number (5) | < (5) | 0.5 |
| `consistency_required_profit` | 5 | 1 | text (5) | string (5) | EQ (5) | total net profit > 2 * highest profit day net P/L |
| `consistency_zero_denominator` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `daily_loss_limit_type` | 5 | 1 | text (5) | string (5) | EQ (5) | soft_pause |
| `drawdown_breach_boundary_static` | 5 | 1 | text (5) | string (5) | EQ (5) | close_at_or_below |
| `drawdown_measurement_object` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `drawdown_type_test` | 5 | 1 | text (5) | string (5) | EQ (5) | EOD_trailing |
| `early_product_close_breach` | 5 | 1 | text (5) | string (5) | EQ (5) | account liquidation if unable to exit before deadline |
| `express_cancel_effect` | 5 | 1 | text (5) | string (5) | EQ (5) | lose_offer_regular_eval_only |
| `express_eligibility` | 5 | 1 | text (5) | string (5) | EQ (5) | fta_termination_within_24h_same_size |
| `express_frequency_cap` | 5 | 1 | text (5) | string (5) | EQ (5) | max_2_per_30d_max_1_at_a_time |
| `holiday_close_breach` | 5 | 1 | text (5) | string (5) | EQ (5) | account liquidation |
| `inactivity_calendar_days` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `max_trailing_drawdown` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | number (5) | EQ (5) | 1500 |
| `minimum_profit_per_winning_day` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `mixed_mini_micro_exposure_formula` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `mll_breach_balance_comparison` | 5 | 1 | text (5) | string (5) | EQ (5) | equity <= current minimum account balance |
| `mll_lock_floor` | 5 | 1 | text (5) | string (5) | EQ (5) | original starting balance |
| `news_product_exceptions` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `news_trading_test` | 5 | 1 | boolean (5) | null (5) | UNKNOWN (5) | (null) |
| `pass_determination` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `trading_day_attribution` | 5 | 1 | text (5) | string (5) | EQ (5) | at or after18:00 Eastern counts next day |
| `trading_day_qualifier` | 5 | 1 | text (5) | string (5) | EQ (5) | at least one trade |
| `trading_hours` | 5 | 1 | string (5) | string (5) | EQ (5) | 18:00-17:00 Eastern |
| `unrealized_included` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `completion_window_access_period` | 4 | 1 | text (4) | null (4) | unknown (4) | (null) |
| `consistency` | 4 | 1 | ratio (4) | number (4) | <= (4) | 0.4 |
| `consistency_rule_applies` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | false |
| `copy_trading_allowed` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | true |
| `daily_loss_limit_option1` | 4 | 1 | USD (4) | null (4) | unknown (4) | (null) |
| `earliest_possible_pass` | 4 | 1 | trading days (4) | number (4) | potential (4) | 3 |
| `eod_threshold_update` | 4 | 1 | text (4) | null (4) | unresolved (4) | (null) |
| `evaluation_items_not_applicable` | 4 | 1 | enum (4) | null (4) | AS_STATED (4) | (null) |
| `ft_daily_loss_limit` | 4 | 1 | USD (4) | object (4) | AS_STATED (4) | {"option_1_trailing":"none","option_2_eod":"none"} |
| `ft_daily_loss_limit_persists` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | true |
| `ft_drawdown_usd` | 4 | 1 | USD (4) | number (4) | EQ (4) | 1000 |
| `ft_max_contracts` | 4 | 1 | contracts (4) | object (4) | AS_STATED (4) | {"option_1_trailing":3,"option_2_eod":2} |
| `ft_min_trading_days` | 4 | 1 | text (4) | string (4) | EQ (4) | none |
| `intraday_trailing_peak` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | true |
| `mom_access_window_days` | 4 | 1 | days (4) | number (4) | EQ (4) | 30 |
| `mom_daily_loss_limit` | 4 | 1 | USD (4) | object (4) | AS_STATED (4) | {"option_1_trailing":"none","option_2_eod":600} |
| `mom_drawdown_usd` | 4 | 1 | USD (4) | number (4) | EQ (4) | 1000 |
| `mom_max_contracts` | 4 | 1 | contracts (4) | object (4) | AS_STATED (4) | {"option_1_trailing":3,"option_2_eod":2} |
| `mom_min_trading_days` | 4 | 1 | text (4) | string (4) | EQ (4) | none |
| `weekend_hold_allowed` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | true |
| `daily_loss_limit_breach_effect` | 3 | 1 | text (3) | string (3) | EQ (3) | hard_breach_immediate_fail |
| `daily_loss_limit_breach_operator` | 3 | 1 | text (3) | string (3) | EQ (3) | touch |
| `dll_fixed_amount` | 3 | 1 | USD (3) | number (3) | >= loss triggers (3) | 1200 |
| `drawdown_breach_boundary_livetrail` | 3 | 1 | text (3) | string (3) | EQ (3) | touch_including_open_profit |
| `evaluation_fee_one_time_usd` | 3 | 1 | USD (3) | number (3) | EQ (3) | 140 |
| `max_loss_limit_static_usd` | 3 | 1 | USD (3) | number (3) | EQ (3) | 500 |
| `tradesheld_addon_dll` | 3 | 1 | boolean (3) | boolean (3) | EQ (3) | true |
| `fasttrack_consistency_to_qualify` | 2 | 1 | text (2) | string (2) | EQ (2) | best_day_le_40pct_of_total_profit |
| `fasttrack_eval_time_limit_days` | 2 | 1 | calendar_days (2) | number (2) | EQ (2) | 10 |
| `fasttrack_sunday_monday_same_day` | 2 | 1 | boolean (2) | boolean (2) | EQ (2) | true |
| `flat_time` | 2 | 1 | enum (2) | null (2) | UNKNOWN (2) | (null) |
| `inactivity_rule_days` | 2 | 1 | days (2) | number (2) | LE (2) | 7 |
| `maximum_completion_time` | 2 | 1 | enum (2) | null (2) | UNKNOWN (2) | (null) |
| `active_account_limit` | 1 | 1 | accounts (1) | number (1) | <= (1) | 10 |
| `automation_allowed_if_not_exploiting` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `collaborative_trading_prohibited` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `copy_trading_others_prohibited` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `gapped_illiquid_exploitation_prohibited` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `hft_allowed` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | false |
| `may_trade` | 1 | 1 | enum (1) | boolean (1) | = (1) | true |
| `order_stacking_manipulation_prohibited` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `passed_evaluations_subject_to_review` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `reserve_limit` | 1 | 1 | accounts (1) | number (1) | <= (1) | 5 |
| `reset_before_deletion` | 1 | 1 | days (1) | number (1) | < (1) | 30 |
| `shared_device_prohibited` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `slippage_bracket_exploitation_prohibited` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `temporary_commodity_restrictions_exist` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `tier1_news_events` | 1 | 1 | text (1) | string (1) | EQ (1) | FOMC Meetings, FOMC Minutes, Employment Report, CPI; EIA for energy; A… |
| `tier1_news_window` | 1 | 1 | text (1) | string (1) | EQ (1) | flat_2min_before_to_2min_after |
| `trading_hours_est` | 1 | 1 | text (1) | string (1) | EQ (1) | 18:00-16:10 |

### Stage `LIVE` - 2,692 records, 179 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `starting_balance` | 57 | 2 | USD (48), enum (9) | number (48), null (9) | = (48), UNKNOWN (9) | 1000 |
| `live_scaling_tier` | 56 | 1 | enum (56) | object (56) | = (56) | {"profit_min":0,"profit_max_literal":1999.99,"CME":{"minis":1,"micros"… |
| `live_starting_balance` | 49 | 4 | USD (24), enum (15), DOLLAR_SYMBOL_ONLY (5) | number (29), null (20) | = (24), unknown (15), EQ (5) | 0 |
| `bonus_day_qualification` | 48 | 1 | net after fees (48) | object (32), null (16) | >= (48) | {"trades_min":1,"absolute_net_pnl_min_usd":1} |
| `bonus_delivery` | 48 | 1 | enum (48) | string (32), null (16) | = (48) | Paid out; not credited to trading balance |
| `repeatable_bonus_days` | 48 | 1 | qualifying trading days (44), trading days (4) | number (32), null (16) | >= (48) | 20 |
| `auto_liquidation` | 44 | 1 | enum (44) | string (44) | = (44) | Optional; configure during onboarding |
| `bonus_trader_split` | 44 | 1 | ratio (44) | number (28), null (16) | = (44) | 0.9 |
| `consistency` | 44 | 1 | ratio (44) | null (44) | none (44) | (null) |
| `dll` | 44 | 1 | USD (44) | null (44) | none (44) | (null) |
| `drawdown_basis` | 44 | 1 | enum (44) | string (44) | = (44) | Highest session closing balance; EOD trailing |
| `headline_max_minis` | 44 | 1 | contracts (44) | number (44) | <= (44) | 2 |
| `hedging_consequence` | 44 | 1 | enum (44) | string (44) | = (44) | Permanent ban, including copytrader-caused hedging |
| `household_sim_trading` | 44 | 1 | enum (44) | boolean (44) | prohibited (44) | false |
| `initial_drawdown` | 44 | 1 | USD (44) | number (44) | = (44) | 1000 |
| `mll_lock_floor` | 44 | 1 | USD (44) | number (44) | = (44) | 100 |
| `payout_cadence` | 44 | 1 | enum (44) | string (44) | = (44) | Daily |
| `repeatable_bonus_gross` | 44 | 1 | USD (44) | number (28), null (16) | = (44) | 1000 |
| `repeatable_bonus_target` | 44 | 1 | USD (44) | number (28), null (16) | >= (44) | 2000 |
| `scaling_circumvention` | 44 | 1 | enum (44) | string (44) | = (44) | Repeated attempts may cause account review |
| `swing_trading` | 44 | 1 | enum (44) | boolean (44) | prohibited (44) | false |
| `payout_frequency` | 39 | 3 | text (30), enum (9) | string (30), null (9) | AS_STATED (30), UNKNOWN (9) | daily after buffer cleared; no payout cap |
| `unresolved__live__new_agreement` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `live_payout_minimum` | 34 | 3 | USD (24), unknown (10) | null (26), number (8) | = (16), UNKNOWN (10), >= (8) | 500 |
| `payout_minimum` | 33 | 2 | USD (24), enum (9) | null (33) | unresolved (24), UNKNOWN (9) | (null) |
| `position_scaling` | 33 | 2 | text (24), enum (9) | string (24), null (9) | AS_STATED (24), UNKNOWN (9) | 2 mini/20 micro below DD level; 4/40 above |
| `trader_split` | 30 | 2 | ratio (30) | number (30) | EQ (30) | 0.9 |
| `unresolved__live__payout_fee` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__live__reserve_review` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `live_mll_lock_balance` | 26 | 2 | USD (16), DOLLAR_SYMBOL_ONLY (5), unknown (5) | number (21), null (5) | = (16), EQ (5), UNKNOWN (5) | 100 |
| `live_payout_frequency` | 26 | 2 | enum (16), text (5), unknown (5) | string (21), null (5) | = (16), EQ (5), UNKNOWN (5) | daily |
| `live_new_agreement` | 25 | 2 | enum (15), unknown (10) | null (25) | unknown (15), UNKNOWN (10) | (null) |
| `dll_enabled` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | false |
| `elite_account_size_rule` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | Elite account size equals the size of the account that transitions (El… |
| `elite_live_setup_cohort` | 24 | 1 | enum (24) | object (24) | AS_STATED (24) | {"rule":"Elite Live account setup table (start $0, EOD drawdown, contr… |
| `inactivity_closure_days` | 24 | 1 | days (24) | number (24) | >= (24) | 30 |
| `live_reentry_after_failure` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | after failing Elite Live: up to 4-week cool-off depending on live perf… |
| `max_drawdown_amount` | 24 | 1 | USD (24) | number (24) | EQ (24) | 2000 |
| `mll_lock_trigger_eod_balance` | 24 | 1 | USD (24) | number (24) | >= (24) | 2100 |
| `unresolved__live__reserve_unlock` | 24 | 1 | enum (24) | null (24) | UNKNOWN (24) | (null) |
| `dll_amount` | 23 | 2 | USD (18), DOLLAR_SYMBOL_ONLY (5) | number (23) | >= loss triggers (18), EQ (5) | 500 |
| `reserve_unlock_profit_target` | 18 | 1 | USD (18) | number (18) | >= (18) | 3000 |
| `household_live_sim_overlap` | 16 | 1 | boolean (16) | boolean (16) | = (16) | false |
| `live_bonus_eligible` | 16 | 1 | boolean (16) | null (16) | = (16) | (null) |
| `live_close_time_rithmic` | 16 | 1 | enum (16) | string (16) | = (16) | 16:15 EST |
| `live_close_time_tradovate` | 16 | 1 | enum (16) | string (16) | = (16) | 16:45 EST |
| `live_consistency_enabled` | 16 | 1 | boolean (16) | boolean (16) | = (16) | false |
| `live_dll_enabled` | 16 | 1 | boolean (16) | boolean (16) | = (16) | false |
| `live_failure_cooldown` | 16 | 1 | days (16) | number (16) | = (16) | 14 |
| `live_mll_lock_trigger` | 16 | 1 | enum (16) | string (16) | = (16) | profits equal starting live drawdown OR early payout request |
| `live_payout_split` | 16 | 1 | ratio (16) | null (16) | = (16) | (null) |
| `live_scaling_recalculation` | 16 | 1 | enum (16) | string (16) | = (16) | end of day, upward and downward |
| `live_swing_trading_allowed` | 16 | 1 | boolean (16) | boolean (16) | = (16) | false |
| `maximum_live_micros` | 16 | 1 | contracts (16) | number (16) | <= (16) | 20 |
| `maximum_live_minis` | 16 | 1 | contracts (16) | number (16) | <= (16) | 2 |
| `starting_live_drawdown` | 16 | 1 | USD (16) | number (16) | = (16) | 1000 |
| `live_account_program` | 15 | 1 | text (15) | null (15) | UNKNOWN (15) | (null) |
| `live_dd_dll` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `live_split_freq_fees` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `live_elite_split` | 14 | 1 | ratio (14) | number (14) | EQ (14) | 0.8 |
| `live_elite_withdrawals` | 14 | 1 | text (14) | string (14) | EQ (14) | daily_on_business_days |
| `unresolved__live__actual_tier` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live__drawdown` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live__effective_cohort` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live__payout_minimum` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live__position_scaling` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live__reentry` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live__starting_balance` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `commission_schedule` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | broker-specific NinjaTrader/Tradovate referenced rates |
| `initial_mll_balance` | 10 | 1 | DOLLAR_SYMBOL_ONLY (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | -1500 |
| `live_breach_boundary` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_dll_amount` | 10 | 1 | DOLLAR_SYMBOL_ONLY (5), unknown (5) | null (10) | EQ (5), UNKNOWN (5) | (null) |
| `live_drawdown_measurement` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_effective_cohort` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_fees` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_inactivity` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_limit_hit_consequence` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | lose account if position held at limit |
| `live_max_contracts` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_news_blackout` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | flat and no working orders one minute before/during/after FOMC stateme… |
| `live_position_scaling` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_qualifying_weekly_day` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | one round-trip; calendar week Sunday–Friday |
| `live_weekly_trading_requirement` | 10 | 1 | days (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 1 |
| `pro_plus_broker` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | Tradovate |
| `pro_plus_buffer` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | false |
| `pro_plus_drawdown` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | EOD_trailing |
| `pro_plus_split` | 10 | 1 | ratio (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 0.9 |
| `self_match_prevention` | 10 | 1 | text (10) | string (10) | EQ (10) | Unified SMP may reject matching orders across firm accounts; rejection… |
| `closure` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `daily_loss_limit` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `drawdown` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `effective_cohort` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `inactivity` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `new_agreement` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `payout_fee` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `payout_split` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `reentry` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `coverage_gap__077` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__078` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__079` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__080` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__081` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__082` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__083` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__084` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__085` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__086` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__087` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__088` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `live_account_fee` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | none |
| `live_broker` | 8 | 1 | text (8) | string (8) | EQ (8) | Blue Row Capital |
| `live_flat_time_et` | 8 | 1 | text (8) | string (8) | EQ (8) | 4:50 PM ET |
| `live_initial_contract_limit` | 8 | 1 | text (8) | string (8) | EQ (8) | 3 mini / 30 micro |
| `live_initial_drawdown` | 8 | 1 | USD (8) | number (8) | = (8) | 3000 |
| `live_max_accounts` | 8 | 1 | count (8) | number (8) | EQ (8) | 5 |
| `live_payout_request_cap` | 8 | 1 | USD (8) | null (8) | none (8) | (null) |
| `live_requalification_eval_price` | 8 | 1 | USD (8) | number (8) | EQ (8) | 199 |
| `live_safety_net_balance` | 8 | 1 | USD (8) | number (8) | EQ (8) | 3100 |
| `live_trader_split` | 8 | 1 | ratio (8) | number (8) | = (8) | 0.9 |
| `live_account_nature` | 7 | 1 | text (7) | string (7) | EQ (7) | real_fcm_brokerage_account |
| `live_data_fees_per_exchange_month` | 7 | 1 | USD (7) | object (7) | EQ (7) | {"rithmic": 140, "ninjatrader_live": 156} |
| `live_drawdown` | 7 | 1 | text (7) | string (7) | EQ (7) | trailing_intraday_open_equity |
| `live_inactive_closure` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `dll_low_balance_tiers` | 6 | 1 | USD_and_contracts (6) | array (6) | range lookup (6) | [[5000,1000,3],[10000,2000,5]] |
| `full_cashout_closes_account` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `lfa_automated_trading` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `lfa_balance_split` | 6 | 1 | text (6) | string (6) | EQ (6) | 20% tradable (min $10K) / 80% Reserve |
| `lfa_daily_payout_unlock` | 6 | 1 | days (6) | number (6) | >= (6) | 30 |
| `lfa_dll_standard` | 6 | 1 | text (6) | string (6) | EQ (6) | 2000/3000/4500 by size (50K/100K/150K) |
| `lfa_inactivity_days` | 6 | 1 | days (6) | number (6) | > (6) | 30 |
| `lfa_liquidation_floor` | 6 | 1 | USD (6) | number (6) | below (6) | 1000 |
| `lfa_max_accounts` | 6 | 1 | count (6) | number (6) | EQ (6) | 1 |
| `lfa_payout_cap` | 6 | 1 | text (6) | null (6) | EQ (6) | (null) |
| `lfa_sizing` | 6 | 1 | text (6) | string (6) | EQ (6) | Average of eligible XFA tiers, rounded up |
| `live_initial_reserve_fraction` | 6 | 1 | ratio (6) | number (6) | EQ (6) | 0.8 |
| `live_initial_tradable_fraction` | 6 | 1 | ratio (6) | number (6) | EQ (6) | 0.2 |
| `live_market_data_fee_per_exchange` | 6 | 1 | USD (6) | object (6) | AS_STATED (6) | {"usd_per_exchange_per_month":133,"exchanges":["CME","NYMEX","COMEX","… |
| `live_objectives` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | only Max Drawdown remains |
| `live_one_time_buffer_amount` | 6 | 1 | USD (6) | null (6) | UNKNOWN (6) | (null) |
| `market_data_fee_applies` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `minimum_profit_per_winning_day` | 6 | 1 | USD (6) | number (6) | >= (6) | 150 |
| `news_restriction_lfa_applicability` | 6 | 1 | text (6) | null (6) | unresolved (6) | (null) |
| `news_tier1_live_max_contracts_low_balance` | 6 | 1 | contracts (6) | object (6) | AS_STATED (6) | {"balance_below_usd":3000,"max_contracts":1,"limit_scope_note":"per-in… |
| `payout_fraction` | 6 | 1 | ratio (6) | number (6) | <= (6) | 0.5 |
| `qualifying_winning_days` | 6 | 1 | days (6) | number (6) | >= (6) | 5 |
| `reserve_program_cap_usd` | 6 | 1 | USD (6) | number (4), null (2) | LE (6) | 5000 |
| `reserve_program_exists` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `reserve_release_fraction` | 6 | 1 | ratio (6) | number (6) | EQ (6) | 0.25 |
| `reserve_review_time` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | Monday morning |
| `sim_and_live_simultaneous` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `unresolved__live__closure` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__live__inactivity` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__live__payout_frequency` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__live__trader_split` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `account_environment` | 5 | 1 | text (5) | string (5) | EQ (5) | LIVE |
| `cooldown_accounting` | 5 | 1 | text (5) | string (5) | EQ (5) | below-starting-balance ending losses on breach minus TPT payout shares… |
| `cooldown_breach_comparison` | 5 | 1 | text (5) | string (5) | EQ (5) | net TPT capital loss >=10000 |
| `cooldown_lookback` | 5 | 1 | calendar_days (5) | number (5) | EQ (5) | 30 |
| `cooldown_net_capital_loss_threshold` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | number (5) | EQ (5) | 10000 |
| `cooldown_update_events` | 5 | 1 | array (5) | array (5) | EQ (5) | ["account breach actual ending balance","withdrawal TPT share credit"] |
| `dll_breach_effect` | 5 | 1 | text (5) | string (5) | EQ (5) | pause; not account failure |
| `live_cooldown_after_breach_days` | 5 | 1 | days (5) | number (5) | EQ (5) | 21 |
| `live_daily_loss_limit_usd` | 5 | 1 | USD (5) | number (5) | GE (5) | 1000 |
| `live_drawdown_type` | 5 | 1 | text (5) | string (5) | EQ (5) | EOD_TRAILING |
| `live_payout_cadence` | 5 | 1 | text (5) | string (5) | EQ (5) | daily |
| `max_loss_amount` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | number (5) | EQ (5) | 750 |
| `max_micro_contracts` | 5 | 1 | contracts (5) | number (5) | EQ (5) | 10 |
| `max_mini_contracts` | 5 | 1 | contracts (5) | number (5) | EQ (5) | 1 |
| `bonus_gross` | 4 | 1 | USD (4) | number (4) | = (4) | 1000 |
| `full_cashout` | 4 | 1 | enum (4) | string (4) | = (4) | Available; 90/10 split |
| `gm_200k_live_not_fixed_drawdown` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | true |
| `live_consistency` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | None |
| `repeatable_bonus_profit_target` | 4 | 1 | USD (4) | number (4) | >= (4) | 2000 |
| `static_mll` | 4 | 1 | USD (4) | number (4) | = (4) | 100 |
| `live_differs_from_sim` | 3 | 1 | boolean (3) | boolean (3) | EQ (3) | true |
| `live_fixed_drawdown_tcp_200k_400k` | 3 | 1 | boolean (3) | boolean (3) | EQ (3) | true |
| `live_reserve_max_usd` | 3 | 1 | USD (3) | number (3) | LE (3) | 5000 |
| `live_starting_balance_usd` | 3 | 1 | USD (3) | number (3) | EQ (3) | 0 |
| `flat_time` | 2 | 1 | EST (2) | string (2) | by (2) | 16:45 |
| `active_account_limit` | 1 | 1 | accounts (1) | number (1) | <= (1) | 5 |

### Stage `FUNDED` - 2,531 records, 235 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `dll_amount` | 52 | 4 | USD (52) | number (46), null (6) | = (32), EQ (11), N/A (4) | 500 |
| `payout_cap_per_request` | 48 | 1 | USD (48) | number (48) | <= (48) | 1000 |
| `unresolved__funded__data_fee` | 36 | 3 | enum (30), USD (6) | null (30), object (6) | UNKNOWN (30), AS_STATED (6) | {"level1_usd_per_month":0,"level1_scope":"free for all simulated accou… |
| `unresolved__funded__feed_restrictions` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__funded__first_trade_deadline` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__funded__loss_resets_cycle` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__funded__loss_resets_days` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__funded__platform_restrictions` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__funded__qualifying_profit_day` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `pa_scaling_tier` | 34 | 1 | text (34) | string (32), null (2) | EQ (32), unresolved (2) | Profit 0-999: 1 contracts, $500 DLL |
| `max_micro_contracts` | 33 | 2 | contracts (33) | number (33) | <= (24), EQ (5), AS_STATED (4) | 20 |
| `maximum_mini_contracts` | 32 | 1 | contracts (32) | number (32) | = (32) | 1 |
| `platform_fee` | 29 | 2 | USD (24), unknown (5) | number (24), null (5) | AS_STATED (24), UNKNOWN (5) | 0 |
| `max_mini_contracts` | 28 | 1 | contracts (28) | number (28) | <= (24), AS_STATED (4) | 2 |
| `inactivity_rule` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | at least 1 trade per week (Mon-Fri), per account; closure/inactive aft… |
| `max_drawdown_amount` | 24 | 1 | USD (24) | number (24) | EQ (24) | 2000 |
| `mll_lock_trigger_eod_balance` | 24 | 1 | USD (24) | number (24) | >= (24) | 52100 |
| `mll_locked_floor` | 24 | 1 | USD (24) | number (24) | EQ (24) | 50100 |
| `initial_mll_balance` | 23 | 3 | USD (18), unknown (5) | number (18), null (5) | = (8), EQ (6), UNKNOWN (5) | 24000 |
| `consistency_rule_applies` | 22 | 2 | boolean (22) | boolean (22) | EQ (22) | false |
| `position_scaling` | 22 | 2 | text (16), contracts (6) | object (16), array (6) | AS_STATED (22) | [{"profit_from":0,"max_mini":2},{"profit_from":1000,"max_mini":3},{"pr… |
| `contract_scaling` | 21 | 2 | enum (13), boolean (8) | boolean (12), null (9) | UNKNOWN (9), = (8), AS_STATED (4) | false |
| `news_flat_window_after` | 21 | 2 | minute (16), minutes (5) | number (21) | = (16), EQ (5) | 1 |
| `news_flat_window_before` | 21 | 2 | minute (16), minutes (5) | number (21) | = (16), EQ (5) | 1 |
| `locked_mll_balance` | 20 | 2 | USD (20) | number (20) | = (16), AS_STATED (4) | 25100 |
| `dll_breach_effect` | 18 | 3 | text (14), event (4) | string (18) | >= (8), AS_STATED (6), = (4) | liquidate open positions and pause until next session; account remains… |
| `dashboard_update_latency` | 16 | 1 | enum (16) | string (16) | = (16) | 5-30 minutes after last closed trade |
| `funded_consistency_enabled` | 16 | 1 | boolean (16) | boolean (16) | = (16) | false |
| `funded_consistency_percent` | 16 | 1 | ratio (16) | null (16) | = (16) | (null) |
| `funded_household_account_limit` | 16 | 1 | count (16) | number (16) | <= (16) | 5 |
| `funded_reset_available` | 16 | 1 | boolean (16) | null (16) | = (16) | (null) |
| `maximum_daily_sim_profit` | 16 | 1 | USD (16) | number (16) | >= (16) | 6000 |
| `news_breach` | 16 | 1 | enum (16) | string (16) | = (16) | hard breach for holding or opening within restricted window |
| `news_restriction` | 16 | 1 | enum (16) | string (16) | = (16) | High impact AND USD |
| `copy_trading_policy` | 15 | 1 | text (15) | string (15) | EQ (15) | banned_across_names_allowed_own_accounts |
| `exchange_data_fee_funded` | 15 | 1 | text (15) | string (15) | EQ (15) | covered_by_funding_partners |
| `funded_activity_requirement` | 15 | 1 | text (15) | string (15) | GE (15) | weekly_volume_ge_50pct_of_eval_average |
| `funded_commission_rates` | 15 | 1 | USD (15) | object (15) | EQ (15) | {"ES":2.04,"NKD":3.01,"NQ":2.04,"YM":2.02,"EMD":2.04,"GE":2.11,"ZT":1.… |
| `funded_daily_loss_limit` | 15 | 1 | text (15) | null (15) | UNKNOWN (15) | (null) |
| `funded_dynamic_scaling` | 15 | 1 | lots (15) | array (15) | EQ (15) | [{"band":"0-1500","lots":2},{"band":"over_1501","lots":3}] |
| `funded_permitted_times` | 15 | 1 | text (15) | string (15) | EQ (15) | same_315pm_ct_close_rule |
| `funded_scaling_basis` | 15 | 1 | text (15) | string (15) | EQ (15) | cash_on_hand_at_session_open |
| `funded_trailing_drawdown` | 15 | 1 | text (15) | string (15) | EQ (15) | trails_up_locks_at_start_breach_terminates |
| `group_trading_ban` | 15 | 1 | boolean (15) | boolean (15) | EQ (15) | true |
| `hedging_ban` | 15 | 1 | boolean (15) | boolean (15) | EQ (15) | true |
| `max_funded_accounts` | 15 | 1 | count (15) | number (15) | EQ (15) | 3 |
| `news_event_list` | 15 | 1 | text (15) | string (15) | EQ (15) | fomc_nfp_cpi_ppi_ism_jolts_retail_gdp_unemployment_treasury_auctions_e… |
| `news_flat_rule_funded` | 15 | 1 | text (15) | string (15) | EQ (15) | flat_1min_before_during_after |
| `payout_methods` | 15 | 2 | text (15) | null (15) | EQ (8), UNKNOWN (7) | (null) |
| `platform_fee_funded` | 15 | 1 | text (15) | string (15) | EQ (15) | trader_responsible_except_free_platforms |
| `post_safety_net_minimum_balance` | 15 | 1 | USD (15) | number (15) | EQ (15) | 50100 |
| `probation_pnl_rule` | 15 | 1 | text (15) | string (15) | GT (15) | positive_net_pnl_above_start_each_15d_for_90d |
| `prohibited_short_duration_trading` | 15 | 1 | text (15) | string (15) | EQ (15) | sub_10s_and_data_inefficiency_exploits_banned |
| `trader_tax_status` | 15 | 1 | text (15) | string (15) | EQ (15) | independent_contractor_ordinary_income |
| `two_strike_policy` | 15 | 1 | text (15) | null (15) | UNKNOWN (15) | (null) |
| `approved_trade_copiers` | 14 | 1 | text (14) | array (14) | EQ (14) | ["Tradesyncer","Tradecopia","Affordable Indicators","Replikanto Flowbo… |
| `commission_per_side_mnq` | 14 | 1 | USD (14) | number (14) | EQ (14) | 0.51 |
| `commission_per_side_nq` | 14 | 1 | USD (14) | number (14) | EQ (14) | 2.04 |
| `consistency_rule_funded_pct` | 14 | 1 | ratio (14) | null (9), number (5) | EQ (9), LE (5) | 0.5 |
| `ea_algo_require_written_authorization` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `elite_loss_limit_rule_20_35` | 14 | 1 | text (14) | string (14) | EQ (14) | lose_gt_35pct_of_accumulated_profit_after_20pct_growth |
| `elite_reset_max_times` | 14 | 1 | times (14) | number (14) | EQ (14) | 10 |
| `equities_options_trading_supported` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | false |
| `forex_trading_supported` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | false |
| `funded_weekly_trade_requirement` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `hedging_prohibited` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `login_every_30_days` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `loss_resets_cycle` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `loss_resets_days` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `master_daily_loss_limit_removal` | 14 | 1 | text (14) | null (14) | unknown (14) | (null) |
| `max_contracts` | 14 | 2 | enum (9), contracts (5) | null (9), number (5) | UNKNOWN (9), EQ (5) | 3 |
| `missed_week_closes_funded` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `safety_net_requirement` | 14 | 1 | USD (14) | number (14) | EQ (14) | 2100 |
| `same_household_participation_prohibited` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `sim_funded_drawdown_type` | 14 | 1 | text (14) | string (14) | EQ (14) | INTRADAY_TRAILING |
| `sim_uses_real_cme_market_data` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `supported_platforms` | 14 | 1 | text (14) | array (14) | EQ (14) | ["TradingView","NinjaTrader","Tradovate","Quantower","Sierra Chart","M… |
| `trading_for_others_prohibited` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `vpn_proxy_vps_prohibited` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `funded_drawdown_lock` | 13 | 2 | text (13) | null (7), string (6) | unknown (7), AS_STATED (6) | locks at initial simulated capital for remaining life of account |
| `max_loss_amount` | 13 | 2 | USD (8), DOLLAR_SYMBOL_ONLY (5) | number (13) | = (8), EQ (5) | 1000 |
| `initial_trail_balance` | 12 | 1 | USD (12) | number (12) | > (8), AS_STATED (4) | 26100 |
| `payout_minimum` | 12 | 2 | USD (12) | number (12) | >= (12) | 500 |
| `unresolved__funded__platform_fee` | 12 | 2 | enum (6), USD (6) | null (12) | UNKNOWN (12) | (null) |
| `mll_lock_floor` | 11 | 2 | USD (6), text (5) | number (6), string (5) | EQ (11) | original starting balance |
| `unresolved__funded__position_scaling` | 10 | 2 | contracts (6), enum (4) | object (6), null (4) | AS_STATED (6), UNKNOWN (4) | {"basis":"current XFA account balance (XFA balance starts at $0)","lot… |
| `consistency_performance` | 9 | 1 | enum (5), boolean (4) | null (5), boolean (4) | UNKNOWN (5), EQ (4) | false |
| `daily_loss_limit_exists` | 9 | 1 | boolean (9) | boolean (9) | EQ (9) | false |
| `daily_pause_amount` | 9 | 1 | enum (5), USD (4) | null (5), number (4) | UNKNOWN (5), EQ (4) | 1000 |
| `dll_consequence` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `dll_trigger_boundary` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `dll_type` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `feed_restrictions` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `flat_time` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `floor_locks_at_starting_balance` | 9 | 1 | boolean (9) | boolean (9) | EQ (9) | true |
| `news_window` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `overnight_holding` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `platform_restrictions` | 9 | 1 | text (9) | string (9) | EQ (9) | Tradovate |
| `qualifying_profit_day` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `tier1_news_sim_funded` | 9 | 1 | text (9) | string (9) | EQ (9) | restricted |
| `trading_commission` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `weekend_holding` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `account_environment` | 8 | 1 | type (8) | string (8) | = (8) | simulated |
| `breach_balance_boundary` | 8 | 1 | balance (8) | string (8) | <= (8) | MLL |
| `consistency_rule_pa` | 8 | 1 | ratio (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__089` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__090` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__091` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__092` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__093` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__094` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__095` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__096` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__097` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__098` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__099` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__100` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__101` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__102` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `dll_amount_initial` | 8 | 1 | USD (8) | number (7), null (1) | EQ (7), none (1) | 1250 |
| `dll_enabled` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | false |
| `dll_increased_amount_at_balance` | 8 | 1 | USD (8) | object (7), null (1) | AS_STATED (7), none (1) | {"balance_threshold":53000,"new_dll":2000,"effective":"next trading se… |
| `dll_reset` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | 6:00 PM ET next session |
| `dll_selected` | 8 | 1 | boolean (8) | boolean (8) | = (8) | true |
| `drawdown_type` | 8 | 1 | type (8) | string (8) | = (8) | end_of_day_trailing |
| `eod_trailing_drawdown` | 8 | 1 | enum (8) | null (8) | UNKNOWN (8) | (null) |
| `mae_rule` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | false |
| `max_active_pa_accounts_household` | 8 | 1 | count (8) | number (8) | <= (8) | 20 |
| `max_drawdown` | 8 | 1 | USD (8) | number (8) | = (8) | 1000 |
| `max_payouts_per_account` | 8 | 1 | count (8) | number (8) | <= (8) | 5 |
| `max_payouts_per_pa` | 8 | 1 | count (8) | number (8) | <= (8) | 6 |
| `mixed_contract_conversion` | 8 | 1 | micro_per_mini (8) | number (8) | = (8) | 10 |
| `mll_lock_trigger` | 8 | 1 | USD (8) | number (8) | >= (8) | 26100 |
| `pa_inactivity_rule` | 8 | 1 | text (8) | string (8) | EQ (8) | 2 trading days with >=$50 net profit in every rolling 30-day window; o… |
| `payout_cycle_days` | 8 | 1 | days (8) | number (8) | EQ (8) | 5 |
| `payout_denials` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | true |
| `payout_min_balance_to_request` | 8 | 1 | USD (8) | number (8) | >= (8) | 26600 |
| `payout_qualifying_min_daily_profit` | 8 | 1 | USD (8) | number (8) | >= (8) | 100 |
| `payout_split_sim` | 8 | 1 | ratio (8) | number (8) | EQ (8) | 1 |
| `risk_reward_rule` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | false |
| `scaling_built_in` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | true |
| `scaling_can_decrease` | 8 | 1 | boolean (8) | boolean (8) | AS_STATED (8) | true |
| `scaling_update` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | prior full trading-session ending balance sets next session tier; no i… |
| `starting_balance` | 8 | 1 | USD (8) | number (8) | = (8) | 25000 |
| `funded_loss_reset_days` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `funded_max_contracts` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `funded_news` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `funded_platform_feed_limits` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `payout_split` | 7 | 1 | ratio (7) | null (4), number (3) | UNKNOWN (4), EQ (3) | 0.8 |
| `back2funded_eligible` | 6 | 1 | boolean (6) | null (6) | UNKNOWN (6) | (null) |
| `back2funded_fee` | 6 | 1 | USD (6) | number (6) | EQ (6) | 599 |
| `back2funded_max_reactivations` | 6 | 1 | count (6) | number (6) | <= (6) | 2 |
| `back2funded_window_days` | 6 | 1 | days (6) | null (6) | unresolved (6) | (null) |
| `funded_subscription_fee` | 6 | 1 | USD (6) | number (6) | EQ (6) | 0 |
| `level2_subscription_carries_to_xfa` | 6 | 1 | boolean (6) | null (6) | unresolved (6) | (null) |
| `profit_target_required` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `scaling_tier_boundary_inclusivity` | 6 | 1 | enum (6) | null (4), object (2) | UNKNOWN (4), AS_STATED (2) | {"tiers":[{"balance_text":"Below $1,500","rule":"balance < 1500","max_… |
| `sim_funded_inactivity_closure_days` | 6 | 1 | days (6) | number (6) | >= (6) | 30 |
| `sim_funded_reset_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `unresolved__funded__consistency` | 6 | 1 | ratio (6) | object (6) | AS_STATED (6) | {"by_xfa_payout_path":{"STANDARD":{"consistency_target":"NONE"},"CONSI… |
| `unresolved__funded__dll_amount` | 6 | 1 | USD (6) | object (6) | AS_STATED (6) | {"dll_optional":true,"amount_if_selected_usd_by_size":{"50000":1000,"1… |
| `unresolved__funded__drawdown` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `xfa_dll_non_topstepx` | 6 | 1 | boolean (6) | null (6) | UNKNOWN (6) | (null) |
| `xfa_max_accounts` | 6 | 1 | count (6) | number (6) | <= (6) | 5 |
| `xfa_mll_trailing` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `xfa_scaling_plan` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `xfa_trading_hours` | 6 | 1 | text (6) | string (6) | EQ (6) | Normal electronic; flat by 3:10 PM CT |
| `daily_loss_limit_type` | 5 | 1 | text (5) | string (5) | EQ (5) | soft_pause |
| `data_fee` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `fomc_minutes_speakers_allowed` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | true |
| `funded_dll_amount` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | null (5) | EQ (5) | (null) |
| `funded_qualifying_profit_day` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `inactivity_rule_days` | 5 | 1 | days (5) | number (5) | LE (5) | 7 |
| `intraday_trail_basis` | 5 | 1 | text (5) | string (5) | EQ (5) | peak including realized and unrealized gains |
| `max_builder_accounts_per_user` | 5 | 1 | count (5) | number (5) | EQ (5) | 1 |
| `mll_breach_balance_comparison` | 5 | 1 | text (5) | string (5) | EQ (5) | equity <= current minimum account balance |
| `mll_breach_consequence` | 5 | 1 | text (5) | string (5) | EQ (5) | immediate liquidation |
| `monthly_rebilling` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `news_working_orders_allowed` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `platform_feed_restrictions` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `pro_automated_trading` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `pro_consistency_rule` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `pro_drawdown_type` | 5 | 1 | text (5) | string (5) | EQ (5) | INTRADAY_trailing |
| `pro_is_sim` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | true |
| `pro_limit_up_down` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | true |
| `pro_max_drawdown` | 5 | 1 | text (5) | string (5) | EQ (5) | same as passed test |
| `pro_news_blackout` | 5 | 1 | text (5) | string (5) | EQ (5) | 1 min before/during/after |
| `pro_resets` | 5 | 1 | count (5) | number (5) | <= (5) | 3 |
| `pro_scaling_plan` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `pro_weekly_trading_requirement` | 5 | 1 | days (5) | number (5) | >= (5) | 1 |
| `weekly_day_definition` | 5 | 1 | text (5) | string (5) | EQ (5) | one round-trip in calendar week Sunday–Friday |
| `consistency_formula` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | largest_day_profit / cycle_profit <= 0.20 |
| `consistency_required_profit` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | MAX(size_cycle_goal, largest_day_profit / 0.20) |
| `consistency_zero_denominator` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Do not divide when cycle_profit <= 0; ineligible for positive profit g… |
| `derived_mll_formula` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | MIN(highest_EOD_balance - MLL_amount, starting_balance + 100) |
| `dll_breach` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Trading stops until next session; account remains valid unless MLL als… |
| `dll_scaling_activation_balance` | 4 | 1 | USD (4) | number (4) | EOD_close > (4) | 26100 |
| `dll_scaling_can_decrease` | 4 | 1 | boolean (4) | boolean (4) | = (4) | false |
| `dll_scaling_coefficient` | 4 | 1 | ratio (4) | number (4) | = (4) | 0.6 |
| `drawdown_breach` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Account balance reaches MLL threshold |
| `drawdown_lock_level_usd` | 4 | 1 | USD (4) | number (4) | EQ (4) | 100 |
| `drawdown_observation` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Highest session-closing balance; trailing threshold rises until start … |
| `gross_to_net` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | request * 0.90 |
| `max_contracts_mini` | 4 | 1 | contracts (4) | number (4) | <= (4) | 4 |
| `maximum_sim_payouts` | 4 | 1 | payouts (4) | number (4) | AS_STATED (4) | 5 |
| `minimum_days_arithmetic` | 4 | 1 | contributing profitable days (4) | number (4) | AS_STATED (4) | 5 |
| `minimum_days_separate_rule` | 4 | 1 | enum (4) | null (4) | AS_STATED (4) | (null) |
| `mll_amount` | 4 | 1 | USD (4) | number (4) | AS_STATED (4) | 1000 |
| `objectives_refresh` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | 5–30 minutes after last closed trade |
| `overnight_positions` | 4 | 1 | text (4) | string (4) | EQ (4) | prohibited |
| `payout_buffer` | 4 | 1 | enum (4) | null (4) | AS_STATED (4) | (null) |
| `payout_caps` | 4 | 1 | USD (4) | null (4) | UNKNOWN (4) | (null) |
| `payout_compliance` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Trading rules, terms, and Direct agreement must be respected |
| `payout_cycle_reset` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Cycle goals and consistency restart after approved payout |
| `payout_frequency` | 4 | 1 | text (4) | string (4) | EQ (4) | daily |
| `payout_processing` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Approved request deducted within minutes; disbursement within 2 busine… |
| `payout_requests_final` | 4 | 1 | enum (4) | boolean (4) | AS_STATED (4) | true |
| `payout_window` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Any eligible day; no fixed window |
| `pending_request_risk` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Trading before processing can cause denial if cycle profit falls below… |
| `sim_funded_max_loss_usd` | 4 | 1 | USD (4) | number (4) | UNKNOWN (4) | 1000 |
| `unresolved__funded__starting_balance` | 4 | 1 | enum (4) | null (4) | UNKNOWN (4) | (null) |
| `daily_pause` | 3 | 1 | boolean (3) | boolean (3) | EQ (3) | true |
| `dll_fixed_amount` | 3 | 1 | USD (3) | number (3) | >= loss triggers (3) | 1200 |
| `dll_scale_formula` | 3 | 1 | enum (3) | string (3) | AS_STATED (3) | 0.60 * highest end-of-day ACCOUNT PROFIT |
| `dll_scale_trigger` | 3 | 1 | enum (3) | string (3) | AS_STATED (3) | Prior session closes strictly above size-specific Initial Trail Balanc… |
| `drawdown_lock_after_first_payout` | 3 | 1 | boolean (3) | boolean (3) | EQ (3) | true |
| `full_contract_allocation_from_day_one` | 3 | 1 | boolean (3) | boolean (3) | EQ (3) | true |
| `payout_best_day_cap` | 3 | 1 | ratio (3) | number (3) | <= (3) | 0.35 |
| `payout_cap` | 3 | 1 | USD (3) | number (3) | <= (3) | 1250 |
| `payout_minimum_net` | 3 | 1 | USD (3) | number (3) | >= (3) | 100 |
| `payout_qualifying_days` | 3 | 1 | days (3) | number (3) | >= (3) | 5 |
| `active_account_limit` | 1 | 1 | accounts (1) | number (1) | <= (1) | 5 |
| `dll_25k` | 1 | 1 | enum (1) | string (1) | AS_STATED (1) | None |
| `max_sim_funded_accounts` | 1 | 1 | count (1) | number (1) | LE (1) | 3 |
| `sim_funded_initial_balance_usd` | 1 | 1 | USD (1) | number (1) | EQ (1) | 0 |

### Stage `LIVE_REVIEW` - 1,759 records, 99 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `remaining_sim_accounts` | 60 | 1 | enum (60) | string (60) | = (60) | closed; evaluation fee refunded for funded accounts with zero payouts |
| `cashout_choice_deadline_hours` | 48 | 1 | hours (48) | number (32), null (16) | within (32), AS_STATED (16) | 24 |
| `cashout_no_choice_default` | 48 | 1 | enum (48) | string (32), null (16) | AS_STATED (48) | automatic_move_to_live |
| `unresolved_live_effective_cohort` | 48 | 1 | enum (48) | null (48) | AS_STATED (48) | (null) |
| `cashout_rate` | 44 | 1 | ratio of live starting balance (44) | null (44) | = (44) | (null) |
| `eligible_funded_account_payouts` | 44 | 1 | payout (44) | number (44) | >= (44) | 1 |
| `live_accounts_per_eligible_funded_account` | 44 | 1 | account (44) | number (44) | = (44) | 1 |
| `other_review_triggers` | 44 | 1 | enum (44) | string (44) | = (44) | Lifetime payouts; exceptional performance; previously live; Daily maxi… |
| `zero_payout_funded_refund` | 44 | 1 | enum (44) | string (44) | = (44) | Evaluation cost |
| `unresolved__live_review__bonus` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__live_review__buffer_transfer` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__live_review__escrow` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__live_review__new_agreement` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__live_review__pending_payout_transfer` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__live_review__refund` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `live_review_trigger` | 30 | 2 | text (30) | object (24), string (6) | AS_STATED (30) | invitation only after FTMO validates sim-funded trading; not automatic |
| `unresolved__live_review__country_eligibility` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__live_review__latest_transition` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `ineligible_funded_refund_min_remaining_drawdown` | 28 | 1 | ratio (28) | number (28) | >= (28) | 0.5 |
| `maximum_sim_payouts` | 28 | 1 | payouts (28) | number (16), null (12) | <= (28) | 5 |
| `cool_off_period` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | up to 4 weeks |
| `earliest_live_transition` | 24 | 1 | text (24) | null (24) | UNKNOWN (24) | (null) |
| `elite_exclusivity` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | Elite Live holders may hold no other Tradeify accounts; household memb… |
| `elite_live_setup_cohort` | 24 | 1 | enum (24) | object (24) | AS_STATED (24) | {"rule":"Elite Live account setup table (start $0, EOD drawdown, contr… |
| `live_review_discretionary_mandatory` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | discretionary selection; mandatory once selected |
| `min_payouts_on_account_to_transition` | 24 | 1 | count (24) | number (24) | >= (24) | 1 |
| `no_return_to_sim_after_live_denial` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | true |
| `sim_balance_carries_to_elite_live` | 24 | 1 | boolean (24) | boolean (24) | AS_STATED (24) | false |
| `sim_profit_carries_to_elite_live` | 24 | 1 | boolean (24) | boolean (24) | AS_STATED (24) | false |
| `live_review` | 22 | 3 | text (13), unknown (5), enum (4) | string (17), null (5) | AS_STATED (12), EQ (5), UNKNOWN (5) | invitation-based discretionary selection at any time; no automatic qua… |
| `funded_transition_terms` | 20 | 1 | text (20) | string (20) | AS_STATED (20) | after at least three successful payouts the Master-level accounts may … |
| `live_split_and_payout_frequency` | 20 | 1 | text (20) | null (20) | unknown (20) | (null) |
| `funded_initial_eod_drawdown_usd` | 16 | 1 | USD (16) | number (16) | EQ (16) | 1500 |
| `live_accounts_per_eligible_funded` | 16 | 1 | count (16) | number (16) | = (16) | 1 |
| `live_cashout_option` | 16 | 1 | ratio (16) | null (16) | = (16) | (null) |
| `live_eligibility_prior_payouts` | 16 | 1 | count (16) | number (16) | >= (16) | 1 |
| `other_live_review_triggers` | 16 | 1 | enum (16) | string (16) | = (16) | substantial lifetime payouts; exceptional simulation performance; prev… |
| `refund_remaining_drawdown_condition_daily_applicability` | 16 | 1 | enum (16) | null (16) | AS_STATED (16) | (null) |
| `transition_accounting_cutoff` | 16 | 1 | enum (16) | string (16) | = (16) | prior-day closing balance; disregard move-session P&L |
| `transition_buffer` | 16 | 1 | enum (16) | string (16) | = (16) | funds live drawdown; not withdrawable |
| `transition_daily_profit_outcome` | 16 | 1 | enum (16) | null (16) | = (16) | (null) |
| `transition_excess_above_cap` | 16 | 1 | enum (16) | string (16) | = (16) | not withdrawable |
| `transition_processing` | 16 | 1 | enum (16) | string (16) | = (16) | after evening 6 PM EST report; may take hours; pause and flatten |
| `transition_sim_cashout_cap` | 16 | 1 | USD (16) | number (16) | <= (16) | 15000 |
| `transition_sim_cashout_qualifier` | 16 | 1 | enum (16) | string (16) | = (16) | profits above buffer, after broker KYC and subaccount approval |
| `live_post_cap` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `live_sim_funds_fate` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `live_timing` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `unresolved__live_review__earliest_transition` | 12 | 2 | enum (6), text (6) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live_review__effective_cohort` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live_review__live_starting_balance` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live_review__profit_transfer` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__live_review__sim_payout_limit_handling` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `escrow_bonus` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `excess_frozen_profit_withdrawal` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | above5000 available under PRO split |
| `live_earliest_transfer` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_latest_transfer` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_mandatory_or_discretionary` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_onboarding_required` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | true |
| `live_setup_typical` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | several days after requirements satisfied |
| `live_trigger_threshold` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `payout_cap_transition` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `pro_account_put_on_hold` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | true |
| `pro_profit_frozen` | 10 | 1 | DOLLAR_SYMBOL_ONLY (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 5000 |
| `professional_data_pause_max` | 10 | 1 | hours (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 12 |
| `refund_on_transition` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `sim_buffer_destination` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `sim_capital_destination` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `sim_pending_payout_destination` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `after_payout_limit` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `bonus` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `buffer_destination` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `discretionary_or_mandatory` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `earliest_transition` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `effective_cohort` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `escrow` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `latest_transition` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `new_agreement` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `payout_destination` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `profit_destination` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `refund` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `review_trigger` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `sim_balance_destination` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `firm_right_to_move_live` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | Tradeify reserves the right to move the trader to a Live Funded Accoun… |
| `live_transition_trigger` | 8 | 1 | text (8) | string (8) | EQ (8) | five_consecutive_payouts |
| `transition_sim_profit_treatment` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | eligible positive simulatedPA profits tracked as potential Bonus Vault… |
| `country_live_eligibility` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `live_ineligible_countries` | 6 | 1 | enum (6) | array (6) | AS_STATED (6) | ["Algeria","Benin","Bosnia and Herzegovina","Botswana","Bulgaria","Cam… |
| `live_setup_business_days` | 6 | 1 | business_days (6) | object (6) | RANGE (6) | {"min":7,"max":10} |
| `live_transition_auto_trigger_usd` | 6 | 1 | USD (6) | number (6) | GE (6) | 10000 |
| `live_transition_choice` | 6 | 1 | enum (6) | array (6) | AS_STATED (6) | ["move to Live","close XFA"] |
| `live_transition_review_path` | 6 | 1 | text (6) | string (6) | EQ (6) | risk_team_review_on_consistent_payouts |
| `transition_balance_cap` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | live_account_tier |
| `unresolved__live_review__review_trigger` | 6 | 1 | text (6) | object (6) | AS_STATED (6) | {"trigger_type":"DISCRETIONARY_RISK_TEAM_REVIEW","basis":"Risk Team re… |
| `unresolved__live_review__sim_balance_transfer` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `development_exit_review` | 5 | 1 | text (5) | string (5) | EQ (5) | roughly60 days disciplined risk management; manual review anytime |
| `pro_plus_invite_only` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | true |
| `funded_starting_drawdown` | 4 | 1 | text (4) | null (4) | unknown (4) | (null) |
| `live_scaling_and_drawdown` | 4 | 1 | text (4) | null (4) | unknown (4) | (null) |

### Stage `ACTIVATION` - 1,044 records, 86 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `first_trade_deadline` | 41 | 4 | text (27), enum (9), unknown (5) | null (41) | unknown (27), UNKNOWN (14) | (null) |
| `activation_deadline` | 38 | 4 | days (16), enum (9), text (8) | null (30), string (8) | UNKNOWN (30), AS_STATED (8) | 6:00 PM ET on the seventh calendar day after marked Passed (worked exa… |
| `unresolved__activation__day_counter_reset` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__activation__dll_reset` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__activation__first_trade_deadline` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__activation__floor_reset` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__activation__high_water_reset` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved_activation_state` | 32 | 1 | enum (32) | null (32) | AS_STATED (32) | (null) |
| `unresolved__activation__agreement` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `activation_fee` | 28 | 2 | USD (28) | number (23), null (5) | EQ (15), = (8), UNKNOWN (5) | 0 |
| `identity_verification_timing` | 24 | 1 | enum (24) | object (24) | AS_STATED (24) | {"standard":"before first payout","listed_country_residents":"before f… |
| `activation_covers` | 20 | 1 | text (20) | string (12), null (8) | EQ (20) | market data + account maintenance |
| `activation_fee_usd` | 20 | 1 | USD (20) | number (20) | EQ (20) | 98 |
| `balance_carryover` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | false |
| `balance_profit_carry_over` | 20 | 1 | text (20) | null (20) | unknown (20) | (null) |
| `unresolved__activation__activation_deadline` | 20 | 3 | enum (20) | null (20) | UNKNOWN (20) | (null) |
| `payout_policy_choice_permanent` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | true |
| `unresolved__activation__activation_latency` | 16 | 3 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `unresolved__activation__pass_review` | 16 | 3 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `activation_payment_terms` | 15 | 1 | text (15) | string (15) | EQ (15) | auto_charge_on_approval_with_7d_grace |
| `activation_state_carryover` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `funding_steps` | 15 | 1 | text (15) | string (15) | EQ (15) | questionnaire_contract_credentials |
| `funding_timeline_days` | 15 | 1 | business_days (15) | number (15) | EQ (15) | 3 |
| `kyc_id_requirement` | 15 | 1 | text (15) | string (15) | EQ (15) | government_id_with_dob |
| `activation_latency` | 14 | 2 | enum (9), unknown (5) | null (14) | UNKNOWN (14) | (null) |
| `activation_link_expiry_days` | 12 | 1 | days (12) | number (12) | EQ (12) | 7 |
| `master_agreement_signing` | 12 | 1 | boolean (12) | boolean (12) | EQ (12) | true |
| `account_agreement_verified` | 11 | 2 | enum (6), unknown (5) | null (11) | UNKNOWN (11) | (null) |
| `unresolved__activation__profit_carryover` | 10 | 2 | enum (10) | null (10) | UNKNOWN (10) | (null) |
| `activation_immediate_from_dashboard` | 9 | 1 | boolean (9) | boolean (9) | EQ (9) | true |
| `carryover_balance` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `carryover_profit` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `contract` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `data_fee` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `days_reset` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `dll_reset` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `feed_restrictions` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `floor_reset` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `highwater_reset` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `kyc` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `pass_review` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `payment` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `platform_fee` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `platform_restrictions` | 9 | 1 | text (9) | string (9) | EQ (9) | Tradovate |
| `activation_deadline_anchor` | 8 | 1 | enum (8) | string (8) | AS_STATED (8) | official_marked_passed_after_market_close |
| `activation_latency_max` | 8 | 1 | hours (8) | number (8) | <= (8) | 6 |
| `activation_same_size_type` | 8 | 1 | boolean (8) | boolean (8) | = (8) | true |
| `coverage_gap__038` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__039` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__040` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__041` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__042` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__043` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__044` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__045` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `coverage_gap__046` | 8 | 1 | enum (8) | null (8) | unresolved (8) | (null) |
| `pa_activation_fee_refundable` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | false |
| `post_pass_review_and_approval` | 8 | 1 | text (8) | null (8) | unknown (8) | (null) |
| `gm_funded_size_matches_eval` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | true |
| `live_setup_time_days` | 7 | 1 | days (7) | number (7) | LTE (7) | 10 |
| `livesim_activation_window_days` | 7 | 1 | days (7) | number (7) | LTE (7) | 30 |
| `livesim_setup_time_business_days` | 7 | 1 | days (7) | number (7) | EQ (7) | 2 |
| `post_pass_process` | 7 | 1 | text (7) | string (7) | EQ (7) | e2t_verifies_forwards_to_helios_or_appius_partner_offers_livesim_or_li… |
| `identity_verification_required` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `sim_funded_starting_balance` | 6 | 1 | USD (6) | number (6) | EQ (6) | 50000 |
| `unresolved__activation__kyc` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `xfa_starting_balance` | 6 | 1 | USD (6) | number (6) | EQ (6) | 0 |
| `activation_balance_carryover` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `activation_days_reset` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `activation_dll_reset` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `activation_floor_reset` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `activation_hwm_reset` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `activation_profit_carryover` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `activation_review` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `overdue_subscription_blocks_activation` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | true |
| `passed_test_activation_limit` | 5 | 1 | count (5) | number (5) | EQ (5) | 10 |
| `passed_test_activation_window` | 5 | 1 | calendar_days (5) | number (5) | EQ (5) | 30 |
| `pro_activation_fee` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | number (5) | EQ (5) | 130 |
| `verification_documents` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `max_activations_per_day` | 4 | 1 | count (4) | number (4) | <= (4) | 5 |
| `sim_funded_reset_available` | 4 | 1 | boolean (4) | boolean (4) | EQ (4) | false |
| `unresolved__activation__balance_carryover` | 4 | 1 | enum (4) | null (4) | UNKNOWN (4) | (null) |
| `activation_after_purchase` | 3 | 1 | text (3) | string (3) | EQ (3) | immediate_on_payment |
| `activation_fee_naf` | 3 | 1 | USD (3) | number (3) | EQ (3) | 0 |
| `activation_fee_standard` | 3 | 1 | USD (3) | number (3) | EQ (3) | 149 |
| `funded_account_provisioned_within_72h` | 2 | 1 | boolean (2) | boolean (2) | EQ (2) | true |

### Stage `EVALUATION;FUNDED` - 950 records, 84 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `touch_is_breach` | 47 | 4 | boolean (47) | boolean (47) | EQ (39), <= (8) | true |
| `breach_observation_basis` | 36 | 3 | enum (24), text (12) | string (36) | AS_STATED (36) | EQUITY = balance + open P&L − commissions |
| `news_trading` | 36 | 2 | enum (28), text (8) | boolean (28), string (8) | = (28), AS_STATED (8) | normal strategy allowed; gambling/bracketing both sides to chase news … |
| `drawdown_type` | 30 | 2 | enum (30) | string (30) | AS_STATED (30) | EOD_TRAILING |
| `mini_micro_ratio` | 30 | 2 | micros per mini (30) | number (30) | EQ (30) | 10 |
| `holiday_flat` | 28 | 1 | enum (28) | string (28) | = (28) | Before actual early market close |
| `late_position_handling` | 28 | 1 | enum (28) | string (28) | = (28) | Auto-close without failed account |
| `market_reopen` | 28 | 1 | EST, Sunday-Thursday (28) | string (28) | at (28) | 18:00 |
| `weekday_flat_time` | 28 | 1 | EST, Monday-Friday (28) | string (28) | by (28) | 16:45 |
| `dll_breach_effect` | 22 | 2 | enum (16), text (6) | string (21), null (1) | AS_STATED (21), none (1) | flatten positions; cancel pending orders; block new trades until next … |
| `mll_breach_balance_comparison` | 22 | 2 | balance (16), text (6) | string (22) | <= (16), AS_STATED (6) | account balance <= current MLL |
| `dll_amount` | 17 | 3 | USD (17) | number (9), null (8) | = (8), >= loss triggers (6), EQ (3) | 1000 |
| `inactivity_calendar_days` | 17 | 2 | days (17) | number (17) | <= (9), < (8) | 7 |
| `inactivity_window` | 17 | 1 | calendar_days (16), calendar days (1) | number (17) | = (16), within (1) | 30 |
| `configuration_change_allowed` | 16 | 1 | boolean (16) | boolean (16) | = (16) | false |
| `inactivity_failure` | 16 | 1 | enum (16) | string (16) | = (16) | permanent deletion |
| `inactivity_qualifier` | 16 | 1 | enum (16) | string (16) | = (16) | trade resulting in at least $1 net profit or loss |
| `initial_mll_balance` | 16 | 1 | USD (16) | number (16) | = (16) | 24000 |
| `initial_trail_balance` | 16 | 1 | USD (16) | number (16) | > (16) | 26100 |
| `intraday_trail_basis` | 16 | 1 | enum (16) | string (16) | = (16) | real-time realized and unrealized P&L |
| `locked_mll_balance` | 16 | 1 | USD (16) | number (16) | = (16) | 25100 |
| `max_loss_allowance` | 16 | 1 | USD (16) | number (16) | = (16) | 1000 |
| `mixed_mini_micro_exposure_formula` | 16 | 1 | enum (16) | null (16) | = (16) | (null) |
| `mll_breach_consequence` | 16 | 1 | enum (16) | string (16) | = (16) | account breach |
| `session_reset_time` | 16 | 1 | text (16) | string (16) | AS_STATED (16) | 6:00 PM ET |
| `sim_contract_scaling_schedule` | 16 | 1 | enum (16) | null (16) | = (16) | (null) |
| `simulation_daily_close_time` | 16 | 1 | enum (16) | null (16) | = (16) | (null) |
| `configuration_mutable_after_purchase` | 14 | 2 | boolean (14) | boolean (14) | = (8), EQ (6) | false |
| `dll_enabled` | 14 | 2 | boolean (14) | boolean (14) | = (8), EQ (6) | false |
| `mlldrawdown_update_event` | 14 | 2 | event (8), text (6) | string (14) | = (8), AS_STATED (6) | session_end_historical_high_closing_balance |
| `news_tier1_window_micro_cap` | 12 | 1 | contracts (12) | number (12) | <= (6), LE (6) | 3 |
| `account_environment` | 9 | 1 | enum (9) | string (9) | EQ (9) | simulated |
| `trail_reference` | 9 | 1 | enum (9) | string (9) | EQ (9) | highest_end_of_day_balance |
| `active_eval_household_limit` | 8 | 1 | accounts (8) | number (8) | <= (8) | 10 |
| `active_funded_household_limit` | 8 | 1 | accounts (8) | number (8) | <= (8) | 5 |
| `automation_and_algorithms_allowed` | 8 | 1 | boolean (8) | boolean (8) | AS_STATED (8) | false |
| `combined_eval_funded_household_limit` | 8 | 1 | accounts (8) | number (8) | <= (8) | 10 |
| `dashboard_update_latency` | 8 | 1 | minutes (8) | string (8) | = (8) | 5-30 |
| `dll_on_price_relative` | 8 | 1 | comparison (8) | string (8) | = (8) | lower_than_OFF |
| `dll_recovery` | 8 | 1 | enum (8) | string (8) | = (8) | next trading session |
| `dll_session_reference_balance` | 8 | 1 | enum (8) | null (8) | = (8) | (null) |
| `dll_soft_breach_requires` | 8 | 1 | enum (8) | string (8) | = (8) | MLL not reached |
| `dll_type` | 8 | 1 | enum (8) | string (8) | = (8) | fixed |
| `drawdown_observation` | 8 | 1 | enum (8) | object (8) | AS_STATED (8) | {"reference":"highest_end_of_day_balance","update":"4:59:59 PM ET per … |
| `fixed_dll` | 8 | 1 | USD (8) | number (8) | >= (8) | 600 |
| `holiday_close_override` | 8 | 1 | event (8) | string (8) | = (8) | earlier_market_close |
| `inactivity_qualifying_absolute_net_pnl` | 8 | 1 | USD (8) | number (8) | >= (8) | 1 |
| `late_position_effect` | 8 | 1 | event (8) | string (8) | = (8) | automatic_close_without_account_failure |
| `market_reopens` | 8 | 1 | EST (8) | string (8) | = (8) | 18:00 |
| `mixed_contract_conversion` | 8 | 1 | micro_per_mini (8) | null (8) | = (8) | (null) |
| `positions_flat_by` | 8 | 1 | EST (8) | string (8) | <= (8) | 16:45 |
| `reserve_eval_with_five_funded` | 8 | 1 | accounts (8) | number (8) | <= (8) | 5 |
| `restrictive_threshold` | 8 | 1 | enum (8) | string (8) | = (8) | MLL prevails if it trails above DLL |
| `automation_ea_bots` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `opposite_position_hedging` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `platform_outage_handling` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `dll_breach_consequence` | 6 | 1 | text (6) | null (6) | AS_STATED (6) | (null) |
| `drawdown_high_water_reference` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | highest balance at close of any preceding trading day (or initial capi… |
| `market_data_requires_cme_nonprofessional_attestation` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `max_drawdown_amount` | 6 | 1 | USD (6) | number (6) | EQ (6) | 2000 |
| `micro_mini_ratio` | 6 | 1 | ratio (6) | string (6) | EQ (6) | 10:1 |
| `mll_can_decrease` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `news_restriction` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | Tier1 new opening transactions restricted by symbol; closing TP/SL acc… |
| `news_tier1_window_mini_new_open_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `news_trading_allowed` | 6 | 1 | text (6) | object (6) | AS_STATED (6) | {"blanket_news_ban_stated":false,"tier1_restriction":"Topstep restrict… |
| `news_window_existing_position_equity_index` | 6 | 1 | boolean (6) | boolean (6) | AS_STATED (6) | true |
| `personal_dll_actions` | 6 | 1 | enum (6) | array (6) | AS_STATED (6) | ["Do Nothing","Liquidate","Liquidate and Block"] |
| `platform_switching_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `platforms_available` | 6 | 1 | enum (6) | array (6) | AS_STATED (6) | ["NinjaTrader","Tradovate","TradingView"] |
| `commission_round_trip_micro` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | number (5) | EQ (5) | 1.5 |
| `commission_round_trip_mini` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | number (5) | EQ (5) | 4.5 |
| `dll_reference` | 3 | 1 | text (3) | string (3) | AS_STATED (3) | balance at start of trading day − DLL; measured on equity; can rise or… |
| `automation_and_copiers` | 1 | 1 | enum (1) | boolean (1) | = (1) | true |
| `combined_account_limit` | 1 | 1 | accounts (1) | number (1) | <= (1) | 10 |
| `dca_scaling_entries` | 1 | 1 | enum (1) | boolean (1) | = (1) | true |
| `enforcement` | 1 | 1 | enum (1) | string (1) | = (1) | Manual review; confirmed bad faith warning; continuing activity profit… |
| `eod_trailing_drawdown` | 1 | 1 | USD (1) | null (1) | unresolved (1) | (null) |
| `flipping_for_trading_days` | 1 | 1 | enum (1) | boolean (1) | = (1) | true |
| `genuine_scalping` | 1 | 1 | enum (1) | boolean (1) | = (1) | true |
| `inactivity_consequence` | 1 | 1 | enum (1) | string (1) | = (1) | Permanent account deletion |
| `inactivity_qualifying_abs_net_pnl` | 1 | 1 | USD (1) | number (1) | >= (1) | 1 |
| `martingale` | 1 | 1 | enum (1) | string (1) | = (1) | Strongly discouraged, not explicitly banned here |
| `microscalping_flag_holding_time` | 1 | 1 | seconds (1) | number (1) | <= (1) | 5 |
| `microscalping_flag_profit_share` | 1 | 1 | ratio (1) | number (1) | > (1) | 0.5 |

### Stage `FUNDED;PAYOUT` - 941 records, 63 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `payout_minimum` | 32 | 1 | USD (32) | number (32) | GE (16), >= (16) | 500 |
| `mll_lock_on_payout_request` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | true |
| `intraday_payout_request_allowed` | 23 | 1 | boolean (23) | boolean (23) | EQ (23) | true |
| `intraday_payout_request_window` | 23 | 1 | time_window (23) | object (15), null (8) | within (15), UNKNOWN (8) | {"start":"18:00","end":"15:45","timezone_text":"ET","official_text":"6… |
| `payout_request_schedule` | 21 | 1 | enum (21) | null (21) | UNKNOWN (21) | (null) |
| `account_debit_basis` | 16 | 1 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `account_deduction_trigger` | 16 | 1 | enum (16) | string (16) | EQ (16) | AFTER_APPROVAL_WITHIN_MINUTES |
| `approval_time_limit` | 16 | 1 | hours (16) | null (16) | LE (16) | (null) |
| `buffer_balance` | 16 | 1 | USD (16) | number (16) | = (16) | 26100 |
| `cycle_profit_reset_anchor` | 16 | 1 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `cycle_profit_test` | 16 | 1 | USD (16) | number (16) | GT (16) | 0 |
| `denied_request_mll_reversal` | 16 | 1 | boolean (16) | null (16) | UNKNOWN (16) | (null) |
| `disbursement_business_days` | 16 | 1 | business_days (16) | number (16) | LE (16) | 2 |
| `funded_consistency_enabled` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | false |
| `intraday_payout_eligible_with_hedging_violation` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | false |
| `maximum_sim_payout_count` | 16 | 1 | count (16) | null (16) | = (16) | (null) |
| `minimum_profit_per_winning_day` | 16 | 1 | USD (16) | number (16) | GE (16) | 100 |
| `minimum_qualifying_profit_days` | 16 | 1 | days (16) | null (16) | = (16) | (null) |
| `minimum_trading_days` | 16 | 1 | days (16) | null (16) | = (16) | (null) |
| `mll_lock_trigger` | 16 | 1 | enum (16) | string (16) | EQ (16) | REQUEST_SUBMITTED |
| `payout_buffer_required` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | false |
| `payout_can_reduce_scaling` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | true |
| `payout_cap` | 16 | 1 | USD (16) | number (16) | LE (16) | 1000 |
| `payout_cycle_reset_event` | 16 | 1 | enum (16) | null (16) | = (16) | (null) |
| `payout_deduction_timing` | 16 | 1 | enum (16) | string (16) | = (16) | minutes after approval |
| `payout_denominator` | 16 | 1 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `payout_firm_share` | 16 | 1 | ratio (16) | number (16) | = (16) | 0.1 |
| `payout_fixed_cap` | 16 | 1 | USD (16) | null (16) | = (16) | (null) |
| `payout_fraction` | 16 | 1 | ratio (16) | number (16) | EQ (16) | 0.5 |
| `payout_frequency` | 16 | 1 | enum (16) | string (16) | = (16) | daily when eligible |
| `payout_maximum` | 16 | 1 | USD (16) | string (16) | <= (16) | current_balance - buffer_balance |
| `payout_net_profit_since_previous` | 16 | 1 | USD (16) | number (16) | > (16) | 0 |
| `payout_payment_timing` | 16 | 1 | business_days (16) | number (16) | <= (16) | 2 |
| `payout_preprocessing_risk` | 16 | 1 | enum (16) | string (16) | = (16) | balance entering buffer may cause denial |
| `payout_processor_fee` | 16 | 1 | USD (16) | null (16) | EQ (16) | (null) |
| `payout_request_edit_cancel_allowed` | 16 | 1 | boolean (16) | boolean (16) | = (16) | false |
| `payout_request_window` | 16 | 1 | enum (16) | string (16) | EQ (16) | ANY_DAY_IF_ELIGIBLE |
| `payout_requirements` | 16 | 1 | enum (16) | string (16) | = (16) | compliance with rules, terms, and Daily agreement |
| `payout_trader_share` | 16 | 1 | ratio (16) | number (16) | = (16) | 0.9 |
| `pending_balance_risk` | 16 | 1 | enum (16) | string (16) | EQ (16) | MAY_BE_DENIED_IF_BALANCE_TOO_LOW |
| `pending_days_attribution` | 16 | 1 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `protected_buffer_profit` | 16 | 1 | USD (16) | number (16) | = (16) | 1100 |
| `qualifying_winning_days` | 16 | 1 | distinct_session_count (16) | number (16) | GE (16) | 5 |
| `request_edit_or_cancel_allowed` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | false |
| `scaling_enabled` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | true |
| `scaling_mini_profit_0_999` | 16 | 1 | contracts (16) | number (16) | LE (16) | 1 |
| `scaling_mini_profit_1000_1999` | 16 | 1 | contracts (16) | number (16) | LE (16) | 2 |
| `scaling_unlisted_ranges` | 16 | 1 | enum (16) | null (16) | EQ (16) | (null) |
| `trader_profit_split` | 16 | 1 | ratio (16) | number (16) | EQ (16) | 0.9 |
| `winning_days_reset_trigger` | 16 | 1 | enum (16) | string (16) | EQ (16) | PAYOUT_APPROVED |
| `intraday_payout_profit_basis` | 15 | 1 | enum (15) | null (15) | UNKNOWN (15) | (null) |
| `post_intraday_payout_trading_state` | 15 | 1 | enum (15) | string (12), null (3) | EQ (12), UNKNOWN (3) | PAUSED_UNTIL_END_OF_TRADING_DAY |
| `scaling_mini_profit_2000_2999` | 12 | 1 | contracts (12) | number (12) | LE (12) | 4 |
| `multiple_intraday_payout_requests_per_session` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | true |
| `scaling_mini_profit_3000_4499` | 8 | 1 | contracts (8) | number (8) | LE (8) | 6 |
| `profit_removal_chargeback` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `termination_appeal_dispute` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `mll_lock_after_payout` | 6 | 1 | USD (6) | object (6) | EQ (6) | {"trigger":"first XFA payout (and each later payout)","mll_after_trigg… |
| `consistency_max_best_day_ratio_by_payout` | 4 | 1 | ratio (4) | object (4) | <= (4) | {"payout_1":0.2,"payout_2":0.25,"payout_3_plus":0.3} |
| `dll_amount_verified_card` | 4 | 1 | USD_PRESUMED_UNCONFIRMED (4) | null (4) | UNKNOWN (4) | (null) |
| `funded_consistency_max_best_day_ratio` | 4 | 1 | ratio (4) | null (4) | UNKNOWN (4) | (null) |
| `scaling_mini_profit_4500_plus` | 4 | 1 | contracts (4) | number (4) | LE (4) | 10 |
| `scaling_unlisted_ranges_assumption` | 4 | 1 | contracts (4) | object (4) | range lookup (4) | {"assumption_id":"LUCID_FLEX104_A","kind":"ASSUMPTION (a user statemen… |

### Stage `UNSPECIFIED` - 915 records, 58 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `unresolved__operations__appeal` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__operations__force_majeure` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__operations__ip` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `hedging_prohibited` | 30 | 2 | boolean (24), text (6) | boolean (24), string (6) | EQ (24), AS_STATED (6) | opposite/offsetting positions across accounts, operators, FTMO Group o… |
| `unresolved__operations__api` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__operations__cross_user_copy` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__operations__exchanges` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__operations__gambling_strategy` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__operations__inconsistent_strategy` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__operations__latency_arbitrage` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__operations__permitted_products` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `account_sharing_or_third_party_trading_prohibited` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | true |
| `bots_allowed_conditions` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | allowed if sole owner (provable, live video on request), not shared wi… |
| `expired_contract_trading_prohibited` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | true |
| `flat_by_time` | 24 | 1 | enum (24) | object (24) | AS_STATED (24) | {"regular_days":"close all positions by 4:45 PM ET (Mon-Fri)","holiday… |
| `good_faith_platform_error_exploitation_prohibited` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | true |
| `hft_prohibited` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | true |
| `kyt_interview_requirement` | 24 | 1 | text (24) | object (24) | AS_STATED (24) | {"what":"AI-conducted trader verification interview about your own tra… |
| `news_event_specific_restrictions` | 24 | 1 | text (24) | null (24) | none (24) | (null) |
| `news_trading_allowed` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | true |
| `residency_based_access` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | restricted by country of permanent residency, not physical location |
| `rule_change_effective` | 24 | 1 | text (24) | string (24) | AS_STATED (24) | effective upon posting (Agreement and Terms of Use) |
| `trading_style_dca_flipping` | 24 | 1 | text (24) | null (24) | AS_STATED (24) | (null) |
| `unresolved__operations__same_name_copy` | 24 | 1 | enum (24) | null (24) | UNKNOWN (24) | (null) |
| `vps_vm_location_obscuring_prohibited` | 24 | 1 | boolean (24) | boolean (24) | EQ (24) | true |
| `approved_symbols_commission` | 14 | 1 | per side / contract; source currency not expressly labeled (14) | array (14) | = (14) | ["ES","NQ","RTY","NKD"] |
| `unresolved__operations__cross_firm_copy` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__operations__genuine_scalping` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__operations__payout_denial` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__operations__platform_failure` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `unresolved__operations__rule_change_notice` | 12 | 2 | enum (12) | null (12) | UNKNOWN (12) | (null) |
| `account_merging_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `automation` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | automated trading permitted; HFT, latency arbitrage and manipulative/a… |
| `copy_trading` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | copying a third party prohibited; copying across own accounts allowed … |
| `exchanges` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | major CME Group exchanges |
| `exploit_errors_prohibited` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `flat_by_end_of_trading_day` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `live_market_consistency` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | no overleveraging, one-sided bets, account rolling; avoid inconsistent… |
| `manual_contract_rolling_required` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `no_new_positions_near_cme_price_limit` | 6 | 1 | ratio (6) | number (6) | < (6) | 0.02 |
| `order_rate_api_limit_value` | 6 | 1 | text (6) | null (6) | AS_STATED (6) | (null) |
| `permitted_instruments` | 6 | 1 | enum (6) | object (6) | AS_STATED (6) | {"mini":["GC","SI","HG","PL","CL","NG","NQ","ES","YM","RTY","NKD","6E"… |
| `simulated_commissions_apply` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `third_party_access_prohibited` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `unresolved__operations__account_sharing` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__bot` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__disputes` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__ea` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__geography` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__hft` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__opposing_positions` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__profit_removal` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__refund` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__termination` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `unresolved__operations__trading_hours` | 6 | 1 | enum (6) | null (6) | UNKNOWN (6) | (null) |
| `violation_consequences` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | trade removal, account termination, forfeiture of rewards, permanent r… |
| `vpn_vps_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `approved_product_listing_status` | 1 | 1 | enum (1) | string (1) | EQ (1) | NOT_LISTED |

### Stage `SCOPE` - 625 records, 58 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `unresolved_full_required_coverage` | 48 | 1 | enum (48) | null (48) | AS_STATED (48) | (null) |
| `account_access_sharing` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `account_cohort_verified` | 19 | 2 | enum (9), boolean (5), unknown (5) | null (19) | UNKNOWN (14), EQ (5) | (null) |
| `dispute_process` | 19 | 2 | enum (9), text (5), unknown (5) | null (14), string (5) | UNKNOWN (14), EQ (5) | individual arbitration/class-action waiver; Florida jurisdiction; enfo… |
| `force_majeure` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `hft` | 19 | 2 | unknown (10), enum (9) | null (10), string (9) | UNKNOWN (10), prohibited (9) | prohibited |
| `latency_arbitrage` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `profit_removal` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `third_party_management` | 19 | 2 | unknown (10), enum (9) | null (19) | UNKNOWN (19) | (null) |
| `consistency_option_effective_date` | 16 | 1 | date (16) | null (16) | UNKNOWN (16) | (null) |
| `approved_exchanges` | 10 | 1 | array (5), unknown (5) | array (5), null (5) | EQ (5), UNKNOWN (5) | ["CME","CBOT","NYMEX","COMEX"] |
| `approved_products` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `copy_trading_cross_firm` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `copy_trading_other_users` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | = (5), UNKNOWN (5) | false |
| `copy_trading_same_owner` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | = (5), UNKNOWN (5) | true |
| `ea_bot_api_scope` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `gambling_inconsistent_strategy` | 10 | 1 | text (10) | string (10) | EQ (10) | Risk assessed over patterns; maximum sizing, repeated loss-limit breac… |
| `genuine_scalping` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `hedging_accounts` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `ip_vpn_geographic` | 10 | 1 | text (10) | string (10) | EQ (10) | Restricted-country access including market-data viewing and VPN/remote… |
| `payout_denial_policy` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `platform_fault_policy` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `rule_change_notice_required` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | false |
| `simulation_exploitation` | 10 | 1 | text (10) | string (10) | EQ (10) | Deliberate sim-only exploitation can lead to funding relationship term… |
| `account_agreement_verified` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `api` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `appeal` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `bot` | 9 | 1 | enum (9) | string (9) | prohibited (9) | prohibited |
| `cross_firm_copy` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `cross_user_copy` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `data_outage` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `denied_payout` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `ea` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `exchanges` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `gambling` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `geographic_restrictions` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `hedging` | 9 | 1 | enum (9) | string (9) | AS_STATED (9) | permitted_within_single_account_only |
| `inconsistent_strategy` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `instruments` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `interaccount_hedging` | 9 | 1 | enum (9) | string (9) | prohibited (9) | prohibited |
| `ip` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `opposing_positions` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `own_account_copy` | 9 | 1 | boolean (9) | boolean (9) | = (9) | true |
| `platform_outage` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `refund` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `rule_change_notice` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `scalping` | 9 | 1 | ratio (9) | number (9) | >= (9) | 0.5 |
| `termination` | 9 | 1 | enum (9) | string (9) | AS_STATED (9) | termination_from_program_and_refund_of_fee_of_breaching_account |
| `trading_hours` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `vpn` | 9 | 1 | enum (9) | null (9) | UNKNOWN (9) | (null) |
| `approved_trade_copiers` | 5 | 1 | array (5) | array (5) | AS_STATED (5) | ["Tradesyncer","TradeCopia","Affordable Indicators","Replikanto Flowbo… |
| `counter_positions_prohibited` | 5 | 1 | unknown (5) | null (5) | UNKNOWN (5) | (null) |
| `direct_evaluation_stage` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `prohibited_trade_copier_uses` | 5 | 1 | array (5) | array (5) | AS_STATED (5) | ["copy or synchronize trades between different users or identities","c… |
| `trade_copier_enforcement` | 5 | 1 | array (5) | array (5) | AS_STATED (5) | ["profit forfeiture","account reset or liquidation","account closure",… |
| `trade_copier_responsibility` | 5 | 1 | text (5) | string (5) | EQ (5) | trader responsible for configuration and copied activity; not permissi… |
| `legacy_scope_guard` | 4 | 1 | enum (4) | string (4) | AS_STATED (4) | Do not import six-payout / escrow legacy transition for a new purchase |
| `public_size_family_catalogue` | 1 | 1 | object (1) | object (1) | AS_STATED (1) | {"Zero Starter":[25000,50000,100000,150000],"Zero Max":[25000,50000,10… |

### Stage `RE_ENTRY` - 552 records, 29 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `cooldown` | 48 | 1 | weeks (48) | number (48) | = (48) | 2 |
| `unresolved__re_entry__eligibility` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__re_entry__fee` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__re_entry__refund` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__re_entry__same_payout_rules` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__re_entry__same_size` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__re_entry__tax` | 36 | 3 | enum (36) | null (36) | UNKNOWN (36) | (null) |
| `unresolved__re_entry__deadline` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__re_entry__dll_discount` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__re_entry__max_reactivations` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__re_entry__ready_time` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `unresolved__re_entry__reset_tuple` | 30 | 2 | enum (30) | null (30) | UNKNOWN (30) | (null) |
| `appeal_process` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `live_direct_reset_allowed` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | false |
| `live_negative_balance_offset` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | deduct negative ending live balance from frozen PRO profits; remainder… |
| `live_reentry_path` | 10 | 1 | array (5), unknown (5) | array (5), null (5) | EQ (5), UNKNOWN (5) | ["pass evaluation","reset existing PRO then upgrade"] |
| `pro_disabled_reset_allowed` | 10 | 1 | boolean (5), unknown (5) | boolean (5), null (5) | EQ (5), UNKNOWN (5) | false |
| `pro_reset_fee` | 10 | 1 | DOLLAR_SYMBOL_ONLY (5), unknown (5) | number (5), null (5) | EQ (5), UNKNOWN (5) | 449 |
| `pro_resets` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `reentry_cooldown` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `termination_discretion` | 10 | 1 | text (5), unknown (5) | string (5), null (5) | EQ (5), UNKNOWN (5) | may suspend/terminate with or without notice |
| `termination_refund` | 10 | 1 | unknown (10) | null (10) | UNKNOWN (10) | (null) |
| `dll_reactivation_discount` | 6 | 1 | USD (6) | number (6) | EQ (6) | 50 |
| `reactivation_ready_event` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | next trading session after purchase |
| `reset_restores` | 6 | 1 | enum (6) | object (6) | AS_STATED (6) | {"balance":0,"pnl":0,"winning_days":0,"trade_history":"reset"} |
| `cooldown_duration` | 5 | 1 | calendar_days (5) | number (5) | EQ (5) | 30 |
| `cooldown_restrictions` | 5 | 1 | array (5) | array (5) | EQ (5) | ["new subscriptions","test resets","PRO resets","receive Standard PRO+… |
| `cooldown_resume` | 5 | 1 | text (5) | string (5) | EQ (5) | after30 days subject to risk-team review |
| `cooldown_retained_permissions` | 5 | 1 | array (5) | array (5) | EQ (5) | ["trade existing Test/PRO/PRO+","wallet withdrawals","passed test acti… |

### Stage `EVALUATION;SIM_FUNDED` - 312 records, 17 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `algo_bot_policy` | 20 | 1 | N/A (20) | null (20) | unresolved (20) | (null) |
| `allowed_products` | 20 | 1 | text (20) | null (20) | EQ (20) | (null) |
| `commission_es_per_side_usd` | 20 | 1 | USD (20) | number (20) | EQ (20) | 2.09 |
| `commission_mes_per_side_usd` | 20 | 1 | USD (20) | number (20) | EQ (20) | 0.61 |
| `copy_trading_policy` | 20 | 1 | N/A (20) | null (20) | unresolved (20) | (null) |
| `flat_by_time` | 20 | 1 | text (20) | string (20) | EQ (20) | 15:59 CT |
| `hedging_policy` | 20 | 1 | N/A (20) | null (20) | UNKNOWN (20) | (null) |
| `inactivity_rule` | 20 | 1 | text (20) | null (20) | EQ (20) | (null) |
| `max_master_accounts` | 20 | 1 | count (20) | number (20) | <= (20) | 5 |
| `news_trading` | 20 | 1 | text (20) | string (20) | EQ (20) | allowed; no blackout windows |
| `opposite_positions_across_master_accounts` | 20 | 1 | text (20) | string (20) | AS_STATED (20) | positions on the same instrument across all Master accounts may be hel… |
| `overnight_hold_rule` | 20 | 1 | text (20) | string (20) | EQ (20) | not allowed; Micro Account 10,000 may carry trades overnight except we… |
| `position_open_window` | 20 | 1 | text (20) | string (20) | EQ (20) | 17:00-15:59 CT |
| `trading_day_window` | 20 | 1 | text (20) | string (20) | EQ (20) | 17:00-16:00 CT next day |
| `weekends_holidays` | 20 | 1 | text (20) | string (20) | EQ (20) | do not count as active trading days |
| `scaling_plan` | 6 | 1 | text (6) | string (6) | EQ (6) | contract size scales up as cash on hand grows |
| `scaling_plan_steps` | 6 | 1 | contracts (6) | object (4), null (2) | AS_STATED (4), UNKNOWN (2) | {"cash_on_hand_tiers":[{"cash_on_hand_min_usd":0,"cash_on_hand_max_usd… |

### Stage `EVALUATION;FUNDED;PAYOUT` - 169 records, 13 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `dll_enabled` | 16 | 1 | boolean (16) | boolean (16) | EQ (16) | true |
| `initial_trail_balance` | 16 | 1 | USD (16) | number (16) | GT_TEXT (16) | 26100 |
| `locked_mll_balance` | 16 | 1 | USD (16) | number (16) | EQ (16) | 25100 |
| `max_micro_contracts` | 16 | 1 | contracts (16) | number (16) | LE (16) | 20 |
| `max_mini_contracts` | 16 | 1 | contracts (16) | number (16) | LE (16) | 2 |
| `mixed_contract_conversion` | 16 | 1 | formula (16) | null (16) | UNKNOWN (16) | (null) |
| `mll_amount` | 16 | 1 | USD (16) | number (16) | EQ (16) | 1000 |
| `threshold_pnl_fee_basis` | 16 | 1 | enum (16) | null (16) | UNKNOWN (16) | (null) |
| `touch_is_breach` | 16 | 1 | boolean (16) | boolean (16) | LE (16) | true |
| `dll_breach_outcome` | 8 | 1 | enum (8) | string (8) | EQ (8) | LOCKED_UNTIL_NEXT_SESSION |
| `rule_change_notice` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `trading_day_definition` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | 6:00 p.m. ET to 4:10 p.m. ET next calendar day |
| `dll_amount_verified_card` | 4 | 1 | USD_PRESUMED_UNCONFIRMED (4) | number (4) | EQ (4) | 600 |

### Stage `SIM_FUNDED` - 162 records, 12 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `master_dd_stops_at_initial_balance` | 20 | 1 | boolean (20) | null (20) | EQ (20) | (null) |
| `master_drawdown_same_as_eval` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | true |
| `master_multi_account_unlock_sequence` | 20 | 1 | text (20) | null (20) | AS_STATED (20) | (null) |
| `master_not_live_capital` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | true |
| `master_reset_fee` | 20 | 1 | USD (20) | null (20) | unknown (20) | (null) |
| `no_monthly_fee_master` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | true |
| `livesim_activation_fee_nonpro_one_time` | 7 | 1 | USD (7) | number (7) | EQ (7) | 139 |
| `livesim_data_fee_professional` | 7 | 1 | USD (7) | object (7) | EQ (7) | {"rithmic_per_exchange_month": 140, "ninjatrader_per_exchange_month": … |
| `livesim_drawdown` | 7 | 1 | text (7) | string (7) | EQ (7) | EOD_same_as_evaluation |
| `livesim_first_withdrawal_minimum_profit` | 7 | 1 | USD (7) | number (7) | GTE (7) | 239 |
| `livesim_is_optional_bridge` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | true |
| `livesim_max_withdrawal_before_auto_live` | 7 | 1 | USD (7) | object (7) | EQ (7) | {"TCP25":1750,"TCP50":3000,"TCP100":6000,"GM50":5000,"GM100":5000,"GM1… |

### Stage `TERMINATION` - 125 records, 7 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `account_closure_reentry` | 20 | 1 | text (20) | null (20) | unknown (20) | (null) |
| `rule_change_notice_disputes` | 20 | 1 | text (20) | null (20) | unknown (20) | (null) |
| `termination_on_fraud` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | true |
| `termination_on_violation` | 20 | 1 | boolean (20) | boolean (20) | EQ (20) | true |
| `dispute_process` | 15 | 1 | text (15) | null (15) | UNKNOWN (15) | (null) |
| `rule_breach_consequence` | 15 | 1 | text (15) | string (15) | EQ (15) | termination_risk |
| `rule_change_notification` | 15 | 1 | text (15) | null (15) | UNKNOWN (15) | (null) |

### Stage `PURCHASE;ACTIVATION` - 124 records, 8 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `advertised_activation_fee` | 36 | 1 | USD_PRESUMED_UNCONFIRMED (36) | number (36) | EQ (36) | 0 |
| `activation_fee_usd` | 18 | 1 | USD (18) | number (18) | EQ (18) | 0 |
| `data_fee_usd` | 18 | 1 | USD (18) | null (18) | unresolved (18) | (null) |
| `platform_fee_usd` | 18 | 1 | USD (18) | null (18) | unresolved (18) | (null) |
| `activation_fee` | 16 | 1 | USD (16) | number (16) | = (16) | 0 |
| `pa_activation_fee_amount` | 16 | 1 | USD (16) | number (16) | EQ (16) | 109 |
| `funded_activation_monthly` | 1 | 1 | USD (1) | number (1) | EQ (1) | 87 |
| `funded_activation_onetime` | 1 | 1 | USD (1) | number (1) | EQ (1) | 247 |

### Stage `ALL` - 100 records, 27 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `ip_vpn_geo` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `platform_failure` | 15 | 1 | enum (15) | null (15) | unknown (15) | (null) |
| `breach_effect_account_failed` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `inactivity_30d_disable` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `tos_violation_ban` | 14 | 1 | boolean (14) | boolean (14) | EQ (14) | true |
| `account_limit` | 4 | 1 | accounts (4) | number (4) | <= (4) | 5 |
| `dll` | 4 | 1 | USD (4) | null (4) | none (4) | (null) |
| `account_access_sharing` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `account_performance_transfer_or_combine` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `cqg_platforms` | 1 | 1 | enum (1) | array (1) | = (1) | ["NinjaTrader","Tradovate","TradingView"] |
| `first_detected_hedge` | 1 | 1 | enum (1) | string (1) | = (1) | Email notice; reset involved accounts to prior-day balance |
| `hedge_reset_remaining_drawdown_effect` | 1 | 1 | enum (1) | string (1) | EQ (1) | TOTAL_REMAINING_DRAWDOWN_NOT_RESET |
| `hft` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `hft_enforcement` | 1 | 1 | enum (1) | string (1) | = (1) | Warning first; repeat profits removed, accounts closed, permanent rest… |
| `in_concert_pool_or_hedge_aggregate_risk` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `in_concert_trades_to_manipulate_or_gain_unfair_advantage` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `opposing_correlated_positions_across_accounts` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `opposing_different_contracts` | 1 | 1 | enum (1) | boolean (1) | = (1) | true |
| `opposing_mini_and_micro_same_contract` | 1 | 1 | enum (1) | boolean (1) | = (1) | true |
| `profit_confiscation_on_prohibited_practice` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `repeat_hedge` | 1 | 1 | enum (1) | string (1) | = (1) | Breach involved accounts; possible permanent restriction |
| `rithmic_platforms` | 1 | 1 | enum (1) | array (1) | = (1) | ["MotiveWave","Quantower","Tradesea","Sierra Chart","Jigsaw","Bookmap"… |
| `same_contract_opposing_positions` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `simulation_exploitation` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `termination_on_breach` | 1 | 1 | boolean (1) | boolean (1) | EQ (1) | true |
| `trading_on_behalf_of_others` | 1 | 1 | enum (1) | boolean (1) | prohibited (1) | false |
| `website_account_limit` | 1 | 1 | accounts (1) | number (1) | <= (1) | 1 |

### Stage `LIVE;PRE_LIVE` - 96 records, 2 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `exchange_scaling_rows` | 48 | 1 | USD and contracts (48) | array (48) | range lookup (48) | [[0,1999.99,1,10,1,10,1,10,0,5],[2000,null,2,20,2,20,2,20,1,10]] |
| `scaling_update` | 48 | 1 | enum (48) | string (48) | = (48) | End of each trading day; moves both up and down |

### Stage `SIM_FUNDED;LIVE` - 79 records, 13 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `funded_blow_consequence` | 7 | 1 | text (7) | string (7) | EQ (7) | auto_closed_terminated |
| `funded_daily_loss_limit` | 7 | 1 | text (7) | string (7) | EQ (7) | applies_but_removable |
| `hedging_between_funded_accounts` | 7 | 1 | text (7) | string (7) | EQ (7) | strictly_forbidden_termination |
| `max_funded_accounts` | 7 | 1 | count (7) | number (7) | LTE (7) | 3 |
| `no_buffer_requirement` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | true |
| `no_consistency_requirement_when_funded` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | true |
| `no_min_trading_days_to_withdraw` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | true |
| `no_subscription_fee_when_funded` | 7 | 1 | boolean (7) | boolean (7) | EQ (7) | true |
| `trade_copiers` | 7 | 1 | text (7) | string (7) | EQ (7) | forbidden_all_programs |
| `unscheduled_absence_rule` | 7 | 1 | text (7) | string (7) | EQ (7) | 5_consecutive_trading_days_termination |
| `capital_progression_ladder` | 3 | 1 | text (3) | array (3) | EQ (3) | [{"tier": "Evaluation $25K", "goal": 1750, "drawdown": 1500, "dd_type"… |
| `tcp_max_scale_by_track` | 3 | 1 | USD (3) | object (3) | EQ (3) | {"TCP25": "$200,000", "TCP50": "$400,000", "TCP100": "$400,000"} |
| `tcp_withdraw_full_profit_to_upgrade` | 3 | 1 | boolean (3) | boolean (3) | EQ (3) | true |

### Stage `EVALUATION;ACTIVATION` - 72 records, 6 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `activation_deadline` | 16 | 1 | days (16) | null (16) | = (16) | (null) |
| `activation_latency_max` | 16 | 1 | minutes (16) | number (16) | <= (16) | 30 |
| `activation_latency_min` | 16 | 1 | minutes (16) | number (16) | >= (16) | 5 |
| `activation_fee` | 8 | 1 | USD (8) | number (8) | = (8) | 0 |
| `upgrade_latency_max` | 8 | 1 | minutes (8) | number (8) | <= (8) | 30 |
| `upgrade_latency_min` | 8 | 1 | minutes (8) | number (8) | >= (8) | 5 |

### Stage `LIVE_REVIEW;LIVE` - 46 records, 4 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `live_starting_balance` | 24 | 1 | USD (24) | number (24) | EQ (24) | 0 |
| `live_sim_coexistence` | 8 | 1 | boolean (8) | boolean (8) | AS_STATED (8) | false |
| `live_new_agreement` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |
| `live_split_frequency` | 7 | 1 | text (7) | null (7) | unknown (7) | (null) |

### Stage `EVALUATION;FUNDED;LIVE` - 41 records, 7 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `commission_cost_rt_micros` | 6 | 1 | USD (6) | number (6) | EQ (6) | 1.22 |
| `commission_cost_rt_minis` | 6 | 1 | USD (6) | number (6) | EQ (6) | 3.78 |
| `cross_account_hedging_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `single_profile_policy` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `third_party_account_operation_allowed` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | false |
| `vpn_prohibited` | 6 | 1 | boolean (6) | boolean (6) | EQ (6) | true |
| `counter_positions_prohibited` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | true |

### Stage `UNSPECIFIED_SIM_SCOPE` - 40 records, 5 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `breached_eval_reset_deadline` | 8 | 1 | days (8) | number (8) | before_expiry (8) | 30 |
| `funded_reset_available` | 8 | 1 | boolean (8) | null (8) | unknown (8) | (null) |
| `mll_lowering_after_payout` | 8 | 1 | boolean (8) | boolean (8) | = (8) | false |
| `pro_agreement_automated_software_prior_approval` | 8 | 1 | boolean (8) | boolean (8) | AS_STATED (8) | true |
| `pro_agreement_prohibited_conduct_listed` | 8 | 1 | enum (8) | array (8) | AS_STATED (8) | ["microscalping","hedging","high frequency trading","trading on behalf… |

### Stage `RESET` - 26 records, 4 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `reset_product_exists` | 15 | 1 | boolean (15) | null (11), boolean (4) | EQ (15) | false |
| `reset_changes_renewal_date` | 5 | 1 | boolean (5) | boolean (5) | EQ (5) | false |
| `reset_fee` | 5 | 1 | DOLLAR_SYMBOL_ONLY (5) | number (5) | EQ (5) | 79 |
| `reset` | 1 | 1 | enum (1) | string (1) | = (1) | Paid dashboard reset; restores initial conditions |

### Stage `PURCHASE;EVALUATION` - 24 records, 2 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `consistency_option_choices` | 16 | 1 | enum (16) | array (16) | AS_STATED (16) | ["40_PERCENT_STANDARD","50_PERCENT_ADDON"] |
| `eval_reset_available` | 8 | 1 | boolean (8) | boolean (8) | EQ (8) | false |

### Stage `UNSPECIFIED;PAYOUT` - 24 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `microscalping_payout_condition` | 24 | 1 | enum (24) | object (24) | AS_STATED (24) | {"applies_to":"funded accounts only (not evaluation)","both_required":… |

### Stage `PURCHASE;EVALUATION;ACTIVATION` - 16 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `activation_fee` | 16 | 1 | USD (16) | number (16) | EQ (16) | 0 |

### Stage `PAYOUT;LIVE_REVIEW` - 16 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `current_max_payout_level` | 16 | 1 | payouts (16) | number (16) | LE (16) | 5 |

### Stage `PRE_LIVE` - 16 records, 4 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `breach_cooldown` | 4 | 1 | days (4) | number (4) | = (4) | 0 |
| `consistency` | 4 | 1 | ratio (4) | null (4) | none (4) | (null) |
| `profit_target` | 4 | 1 | USD (4) | number (4) | >= (4) | 1000 |
| `scaling_plan` | 4 | 1 | enum (4) | string (4) | = (4) | Standard Live scaling |

### Stage `UNSPECIFIED_ON_SHARED_PAGE` - 16 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `red_folder_news` | 16 | 1 | enum (16) | string (16) | = (16) | Hard breach |

### Stage `FUNDED;RESET` - 16 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `funded_reset_available` | 16 | 1 | boolean (16) | null (16) | unknown (16) | (null) |

### Stage `EVALUATION;SIM_FUNDED;LIVE` - 14 records, 2 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `prohibited_conduct_consequences` | 7 | 1 | text (7) | array (7) | potential (7) | ["warning","delete_trading_data_of_affected_day","account_reset","perm… |
| `prohibited_conduct_list` | 7 | 1 | text (7) | array (7) | EQ (7) | ["exploit_platform_errors_or_price_display_or_update_delays","disrupti… |

### Stage `EVALUATION;FUNDED;ACTIVATION` - 14 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `funded_activation_state_tuple` | 14 | 1 | enum (8), state_tuple (6) | null (14) | UNKNOWN (14) | (null) |

### Stage `PURCHASE;RESET` - 14 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `reset_fee_usd` | 14 | 1 | USD (14) | null (14) | unresolved (14) | (null) |

### Stage `LIVE;PAYOUT` - 12 records, 3 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `payout_cadence` | 4 | 1 | enum (4) | string (4) | = (4) | Daily; no cap/window |
| `trader_profit_split` | 4 | 1 | ratio (4) | number (4) | = (4) | 0.9 |
| `withdrawable_starting_balance_day` | 4 | 1 | day (4) | number (4) | = (4) | 1 |

### Stage `PAYOUT;RE_ENTRY` - 8 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `payout_limit_consequence` | 8 | 1 | text (8) | string (8) | AS_STATED (8) | PA closes after sixth approved payout; another evaluation needed for n… |

### Stage `EVALUATION;PRE_LIVE` - 8 records, 2 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `eod_drawdown` | 4 | 1 | USD (4) | number (4) | = (4) | 1000 |
| `existing_accounts_trade_and_reset_while_live` | 4 | 1 | enum (4) | boolean (4) | = (4) | true |

### Stage `EVALUATION;RESET` - 6 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `reset_purchase_limit` | 6 | 1 | count (6) | null (6) | AS_STATED (6) | (null) |

### Stage `PAYOUT;LIVE` - 6 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `pending_trading_guidance` | 6 | 1 | text (6) | string (6) | AS_STATED (6) | pause trading until fully processed and deducted |

### Stage `KYC;PAYOUT` - 3 records, 3 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `provider_verification` | 1 | 1 | enum (1) | string (1) | = (1) | WorkMarket Support review required before transfer |
| `verification_destination` | 1 | 1 | enum (1) | string (1) | = (1) | compliance@lucidtrading.com |
| `verification_documents` | 1 | 1 | enum (1) | array (1) | = (1) | ["Incorporation","Ownership","Government photo ID for each owner >=25%… |

### Stage `FUNDED;LIVE` - 1 records, 1 metrics

| metric | records | firms | unit | value_type | operator | example value |
|---|---|---|---|---|---|---|
| `activity_location` | 1 | 1 | enum (1) | string (1) | = (1) | Outside United States |

## 2. Fields and observed values

### 2.1 Rule record fields

| field | present in records | meaning |
|---|---|---|
| `record_id` | 26,505 | name is self-explanatory; see README_DATA.md |
| `plan_id` | 26,505 | name is self-explanatory; see README_DATA.md |
| `product` | 26,505 | meaning not documented in the data |
| `account_size` | 26,505 | meaning not documented in the data |
| `dll_option` | 26,505 | meaning not documented in the data |
| `eval_drawdown` | 26,505 | meaning not documented in the data |
| `funded_drawdown` | 26,505 | meaning not documented in the data |
| `stage` | 26,505 | meaning not documented in the data |
| `metric` | 26,505 | name is self-explanatory; see README_DATA.md |
| `value` | 26,505 | name is self-explanatory; see README_DATA.md |
| `value_type` | 26,505 | meaning not documented in the data |
| `value_state` | 26,505 | name is self-explanatory; see README_DATA.md |
| `unit` | 26,505 | meaning not documented in the data |
| `operator` | 26,505 | meaning not documented in the data |
| `rule_event` | 26,505 | meaning not documented in the data |
| `version` | 26,505 | meaning not documented in the data |
| `cohort` | 26,505 | meaning not documented in the data |
| `availability` | 26,505 | meaning not documented in the data |
| `applicability` | 26,505 | meaning not documented in the data |
| `notes` | 26,505 | meaning not documented in the data |
| `original_value` | 26,505 | meaning not documented in the data |
| `original_unit` | 26,505 | meaning not documented in the data |
| `original_value_type` | 26,505 | meaning not documented in the data |
| `original_value_present` | 26,505 | meaning not documented in the data |
| `canonical_plan_ids` | 26,505 | meaning not documented in the data |
| `sources` | 26,505 | name is self-explanatory; see README_DATA.md |
| `source_urls` | 26,505 | name is self-explanatory; see README_DATA.md |
| `checked_at` | 26,505 | name is self-explanatory; see README_DATA.md |
| `source_missing` | 26,505 | meaning not documented in the data |
| `checked_at_missing` | 26,505 | meaning not documented in the data |
| `source_locator` | 26,505 | meaning not documented in the data |
| `source_as_of` | 26,505 | meaning not documented in the data |

### 2.2 Plan fields

| field | present in plans |
|---|---|
| `plan_id` | 186 |
| `product` | 186 |
| `account_size` | 186 |
| `dll_option` | 186 |
| `eval_drawdown` | 186 |
| `funded_drawdown` | 186 |
| `availability` | 186 |
| `cohort` | 186 |
| `version` | 186 |
| `model_id` | 186 |
| `plan_notes` | 186 |
| `plan_record` | 186 |
| `current_price_snapshot` | 186 |
| `price_snapshot_missing` | 186 |
| `superseded_snapshots` | 186 |
| `free_tier` | 186 |

### 2.3 Enumerated fields: observed distinct values with counts

Counts are rule records unless the column says plans. Meaning of every value: meaning not documented in the data (except `value_state`, see README_DATA.md).

#### rules.eval_drawdown - 12 distinct values

| value | count |
|---|---|
| `EOD` | 17,468 |
| `INTRADAY` | 2,141 |
| `TRAILING_LOCK_AT_START` | 1,595 |
| `N/A` | 1,174 |
| `RISK_MODEL_OPTION_DEPENDENT` | 828 |
| `NOT_APPLICABLE` | 720 |
| `TRAILING_INTRADAY` | 582 |
| `TRAILING_EOD` | 578 |
| `EOD_TRAILING` | 529 |
| `STATIC` | 495 |
| `LIVE_TRAILING` | 281 |
| `(null)` | 114 |

#### rules.funded_drawdown - 12 distinct values

| value | count |
|---|---|
| `EOD` | 15,432 |
| `INTRADAY` | 4,972 |
| `TRAILING_LOCK_AT_START` | 1,595 |
| `EOD_LIVESIM;TRAILING_LIVE` | 947 |
| `RISK_MODEL_OPTION_DEPENDENT` | 828 |
| `TRAILING_INTRADAY` | 582 |
| `TRAILING_EOD` | 578 |
| `EOD_TRAILING` | 529 |
| `STATIC` | 495 |
| `LIVE_TRAILING` | 281 |
| `N/A_PRELIVE` | 152 |
| `(null)` | 114 |

#### rules.dll_option - 14 distinct values

| value | count |
|---|---|
| `ON` | 4,833 |
| `(null)` | 4,476 |
| `UNCONFIRMED` | 3,580 |
| `NONE` | 3,556 |
| `OFF` | 2,726 |
| `FUNDED_ONLY` | 2,243 |
| `UNKNOWN` | 2,099 |
| `RISK_MODEL_OPTION_DEPENDENT` | 828 |
| `SOFT_BREACH` | 770 |
| `FIXED_DAILY` | 578 |
| `FIXED_THEN_LUCIDSCALE` | 306 |
| `HARD_BREACH` | 281 |
| `SOFT_PAUSE` | 214 |
| `NOT_STATED` | 15 |

#### rules.operator - 33 distinct values

| value | count |
|---|---|
| `EQ` | 7,923 |
| `UNKNOWN` | 7,096 |
| `=` | 2,858 |
| `AS_STATED` | 2,773 |
| `unknown` | 1,381 |
| `unresolved` | 1,165 |
| `<=` | 915 |
| `>=` | 912 |
| `GE` | 325 |
| `LE` | 276 |
| `none` | 176 |
| `prohibited` | 129 |
| `within` | 60 |
| `>` | 59 |
| `range lookup` | 58 |
| `N/A` | 46 |
| `RANGE` | 46 |
| `at` | 40 |
| `<` | 36 |
| `GTE` | 35 |
| `GT` | 31 |
| `>= loss triggers` | 30 |
| `by` | 30 |
| `LTE` | 28 |
| `before_expiry` | 17 |
| `GT_TEXT` | 16 |
| `potential` | 11 |
| `TOUCH_OR_BELOW` | 7 |
| `TOUCH` | 7 |
| `LT` | 7 |
| `below` | 6 |
| `EOD_close >` | 4 |
| `excluded` | 2 |

#### rules.rule_event - 146 distinct values

| value | count |
|---|---|
| `AS_STATED` | 16,024 |
| `at_purchase` | 1,577 |
| `during_evaluation` | 1,361 |
| `at_payout` | 593 |
| `during_funded` | 562 |
| `at_activation` | 326 |
| `at_payout_request` | 306 |
| `payout_request` | 279 |
| `during_trading` | 260 |
| `always` | 256 |
| `when_funded` | 255 |
| `PUBLIC_CONFIGURATOR_OBSERVATION` | 253 |
| `during_live` | 243 |
| `at_live` | 235 |
| `checkout` | 226 |
| `before_purchase` | 200 |
| `before_payout` | 158 |
| `at_withdrawal` | 146 |
| `at_checkout` | 135 |
| `on_breach` | 116 |
| `after_payout` | 94 |
| `after_approval` | 91 |
| `at_reset` | 83 |
| `pass_evaluation` | 78 |
| `at_signup` | 75 |
| `per_payout_cycle` | 73 |
| `next_session_tier` | 64 |
| `after_pass_review` | 60 |
| `during_master` | 60 |
| `at_termination` | 60 |
| `SESSION_END` | 60 |
| `n/a` | 60 |
| `per_completed_round_turn` | 60 |
| `per_trade` | 56 |
| `on_approval` | 53 |
| `pending_payout` | 48 |
| `during_news` | 45 |
| `at_pass_check` | 44 |
| `advertised_on_site_banner` | 44 |
| `cumulative` | 42 |
| `on_request` | 42 |
| `at_pass` | 39 |
| `at_account_setup` | 35 |
| `at_funding` | 35 |
| `before_use` | 32 |
| `payout_disbursement` | 32 |
| `account_deduction` | 32 |
| `MOVE_TO_LIVE_EMAIL_RECEIVED` | 32 |
| `CASHOUT_CHOICE_WINDOW_EXPIRES` | 32 |
| `after_payment` | 30 |
| `after_purchase` | 30 |
| `per_reward_cycle` | 30 |
| `at_payout_approval` | 30 |
| `reset_purchase` | 30 |
| `at_rebill` | 29 |
| `intraday` | 29 |
| `on_order` | 29 |
| `at_live_transition` | 29 |
| `ongoing` | 28 |
| `each_calendar_week` | 28 |
| `rolling_30d` | 28 |
| `SESSION_LOSS` | 28 |
| `LIVE_TRANSITION` | 28 |
| `on_news_event` | 25 |
| `after_breach` | 24 |
| `at_page_read` | 24 |
| `after_xfa_loss` | 24 |
| `tier1_news_release` | 24 |
| `advertised_on_plan_card` | 22 |
| `session_close` | 20 |
| `after_activation` | 20 |
| `after_payouts` | 20 |
| `after_master_breach` | 20 |
| `on_trigger` | 20 |
| `on_cancel` | 20 |
| `monthly` | 18 |
| `before_first_payout` | 17 |
| `position_check` | 16 |
| `live_activation` | 16 |
| `at_funded_transition` | 16 |
| `purchase` | 16 |
| `upgrade_to_funded` | 16 |
| `after_first_trade` | 16 |
| `evaluation` | 16 |
| `objectives_met` | 16 |
| `mll_observation` | 16 |
| `funded` | 16 |
| `request_submitted` | 16 |
| `payout_approval` | 16 |
| `new_payout_cycle` | 16 |
| `payout_denied` | 16 |
| `post_payout_session_update` | 16 |
| `profit_tests` | 16 |
| `position_open` | 16 |
| `on_safety_net_met` | 15 |
| `on_violation` | 15 |
| `after_rule_violation` | 15 |
| `at_payment` | 15 |
| `after_objectives_met` | 15 |
| `at_firm_discretion` | 15 |
| `at_end_of_day` | 14 |
| `at_first_withdrawal` | 14 |
| `before_first_reward` | 14 |
| `on_chargeback` | 14 |
| `per_trading_day` | 14 |
| `per_payout` | 14 |
| `any_time` | 14 |
| `eval_pass_to_funded_activation` | 14 |
| `after_target_reached` | 12 |
| `at_reset_purchase` | 12 |
| `before_session_close` | 11 |
| `on_pass` | 11 |
| `after_funding_approval` | 10 |
| `at_funded` | 8 |
| `after_pass` | 8 |
| `between_payouts` | 8 |
| `reach_target` | 8 |
| `threshold_lock` | 8 |
| `peak_update` | 8 |
| `touch_threshold` | 8 |
| `activation` | 8 |
| `hit_dll` | 8 |
| `payout_cycle_reset` | 8 |
| `payout` | 8 |
| `after_first_payout` | 8 |
| `before_rebill` | 7 |
| `at_cancel` | 7 |
| `on_inactivity` | 7 |
| `on_touch` | 6 |
| `at_renewal_payment_failure` | 6 |
| `after_renewal_payment_failure` | 6 |
| `after_grace_period` | 6 |
| `at_first_login` | 6 |
| `at_payout_invoice_confirmation` | 6 |
| `at_payout_disbursement` | 6 |
| `at_payout_receipt` | 6 |
| `live_call_up_review` | 6 |
| `cumulative_payouts` | 6 |
| `on_close` | 5 |
| `after_buffer_secured` | 4 |
| `at_session_close` | 4 |
| `on_purchase` | 3 |
| `at_reward` | 2 |
| `advertised_in_help_article` | 2 |
| `during_evaluation;during_funded` | 1 |
| `payout_split` | 1 |

#### rules.value_type - 6 distinct values

| value | count |
|---|---|
| `null` | 11,490 |
| `number` | 5,873 |
| `string` | 5,068 |
| `boolean` | 2,736 |
| `object` | 925 |
| `array` | 413 |

#### rules.unit - 74 distinct values

| value | count |
|---|---|
| `enum` | 9,480 |
| `text` | 4,610 |
| `USD` | 3,632 |
| `boolean` | 2,758 |
| `unknown` | 1,245 |
| `ratio` | 810 |
| `days` | 621 |
| `contracts` | 506 |
| `USD_PRESUMED_UNCONFIRMED` | 493 |
| `count` | 462 |
| `DOLLAR_SYMBOL_ONLY` | 170 |
| `minutes` | 93 |
| `business_days` | 90 |
| `hours` | 88 |
| `accounts` | 87 |
| `array` | 65 |
| `calendar_days` | 61 |
| `N/A` | 60 |
| `payouts` | 60 |
| `event` | 56 |
| `years` | 49 |
| `net after fees` | 48 |
| `weeks` | 48 |
| `USD and contracts` | 48 |
| `USD_PRESUMED_UNCONFIRMED per contract round trip` | 48 |
| `payout` | 44 |
| `account` | 44 |
| `qualifying trading days` | 44 |
| `ratio of live starting balance` | 44 |
| `distinct_session_count` | 32 |
| `type` | 32 |
| `balance` | 32 |
| `minute` | 32 |
| `micros per mini` | 30 |
| `EST, Monday-Friday` | 28 |
| `EST, Sunday-Thursday` | 28 |
| `date` | 27 |
| `trading_days` | 24 |
| `USD_per_month` | 24 |
| `time_window` | 23 |
| `formula` | 22 |
| `EST` | 18 |
| `micro_per_mini` | 16 |
| `ISO_currency` | 16 |
| `object` | 15 |
| `symbols` | 15 |
| `lots` | 15 |
| `country_list` | 14 |
| `territory_list` | 14 |
| `promo` | 14 |
| `phases` | 14 |
| `times` | 14 |
| `per side / contract; source currency not expressly labeled` | 14 |
| `USD per contract` | 12 |
| `USD per side per contract` | 12 |
| `string` | 10 |
| `business_hours` | 10 |
| `comparison` | 8 |
| `schedule` | 8 |
| `timing` | 8 |
| `trading days` | 8 |
| `USD per month` | 6 |
| `state_tuple` | 6 |
| `time_ct` | 6 |
| `trades` | 6 |
| `USD_and_contracts` | 6 |
| `attempts` | 6 |
| `time` | 4 |
| `contributing profitable days` | 4 |
| `day` | 4 |
| `calendar days` | 1 |
| `seconds` | 1 |
| `permanent profile` | 1 |
| `year` | 1 |

#### rules.stage - 42 distinct values

| value | count |
|---|---|
| `PURCHASE` | 4,677 |
| `PAYOUT` | 4,655 |
| `EVALUATION` | 3,558 |
| `LIVE` | 2,692 |
| `FUNDED` | 2,531 |
| `LIVE_REVIEW` | 1,759 |
| `ACTIVATION` | 1,044 |
| `EVALUATION;FUNDED` | 950 |
| `FUNDED;PAYOUT` | 941 |
| `UNSPECIFIED` | 915 |
| `SCOPE` | 625 |
| `RE_ENTRY` | 552 |
| `EVALUATION;SIM_FUNDED` | 312 |
| `EVALUATION;FUNDED;PAYOUT` | 169 |
| `SIM_FUNDED` | 162 |
| `TERMINATION` | 125 |
| `PURCHASE;ACTIVATION` | 124 |
| `ALL` | 100 |
| `LIVE;PRE_LIVE` | 96 |
| `SIM_FUNDED;LIVE` | 79 |
| `EVALUATION;ACTIVATION` | 72 |
| `LIVE_REVIEW;LIVE` | 46 |
| `EVALUATION;FUNDED;LIVE` | 41 |
| `UNSPECIFIED_SIM_SCOPE` | 40 |
| `RESET` | 26 |
| `PURCHASE;EVALUATION` | 24 |
| `UNSPECIFIED;PAYOUT` | 24 |
| `PURCHASE;EVALUATION;ACTIVATION` | 16 |
| `PAYOUT;LIVE_REVIEW` | 16 |
| `PRE_LIVE` | 16 |
| `UNSPECIFIED_ON_SHARED_PAGE` | 16 |
| `FUNDED;RESET` | 16 |
| `EVALUATION;SIM_FUNDED;LIVE` | 14 |
| `EVALUATION;FUNDED;ACTIVATION` | 14 |
| `PURCHASE;RESET` | 14 |
| `LIVE;PAYOUT` | 12 |
| `PAYOUT;RE_ENTRY` | 8 |
| `EVALUATION;PRE_LIVE` | 8 |
| `EVALUATION;RESET` | 6 |
| `PAYOUT;LIVE` | 6 |
| `KYC;PAYOUT` | 3 |
| `FUNDED;LIVE` | 1 |

#### rules.value_state - 17 distinct values

| value | count |
|---|---|
| `VERIFIED` | 13,835 |
| `UNKNOWN` | 9,151 |
| `PUBLIC_ADVERTISEMENT` | 588 |
| `NOT_STATED` | 538 |
| `AMBIGUOUS` | 515 |
| `NOT_PUBLISHED` | 432 |
| `VERIFIED_PUBLIC_CARD` | 329 |
| `CONFLICT` | 300 |
| `NONE` | 222 |
| `DERIVED` | 183 |
| `NOT_APPLICABLE` | 131 |
| `USER_ACCOUNT_UNKNOWN` | 85 |
| `UNVERIFIED` | 54 |
| `NOT_PUBLICLY_VERIFIED` | 50 |
| `EXPLICIT_UNLIMITED` | 50 |
| `DOCUMENT_NOT_RETRIEVED` | 22 |
| `NO_FIXED_LIMIT` | 20 |

#### rules.availability - 9 distinct values

| value | count |
|---|---|
| `PUBLIC_CURRENT` | 13,166 |
| `PUBLIC_PRODUCT_CONFIGURATION_UNCONFIRMED` | 7,789 |
| `CONFIGURATION_TEMPLATE_UNCONFIRMED` | 2,099 |
| `INVITED_CURRENT_OFFER_EFFECTIVE_DATE_UNCONFIRMED` | 1,452 |
| `PUBLIC_SIZE_FAMILY_CONFIGURATION_UNVERIFIED` | 1,395 |
| `NOT_OFFERED_ON_PUBLIC_PAGES` | 388 |
| `(null)` | 114 |
| `STATUS_CONFLICT_NOT_IN_PICKER` | 83 |
| `PUBLIC_LISTED_IN_PICKER_NOT_ON_PLAN_PAGE` | 19 |

#### rules.cohort - 14 distinct values

| value | count |
|---|---|
| `PUBLIC_OBSERVED_2026_10_26_NEW_PURCHASE_TERMS_ACCOUNT_UNCONFIRMED` | 4,696 |
| `PUBLIC_OBSERVED_2026_10_26_ACCOUNT_TERMS_UNCONFIRMED` | 4,107 |
| `PUBLIC_OBSERVED_2026_10_13_ACCOUNT_TERMS_UNCONFIRMED` | 3,580 |
| `PUBLIC_OBSERVED_2026_10_15_ACCOUNT_TERMS_UNCONFIRMED` | 2,597 |
| `DAILY_CURRENT_PUBLIC_2026_10_05` | 2,528 |
| `PUBLIC_OBSERVED_2026_10_05_ACCOUNT_TERMS_UNCONFIRMED` | 2,487 |
| `PUBLIC_SCOPE_ACCOUNT_TERMS_UNCONFIRMED` | 2,100 |
| `PUBLIC_OBSERVED_2026_10_26` | 1,595 |
| `PUBLIC_OBSERVED_2026_10_22_ACCOUNT_TERMS_UNCONFIRMED` | 974 |
| `PUBLIC_OBSERVED_2026_10_19` | 947 |
| `PUBLIC_OBSERVED_2026_10_19_ACCOUNT_TERMS_UNCONFIRMED` | 666 |
| `INVITED_ADVERTISED_PROGRAM_ACCOUNT_APPLICABILITY_UNKNOWN` | 152 |
| `PUBLIC_OBSERVED_ACCOUNT_UNCONFIRMED` | 75 |
| `LUCIDPRO_PURCHASED_OR_RESET_BEFORE_2025-11-28_1500_EST` | 1 |

#### rules.version - 8 distinct values

| value | count |
|---|---|
| `PUBLIC_2026_10_26` | 10,398 |
| `PUBLIC_2026_10_05` | 5,235 |
| `PUBLIC_2026_10_13` | 3,580 |
| `PUBLIC_2026_10_15` | 2,597 |
| `PUBLIC_2026_10_15_REPAIR` | 2,100 |
| `PUBLIC_2026_10_19` | 1,613 |
| `PUBLIC_2026_10_22` | 976 |
| `PUBLIC_2026_10_23` | 6 |

#### plans.eval_drawdown (counted over plans) - 11 distinct values

| value | count |
|---|---|
| `EOD` | 108 |
| `TRAILING_LOCK_AT_START` | 15 |
| `INTRADAY` | 12 |
| `N/A` | 9 |
| `RISK_MODEL_OPTION_DEPENDENT` | 8 |
| `STATIC` | 8 |
| `TRAILING_INTRADAY` | 6 |
| `TRAILING_EOD` | 6 |
| `EOD_TRAILING` | 6 |
| `LIVE_TRAILING` | 4 |
| `NOT_APPLICABLE` | 4 |

#### plans.funded_drawdown (counted over plans) - 11 distinct values

| value | count |
|---|---|
| `EOD` | 93 |
| `INTRADAY` | 29 |
| `TRAILING_LOCK_AT_START` | 15 |
| `RISK_MODEL_OPTION_DEPENDENT` | 8 |
| `STATIC` | 8 |
| `EOD_LIVESIM;TRAILING_LIVE` | 7 |
| `TRAILING_INTRADAY` | 6 |
| `TRAILING_EOD` | 6 |
| `EOD_TRAILING` | 6 |
| `LIVE_TRAILING` | 4 |
| `N/A_PRELIVE` | 4 |

#### plans.dll_option (counted over plans) - 15 distinct values

| value | count |
|---|---|
| `NONE` | 32 |
| `ON` | 30 |
| `` | 24 |
| `OFF` | 20 |
| `(null)` | 15 |
| `UNCONFIRMED` | 14 |
| `FUNDED_ONLY` | 11 |
| `UNKNOWN` | 9 |
| `RISK_MODEL_OPTION_DEPENDENT` | 8 |
| `FIXED_DAILY` | 6 |
| `SOFT_PAUSE` | 5 |
| `SOFT_BREACH` | 5 |
| `HARD_BREACH` | 3 |
| `FIXED_THEN_LUCIDSCALE` | 3 |
| `NOT_STATED` | 1 |

#### plans.availability (counted over plans) - 8 distinct values

| value | count |
|---|---|
| `PUBLIC_CURRENT` | 116 |
| `PUBLIC_PRODUCT_CONFIGURATION_UNCONFIRMED` | 36 |
| `INVITED_CURRENT_OFFER_EFFECTIVE_DATE_UNCONFIRMED` | 14 |
| `CONFIGURATION_TEMPLATE_UNCONFIRMED` | 9 |
| `PUBLIC_SIZE_FAMILY_CONFIGURATION_UNVERIFIED` | 5 |
| `NOT_OFFERED_ON_PUBLIC_PAGES` | 4 |
| `STATUS_CONFLICT_NOT_IN_PICKER` | 1 |
| `PUBLIC_LISTED_IN_PICKER_NOT_ON_PLAN_PAGE` | 1 |

#### plans.cohort (counted over plans) - 12 distinct values

| value | count |
|---|---|
| `PUBLIC_OBSERVED_2026_10_26_ACCOUNT_TERMS_UNCONFIRMED` | 40 |
| `PUBLIC_OBSERVED_2026_10_26_NEW_PURCHASE_TERMS_ACCOUNT_UNCONFIRMED` | 24 |
| `PUBLIC_OBSERVED_2026_10_05_ACCOUNT_TERMS_UNCONFIRMED` | 20 |
| `PUBLIC_OBSERVED_2026_10_19_ACCOUNT_TERMS_UNCONFIRMED` | 17 |
| `DAILY_CURRENT_PUBLIC_2026_10_05` | 16 |
| `PUBLIC_OBSERVED_2026_10_26` | 15 |
| `PUBLIC_OBSERVED_2026_10_13_ACCOUNT_TERMS_UNCONFIRMED` | 14 |
| `PUBLIC_OBSERVED_2026_10_15_ACCOUNT_TERMS_UNCONFIRMED` | 12 |
| `PUBLIC_SCOPE_ACCOUNT_TERMS_UNCONFIRMED` | 9 |
| `PUBLIC_OBSERVED_2026_10_22_ACCOUNT_TERMS_UNCONFIRMED` | 8 |
| `PUBLIC_OBSERVED_2026_10_19` | 7 |
| `INVITED_ADVERTISED_PROGRAM_ACCOUNT_APPLICABILITY_UNKNOWN` | 4 |

#### plans.version (counted over plans) - 7 distinct values

| value | count |
|---|---|
| `PUBLIC_2026_10_26` | 79 |
| `PUBLIC_2026_10_05` | 40 |
| `PUBLIC_2026_10_19` | 24 |
| `PUBLIC_2026_10_13` | 14 |
| `PUBLIC_2026_10_15` | 12 |
| `PUBLIC_2026_10_15_REPAIR` | 9 |
| `PUBLIC_2026_10_22` | 8 |

#### plans.product (counted over plans) - 27 distinct values

| value | count |
|---|---|
| `Evaluation` | 35 |
| `Flex` | 16 |
| `Daily` | 16 |
| `Qualification` | 12 |
| `Pro` | 12 |
| `Trading Combine` | 6 |
| `Tradeify 50K` | 6 |
| `Tradeify 25K` | 6 |
| `Tradeify 100K` | 6 |
| `Tradeify 150K` | 6 |
| `E8 Zero (futures)` | 5 |
| `Builder` | 5 |
| `Test` | 5 |
| `PRO+ Development` | 5 |
| `FastTrack` | 4 |
| `Momentum` | 4 |
| `E8 Signature (futures)` | 4 |
| `Gauntlet Mini` | 4 |
| `Direct` | 4 |
| `Maxx` | 4 |
| `Rapid` | 4 |
| `Trader Career Path` | 3 |
| `Direct to Funded` | 3 |
| `FTMO Futures Growth` | 3 |
| `FTMO Futures Pro` | 3 |
| `Studio` | 3 |
| `Rapid EOD` | 2 |

#### rules.applicability (top 40 of many; free text, sometimes a JSON-encoded string) - 767 distinct values

| value | count |
|---|---|
| `{"configuration":"unconfirmed"}` | 3,746 |
| `{}` | 2,994 |
| `{"assessment_only":true,"lifecycle_applicability":"undetermined"}` | 1,651 |
| `{"family":"LucidDaily","size":null,"drawdown":null,"dll_enabled":null}` | 1,328 |
| `Public product-family evidence; actual purchase option/platform/account agreement must be confirmed` | 1,080 |
| `All plans` | 1,005 |
| `Flex` | 876 |
| `all_7_current_plans` | 812 |
| `LucidLive transition from current Flex/Pro/Direct/Daily` | 748 |
| `ETF_1STEP_50K_LIVETRAIL;ETF_1STEP_100K_LIVETRAIL;ETF_1STEP_250K_LIVETRAIL;ETF_EOD_50K;ETF_EOD_100K;ETF_STATIC_10K;ETF_STATIC_25K;ETF_STATIC_50K;ETF_FASTTRACK_10K_EOD;ETF_FASTTRACK_10K_STATIC;ETF_DIAMO` | 686 |
| `{"product":"PRO+ Development","scope_confirmation":"undetermined"}` | 650 |
| `All account types` | 600 |
| `{"product":"Test","scope_confirmation":"undetermined"}` | 595 |
| `{"plan_scope":"plan_ids as listed","account_terms":"public page terms; account agreement and purchase cohort unconfirmed"}` | 586 |
| `Published Test→PRO→conditional Standard PRO+ lifecycle; account terms unconfirmed` | 555 |
| `Public wording observed 2026-10-15; policy effective date and individual account applicability unknown` | 444 |
| `Master` | 340 |
| `Evaluation` | 330 |
| `Trading Combine` | 327 |
| `Evaluation entry; includes subsequent funded activation` | 225 |
| `DLL_ON` | 204 |
| `All LucidPro accounts, subject to source-specific cohort` | 192 |
| `DLL_OFF` | 184 |
| `{"original":"LucidLive transition from current Flex/Pro/Direct/Daily","products":["Flex","Pro","Direct"],"scope_resolution":"split existing mixed verification/applicability states; not new firm policy` | 168 |
| `Test` | 165 |
| `Qualification` | 120 |
| `LucidPro; LucidFlex; LucidDirect` | 112 |
| `{"plan_scope":"size-family template; configuration not verified"}` | 103 |
| `LucidMaxx (new advertised program; invited traders)` | 100 |
| `{"product":"PRO+ Development"}` | 100 |
| `ALL_CURRENT_DIRECT` | 96 |
| `{"original":"LucidLive transition from current Flex/Pro/Direct/Daily","products":["Daily"],"scope_resolution":"split existing mixed verification/applicability states; not new firm policy"}` | 96 |
| `LucidLive` | 88 |
| `{"family":"LucidDaily","size":150000,"drawdown":null,"dll_enabled":null}` | 84 |
| `{"family":"LucidDaily","size":100000,"drawdown":null,"dll_enabled":null}` | 80 |
| `{"family":"LucidDaily","size":50000,"drawdown":null,"dll_enabled":null}` | 76 |
| `Direct size table` | 76 |
| `{"family":"LucidDaily","size":25000,"drawdown":null,"dll_enabled":null}` | 72 |
| `ETF_1STEP_50K_LIVETRAIL;ETF_1STEP_100K_LIVETRAIL;ETF_1STEP_250K_LIVETRAIL;ETF_EOD_50K;ETF_EOD_100K;ETF_STATIC_10K;ETF_STATIC_25K;ETF_STATIC_50K;ETF_DIAMOND_100K` | 63 |
| `Master-level accounts` | 60 |
| ... 727 more distinct values (each with lower counts) | |

## 3. Plans, cohorts and versions per firm

Counted from `plans[]` (plan-level `cohort` and `version`). "Rule cohorts/versions" are the distinct values on the rule records.

| firm | plans | plan cohorts | plan versions | rule cohorts | rule versions | multiple versions? |
|---|---|---|---|---|---|---|
| apex | 8 | 1 | 1 | 2 | 2 | yes |
| bulenox | 20 | 1 | 1 | 1 | 1 | no |
| e8markets | 9 | 1 | 1 | 1 | 1 | no |
| earn2trade | 7 | 1 | 1 | 1 | 1 | no |
| elitetraderfunding | 15 | 1 | 1 | 1 | 1 | no |
| ftmofutures | 6 | 2 | 2 | 2 | 2 | yes |
| lucid | 48 | 4 | 2 | 6 | 3 | yes |
| myfundedfutures | 18 | 2 | 2 | 2 | 2 | yes |
| oneuptrader | 15 | 1 | 1 | 1 | 1 | no |
| takeprofittrader | 10 | 1 | 1 | 1 | 1 | no |
| topstep | 6 | 1 | 1 | 1 | 1 | no |
| tradeify | 24 | 1 | 1 | 1 | 1 | no |

Firms with more than one version (plan versions; additional versions only on rule records; plan cohorts):

- **apex**: plan versions ['PUBLIC_2026_10_13']; rule-only versions ['PUBLIC_2026_10_15']; plan cohorts ['PUBLIC_OBSERVED_2026_10_13_ACCOUNT_TERMS_UNCONFIRMED']
- **ftmofutures**: plan versions ['PUBLIC_2026_10_15', 'PUBLIC_2026_10_26']; rule-only versions []; plan cohorts ['PUBLIC_OBSERVED_2026_10_15_ACCOUNT_TERMS_UNCONFIRMED', 'PUBLIC_OBSERVED_2026_10_26_ACCOUNT_TERMS_UNCONFIRMED']
- **lucid**: plan versions ['PUBLIC_2026_10_05', 'PUBLIC_2026_10_22']; rule-only versions ['PUBLIC_2026_10_23']; plan cohorts ['DAILY_CURRENT_PUBLIC_2026_10_05', 'INVITED_ADVERTISED_PROGRAM_ACCOUNT_APPLICABILITY_UNKNOWN', 'PUBLIC_OBSERVED_2026_10_05_ACCOUNT_TERMS_UNCONFIRMED', 'PUBLIC_OBSERVED_2026_10_22_ACCOUNT_TERMS_UNCONFIRMED']
- **myfundedfutures**: plan versions ['PUBLIC_2026_10_19', 'PUBLIC_2026_10_26']; rule-only versions []; plan cohorts ['PUBLIC_OBSERVED_2026_10_19_ACCOUNT_TERMS_UNCONFIRMED', 'PUBLIC_OBSERVED_2026_10_26_ACCOUNT_TERMS_UNCONFIRMED']

## 4. value_state counts per firm and UNKNOWN share

| firm | rules | AMBIGUOUS | CONFLICT | DERIVED | DOCUMENT_NOT_RETRIEVED | EXPLICIT_UNLIMITED | NONE | NOT_APPLICABLE | NOT_PUBLICLY_VERIFIED | NOT_PUBLISHED | NOT_STATED | NO_FIXED_LIMIT | PUBLIC_ADVERTISEMENT | UNKNOWN | UNVERIFIED | USER_ACCOUNT_UNKNOWN | VERIFIED | VERIFIED_PUBLIC_CARD | UNKNOWN share |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| apex | 1,772 | 20 | 18 | 8 | 0 | 0 | 18 | 0 | 0 | 0 | 0 | 0 | 55 | 880 | 0 | 0 | 773 | 0 | 49.7% (880/1,772) |
| bulenox | 1,988 | 56 | 158 | 0 | 0 | 0 | 4 | 52 | 32 | 56 | 12 | 0 | 32 | 482 | 0 | 0 | 1032 | 72 | 24.2% (482/1,988) |
| e8markets | 2,100 | 35 | 10 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 9 | 7 | 44 | 1676 | 0 | 4 | 306 | 9 | 79.8% (1,676/2,100) |
| earn2trade | 947 | 0 | 0 | 14 | 0 | 0 | 0 | 0 | 0 | 0 | 32 | 0 | 28 | 238 | 0 | 0 | 600 | 35 | 25.1% (238/947) |
| elitetraderfunding | 1,245 | 0 | 2 | 0 | 0 | 0 | 0 | 6 | 0 | 0 | 5 | 0 | 59 | 69 | 9 | 0 | 1055 | 40 | 5.5% (69/1,245) |
| ftmofutures | 1,281 | 6 | 0 | 6 | 0 | 18 | 12 | 0 | 0 | 12 | 36 | 0 | 0 | 576 | 0 | 6 | 609 | 0 | 45.0% (576/1,281) |
| lucid | 6,217 | 334 | 34 | 80 | 16 | 16 | 105 | 56 | 16 | 280 | 279 | 8 | 235 | 424 | 42 | 16 | 4146 | 130 | 6.8% (424/6,217) |
| myfundedfutures | 686 | 0 | 4 | 0 | 0 | 0 | 24 | 0 | 2 | 0 | 38 | 0 | 57 | 92 | 3 | 0 | 446 | 20 | 13.4% (92/686) |
| oneuptrader | 1,595 | 5 | 24 | 10 | 0 | 0 | 25 | 0 | 0 | 60 | 30 | 0 | 20 | 505 | 0 | 0 | 901 | 15 | 31.7% (505/1,595) |
| takeprofittrader | 2,166 | 10 | 0 | 5 | 0 | 0 | 10 | 0 | 0 | 0 | 5 | 5 | 15 | 1255 | 0 | 5 | 856 | 0 | 57.9% (1,255/2,166) |
| topstep | 1,812 | 24 | 0 | 7 | 6 | 12 | 0 | 0 | 0 | 24 | 10 | 0 | 3 | 858 | 0 | 6 | 854 | 8 | 47.4% (858/1,812) |
| tradeify | 4,696 | 25 | 50 | 53 | 0 | 4 | 24 | 17 | 0 | 0 | 82 | 0 | 40 | 2096 | 0 | 48 | 2257 | 0 | 44.6% (2,096/4,696) |
| **all** | 26,505 | 515 | 300 | 183 | 22 | 50 | 222 | 131 | 50 | 432 | 538 | 20 | 588 | 9151 | 54 | 85 | 13835 | 329 | 34.5% (9,151/26,505) |

UNKNOWN share = UNKNOWN rule records / all rule records of the firm (metadata records included).

## 5. Records with multiple sources

Counted on `rules[].sources[]` (source entries per rule record) and `rules[].source_urls[]` (distinct URLs listed).

| firm | rules | with >1 `sources` entry | with >1 `source_urls` | with 0 sources | max sources on one record |
|---|---|---|---|---|---|
| apex | 1,772 | 474 | 474 | 872 | 10 |
| bulenox | 1,988 | 618 | 618 | 446 | 4 |
| e8markets | 2,100 | 148 | 148 | 1,658 | 4 |
| earn2trade | 947 | 335 | 335 | 224 | 5 |
| elitetraderfunding | 1,245 | 348 | 348 | 7 | 5 |
| ftmofutures | 1,281 | 410 | 410 | 558 | 8 |
| lucid | 6,217 | 1,046 | 1,046 | 304 | 16 |
| myfundedfutures | 686 | 262 | 262 | 0 | 6 |
| oneuptrader | 1,595 | 280 | 280 | 555 | 6 |
| takeprofittrader | 2,166 | 165 | 165 | 1,250 | 3 |
| topstep | 1,812 | 942 | 942 | 822 | 14 |
| tradeify | 4,696 | 1,705 | 1,705 | 2,096 | 8 |
| **all** | 26,505 | 6,733 | 6,733 | 8,792 | |

## 6. `data/index.json` structure

Top-level keys: `dataset`, `snapshot_date`, `firm_count`, `totals`, `firms`, `notes`.

- `totals` keys: `plans`, `rules`, `sources`, `unknown_rules`, `unknown_share`, `rules_by_value_state`.
- each `firms[]` entry keys: `slug`, `name`, `file`, `file_bytes`, `plans`, `rules`, `sources`, `unknown_rules`, `unknown_share`, `rules_by_value_state`, `latest_checked_at`, `last_checked`.
- `latest_checked_at` is the latest `checked_at` among the firm's rule records; `last_checked` is the snapshot check date (2026-10-27). `drive_modifiedTime` is not exported.

```json
{
 "dataset": "PropSim-Skill rules data (bettertrading.ai)",
 "snapshot_date": "2026-10-27",
 "firm_count": 12,
 "totals": {
  "plans": 186,
  "rules": 26505,
  "sources": 707,
  "unknown_rules": 9151,
  "unknown_share": 0.3453,
  "rules_by_value_state": {
   "AMBIGUOUS": 515,
   "CONFLICT": 300,
   "DERIVED": 183,
   "DOCUMENT_NOT_RETRIEVED": 22,
   "EXPLICIT_UNLIMITED": 50,
   "NONE": 222,
   "NOT_APPLICABLE": 131,
   "NOT_PUBLICLY_VERIFIED": 50,
   "NOT_PUBLISHED": 432,
   "NOT_STATED": 538,
   "NO_FIXED_LIMIT": 20,
   "PUBLIC_ADVERTISEMENT": 588,
   "UNKNOWN": 9151,
   "UNVERIFIED": 54,
   "USER_ACCOUNT_UNKNOWN": 85,
   "VERIFIED": 13835,
   "VERIFIED_PUBLIC_CARD": 329
  }
 },
 "notes": "UNKNOWN means not confirmed; nothing is guessed. See README_DATA.md.",
 "firms": [
  {
   "slug": "apex",
   "name": "Apex",
   "file": "data/apex.json",
   "file_bytes": 2694515,
   "plans": 8,
   "rules": 1772,
   "sources": 58,
   "unknown_rules": 880,
   "unknown_share": 0.4966,
   "rules_by_value_state": {
    "AMBIGUOUS": 20,
    "CONFLICT": 18,
    "DERIVED": 8,
    "NONE": 18,
    "PUBLIC_ADVERTISEMENT": 55,
    "UNKNOWN": 880,
    "VERIFIED": 773
   },
   "latest_checked_at": "2026-10-27T06:47:20Z",
   "last_checked": "2026-10-27"
  },
  "..."
 ]
}
```
