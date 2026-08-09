---
id: coup-master
name: Coup Master
category: back
type: target-based
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Coup Plan
---

# Coup Master Staking Plan

## Overview

A target-based staking plan where each successful "coup" (completing a target cycle) leads to a new, larger target. Designed for structured, compounding bankroll growth through repeated target achievement.

## How It Works

1. Set an initial profit target
2. Stake to achieve the target using a divisor or fixed calculation
3. When target is reached (coup completed):
   - Bankroll has grown
   - Set a new, larger target based on the increased bankroll
4. Repeat — each coup builds toward larger targets

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `initial_target` | number | 100 | Starting profit target |
| `target_increase` | string | "percentage" | How targets increase ("percentage" or "fixed") |
| `increase_amount` | number | 20 | Percentage or fixed amount increase per coup |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** During any single coup attempt — moderate
- **Recommended Bankroll:** 5–10× initial target
- **Ruin Risk:** Medium — each coup attempt is independent

## When to Use

- You want structured, compounding growth
- You enjoy goal-oriented betting with clear milestones
- Your bankroll can support escalating targets

## When to Avoid

- Inconsistent results (failed coups are discouraging)
- You prefer simpler, non-target-based plans

## Betfair Exchange Notes

- After each successful coup, recalculate based on new bankroll accounting for commission
- Works for both back and lay betting

## Related Plans

- [Bookies Bank](./bookies-bank.md) — Similar target-based compounding
- [Retirement](./retirement.md) — Single-target cousin

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
