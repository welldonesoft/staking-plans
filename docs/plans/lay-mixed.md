---
id: lay-mixed
name: Lay Mixed Staking Plan
category: lay
type: hybrid
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Mixed Lay Staking
---

# Lay Mixed Staking Plan

## Overview

A hybrid lay staking plan that combines elements of flat staking and proportional staking. Part of the stake is fixed, part scales with bankroll — providing a middle ground between conservative and growth-oriented approaches.

## How It Works

The stake is composed of two parts:
1. **Fixed component:** A constant amount (like lay level)
2. **Proportional component:** A percentage of bankroll (like lay percentage)

$$Stake = F + (B \times p)$$

Where $F$ = fixed amount, $B$ = bankroll, $p$ = percentage.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `fixed_stake` | number | 5 | Fixed portion of the stake |
| `percentage` | number | 1 | Percentage of bankroll for proportional portion |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Between flat and proportional — moderate
- **Recommended Bankroll:** 50× total initial stake

## When to Use

- You want some growth but find pure proportional too volatile
- You want a blend of predictability and compounding

## When to Avoid

- Simplicity is paramount (use pure flat or pure proportional)
- Very small bankrolls (proportional component adds negligible amount)

## Betfair Exchange Notes

- For lay, ensure both components are sized with liability in mind
- The proportional component creates compounding; the fixed component creates stability

## Related Plans

- [Lay Level](./lay-level.md) — Pure flat
- [Lay Percentage](./lay-percentage.md) — Pure proportional

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
