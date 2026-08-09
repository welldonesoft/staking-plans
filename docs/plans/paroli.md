---
id: paroli
name: Paroli (Reverse Martingale)
category: back
type: positive-progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Reverse Martingale
  - Anti-Martingale
  - Paroli System
---

# Paroli (Reverse Martingale)

## Overview

The exact opposite of Martingale: double your stake after **wins**, not losses. After 3 consecutive wins, reset to base. The philosophy: ride winning streaks with the house's money, but never chase losses. One of the oldest positive progression systems, dating back to 16th-century Italy.

## How It Works

1. Start with 1 unit
2. **Win:** Double the stake (up to 2 more times — max 3 doublings)
3. **Loss:** Reset to 1 unit
4. After 3 consecutive wins, reset to 1 unit

**Example:** £10 → Win (+£10) → £20 → Win (+£20) → £40 → Win (+£40) → Reset to £10. Total profit: £70 from an initial £10 risk.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_unit` | number | 1 | Starting stake |
| `max_steps` | number | 3 | Maximum consecutive doublings |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Only 1 unit per losing bet (never chase losses)
- **Recommended Bankroll:** 20× base unit
- **Ruin Risk:** Low — you only ever risk your base unit

## When to Use

- Your winners tend to cluster in streaks
- You want to compound during hot runs without risking your bankroll
- You prefer the psychological comfort of "never increase after a loss"

## When to Avoid

- Isolated winners (rarely get to step 2 or 3)
- Low strike rate (mostly resetting to base)
- You want aggressive bankroll growth (use proportional staking)

## Paroli vs Parlay vs 1-3-2-6

| | Paroli | Parlay | 1-3-2-6 |
|---|---|---|---|
| After win | Double stake | Reinvest stake+profit | Follow fixed sequence |
| After loss | Reset to base | Reset to base | Reset to base |
| Max steps | 3 | Configurable | 4 |
| Risk profile | Medium | Medium | Medium |

## Betfair Exchange Notes

- Works identically for back and lay
- For lay Paroli, double liability after each winning lay (not recommended — better to double stake)
- Commission reduces effective profit per step

## Related Plans

- [Martingale](./martingale.md) — Opposite philosophy (double after losses)
- [Parlay](./parlay.md) — Similar but reinvests stake+profit
- [1-3-2-6](./1326.md) — Fixed-sequence positive progression
- [Back Accumulator](./back-accumulator.md) — Accumulates base+profit after wins

---

## Sources

- **Plan mechanics:** Classic betting system dating to 16th-century Italy (public domain)
- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
