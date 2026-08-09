---
id: percentage-point
name: Percentage Point Staking Plan
category: back
type: proportional
risk: low
betfair_compatible: true
aliases:
  - Point Staking
  - Bank Divided by Points
source: marketfeeder
---

# Percentage Point Staking Plan

## Overview

A simple proportional staking plan: divide your bank into a fixed number of "points," then bet one point. After each result, recalculate the point value based on your new bank balance. Similar to percentage staking but framed in terms of points.

## How It Works

1. Decide how many points to divide your bank into (e.g., 100)
2. Each bet = 1 point = Bank ÷ number of points
3. After each result (win or loss), recalculate: new bet = New Bank ÷ number of points
4. The point value naturally grows with wins and shrinks with losses

**Example:** £1,000 bank ÷ 100 points = £10 per bet. After a win at 2.0 (+£10), bank = £1,010. Next bet = £1,010 ÷ 100 = £10.10.

## Formula

$$S = \frac{B}{N}$$

Where:
- $S$ = stake (1 point)
- $B$ = current bankroll
- $N$ = number of points (fixed)

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `num_points` | number | 100 | Number of points to divide bank into |
| `starting_bank` | number | 1000 | Initial bankroll |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** Self-correcting — stakes shrink as bank shrinks
- **Recommended Bankroll:** N points (by definition)
- **Ruin Risk:** Very low — mathematically identical to percentage staking

## Comparison: Point Staking vs Percentage Staking

| | Point Staking (100 pts) | Percentage Staking (1%) |
|---|---|---|
| Stake calculation | Bank ÷ 100 | Bank × 1% |
| Result | Identical | Identical |
| Framing | "I have 100 points" | "I bet 1%" |
| Psychology | Points feel tangible | Percentages feel abstract |

## When to Use

- You prefer thinking in "points" rather than percentages
- Simple, clean bankroll management
- Long-term conservative betting

## When to Avoid

- You want more sophisticated proportional staking (use Kelly)
- Very small banks (1 point may be below minimum bet)

## Betfair Exchange Notes

- Works identically for back and lay
- For lay betting, define whether 1 point = 1 point of stake or 1 point of liability

## Related Plans

- [Percentage Staking](./percentage-staking.md) — Mathematically identical, different framing
- [Level Stakes](./level-stakes.md) — Fixed stakes, no recalculating
- [Secure](./secure.md) — Conservative flat alternative

---

## Sources

- **Plan source:** [MarketFeeder — Percentage Point Staking](https://marketfeeder.co.uk/learn/triggers/back-percentage-point/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
