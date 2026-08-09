---
id: certain-profit
name: Certain Profit
category: back
type: target-based
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Guaranteed Profit Plan
---

# Certain Profit Staking Plan

## Overview

A target-based plan that calculates stakes to achieve a specific profit target while factoring in cumulative losses. After each loss, the target increases to include recovering previous losses, but the plan ensures any single winner at the right odds clears the entire target.

## How It Works

1. Set a profit target
2. After each loss, add the lost stake to the target
3. Calculate the next stake to achieve (original target + accumulated losses) given the odds
4. A winner at sufficient odds clears all losses and achieves the target

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target` | number | 100 | Profit target |
| `max_steps` | number | 10 | Maximum bets before forced reset |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Controlled by max_steps and odds
- **Recommended Bankroll:** 10× target
- **Ruin Risk:** Medium — max_steps provides a safety ceiling

## When to Use

- You want guaranteed profit per cycle (assuming a winner arrives within the step limit)
- Controlled risk through step limits
- Moderate strike rates

## When to Avoid

- Very low strike rate (winners arrive after max_steps expires)
- High-odds selections (stakes to clear target become very small, prolonging cycles)

## Betfair Exchange Notes

- Commission effectively reduces the "certain" profit slightly
- Works better for back betting than lay (predictable stake-to-return ratio)

## Related Plans

- [Retirement](./retirement.md) — Similar target approach with divisor
- [Pro](./pro.md) — Aggressive recovery with profit target
- [6 Point Divisor](./6-point-divisor.md) — Divisor-based target plan

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
