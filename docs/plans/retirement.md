---
id: retirement
name: Retirement Staking Plan
category: back
type: target-based
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Retirement Plan
---

# Retirement Staking Plan

## Overview

A target-based staking plan where you aim to achieve a set profit target within a fixed number of bets. Stakes are calculated to reach the target while managing risk through a divisor that adjusts based on results.

## How It Works

1. Set a **profit target** and a **divisor** (e.g., target = £100, divisor = 10)
2. Stake = Target / Divisor (£100/10 = £10 for the first bet)
3. **Win:** Reduce target by profit won, reduce divisor by 1
4. **Loss:** Add lost stake to target, divisor stays the same

The plan "retires" when the target reaches zero (profit achieved).

## Formula

$$S = \frac{T}{D}$$

Where:
- $S$ = stake
- $T$ = remaining profit target
- $D$ = current divisor

After a win: $T_{new} = T - \text{profit}$, $D_{new} = D - 1$
After a loss: $T_{new} = T + \text{stake lost}$, $D_{new} = D$

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target` | number | 100 | Profit target to achieve |
| `divisor` | number | 10 | Initial divisor (controls stake size) |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Moderate — losses increase the target, inflating future stakes
- **Recommended Bankroll:** 5–10× target
- **Ruin Risk:** Medium — prolonged losing can cause target inflation

## When to Use

- You have a specific profit goal in mind
- You want structured, goal-oriented staking
- Your strike rate is reasonable (40%+)

## When to Avoid

- Very long odds — wins are too infrequent to reduce the target
- You have no specific profit target

## Betfair Exchange Notes

- Adjust target for commission: after a win, target reduces by profit × (1 − commission)
- Works for both back and lay

## Related Plans

- [6 Point Divisor](./6-point-divisor.md) — Similar divisor-based plan
- [Bookies Bank](./bookies-bank.md) — Target-based plan with different divisor rules

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
