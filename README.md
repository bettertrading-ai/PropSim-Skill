# PropSim

PropSim is a skill that simulates prop firm evaluation and funded accounts from a daily trade series and firm rules data. See `SKILL.md`.

You must bring a daily trade series from your own backtest. The firm rules data is included in the `data/` folder of this repo: `data/index.json` (list of firms, with counts and the share of UNKNOWN values per firm) and one file `data/<slug>.json` per firm (12 firm files, about 43 MB in total). No trade data is included.

The data may contain UNKNOWN or conflicting values, and each rule has source information where available. Every rule keeps its `value_state` as recorded; UNKNOWN means not confirmed, never zero.

**Disclaimer:** Simulation output is an estimate, not financial advice; prop firm rules change, always use the current firm rules data.

License: MIT (see `LICENSE`).
