# Staking Plans

> Comprehensive, structured catalog of 71 betting staking plans — built for AI agents and humans alike.

A public, AI-friendly repository containing structured Markdown definitions of all known staking plans used in betting, with a focus on the Betfair Exchange.

## What's Inside

| Layer | Description |
|-------|-------------|
| **`docs/`** | GitHub Pages site — 71 staking plan pages + index |
| **`docs/index.md`** | Master index with all plans categorized by type and risk |
| **`docs/plans/`** | Individual plan pages with formulas, parameters, risk assessment, and Betfair notes |

## Staking Plans (71 total)

| Category | Count | Examples |
|----------|-------|----------|
| 🔵 **Back** | 44 | Level Stakes, Kelly, Martingale, Fibonacci, Paroli, Oscar's Grind... |
| 🔴 **Lay** | 25 | Lay Level, Lay Kelly, Lay Liability, Lay Ladder, Lay D'Alembert... |
| 🟢 **Each-Way** | 2 | Each-Way Level, Each-Way Combined |

> 3 plans are community-contributed: Diluted Loss Recovery, Stepped Time-Based, Divide-by-N Recovery

### Plan Types

- **Flat** — Same stake every bet (Level Stakes, Secure)
- **Proportional** — Stake scales with bankroll (Percentage, Kelly, Square Root)
- **Positive Progression** — Increase after wins (Paroli, Parlay, Oscar's Grind)
- **Negative Progression** — Increase after losses (Martingale, Fibonacci, D'Alembert)
- **Recovery** — Aggressively chase losses (Recovery, Stop at a Winner)
- **Target-Based** — Aim for a specific profit (Retirement, 6 Point Divisor, Bookies Bank)

## Sources

Plans are sourced and attributed from:

| Source | Plans | 
|--------|-------|
| [The Staking Machine](https://thestakingmachine.com/staking-plans/) | 58 plans — primary catalog reference |
| [MarketFeeder](https://marketfeeder.co.uk/learn/triggers/by-tag/tags/staking-plan/) | 10 plans — trigger library |
| [WellDone Community Forum](https://community.welldonesoft.com/) | 3 plans — user-contributed concepts |

Individual plan pages contain specific source attribution. Plan mechanics and mathematical formulas are in the public domain.

## AI-Friendly Design

- **YAML frontmatter** on every page — machine-parseable metadata (id, category, type, risk, aliases, source)
- **Consistent structure** — Overview, How It Works, Formula, Parameters, Risk Assessment, Betfair Notes
- **Cross-linked** — Every plan links to related plans
- **Markdown-native** — No build step, no JavaScript, readable by any AI agent or tool
- **GitHub Pages** — Enable in repo settings pointing to `/docs`

### AI Ingestion Files

| File | Purpose | Size |
|------|---------|------|
| [`llms.txt`](./llms.txt) | Discovery file — all 71 plans with descriptions. Emerging standard for LLM-friendly sites. | ~3 KB |
| [`llms-full.txt`](./llms-full.txt) | All 71 plans concatenated. Single-read ingestion for agents with large context windows. | ~170 KB |
| [`docs/plans/index.json`](./docs/plans/index.json) | Machine-parseable JSON index — every plan's metadata in structured form. | ~15 KB |

## License

Content is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to use, share, and adapt with attribution.

Plan mechanics and mathematical formulas are in the public domain.

## Risk Warning

Staking plans do not create profit from losing selections. No money management system can turn a negative expected value into a positive one. Always gamble responsibly.
