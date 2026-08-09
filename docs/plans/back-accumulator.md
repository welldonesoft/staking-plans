---
id: back-accumulator
name: Back Accumulator Staking Plan
category: back
type: positive-progression
risk: medium
betfair_compatible: true
aliases:
  - Accumulator Staking (Back)
  - Profit Accumulator
source: marketfeeder
---

# Back Accumulator Staking Plan

## Overview

A positive progression plan for back betting: after each win, accumulate the stake by adding the base stake plus a percentage of the profit. Reset to base after a loss or after completing the cycle. The opposite of recovery staking — it compounds winnings, not losses.

## How It Works

1. Start with a base stake (e.g., £5)
2. **Win:** Next stake = base stake × step number + % of previous profit
3. **Loss:** Reset to base stake
4. After N steps (e.g., 5), reset to base stake regardless

**Example (5-step cycle, £5 base, 50% profit accumulation):**
- Step 1: £5 (Win) → Step 2: £10 + 50% of £5 profit = £12.50
- Step 2: £12.50 (Win) → Step 3: £15 + 50% of £12.50 profit = £21.25
- Step 3: £21.25 (Loss) → Reset to £5

## Formula

$$S_n = B \times n + p \times P_{n-1}$$

Where:
- $S_n$ = stake at step $n$
- $B$ = base stake
- $n$ = step number in cycle (1, 2, 3...)
- $p$ = profit accumulation percentage (e.g., 0.50)
- $P_{n-1}$ = profit from the previous winning bet

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 5 | Starting stake |
| `cycle_length` | number | 5 | Number of steps before forced reset |
| `profit_pct` | number | 50 | % of profit to accumulate into next stake |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Base stake per losing bet (never chases losses)
- **Recommended Bankroll:** 30× maximum cycle stake
- **Ruin Risk:** Low — you only risk accumulated profits, never increase after losses

## When to Use

- Your selections cluster in winning streaks
- You want to compound during hot runs
- Risk-averse approach to progression (never chase losses)

## When to Avoid

- Isolated winners (rarely get to step 3+)
- Low strike rates (mostly resetting to base)
- You prefer flat staking for consistency

## Betfair Exchange Notes

- Commission reduces the effective profit for accumulation — use post-commission profit in the formula
- Works well on exchange where you can adjust stakes fluidly

## Related Plans

- [Lay Accumulator](./lay-accumulator.md) — Lay equivalent (liability-based)
- [Parlay](./parlay.md) — Simpler "let it ride" approach
- [1-3-2-6](./1326.md) — Fixed-sequence positive progression

---

## Sources

- **Plan source:** [MarketFeeder — Back Accumulator Staking](https://marketfeeder.co.uk/learn/triggers/back-accumulator-staking-plan/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
