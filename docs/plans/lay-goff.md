---
id: lay-goff
name: Lay Goff Staking Plan
category: lay
type: target-based
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Goff Lay Plan
---

# Lay Goff Staking Plan

## Overview

A target-based lay staking plan with a specific structure for achieving profit targets through lay betting. Uses a divisor-style calculation adapted for the unique characteristics of lay betting.

## How It Works

1. Set a profit target for lay betting
2. Calculate lay stakes using a divisor that adjusts based on results
3. **Winning lay (selection loses):** Profit reduces target
4. **Losing lay (selection wins):** Loss is incorporated into the target
5. Target reached = cycle complete

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target` | number | 100 | Profit target |
| `divisor` | number | 4 | Starting divisor |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Target inflation after losing lays
- **Recommended Bankroll:** 5× target

## When to Use

- Structured, goal-oriented lay betting
- You want a target to work toward

## When to Avoid

- Low lay strike rates (target grows without being reduced)
- You prefer simpler lay staking

## Betfair Exchange Notes

- Factor commission into target reduction (winning lay profit = stake × (1−commission))

## Related Plans

- [Bookies Bank](./bookies-bank.md) — Back betting divisor plan
- [Lay Liability](./lay-liability.md) — Simpler alternative

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
