---
id: lay-whitaker
name: Lay Whitaker
category: lay
type: hybrid
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Lay Whittaker
---

# Lay Whitaker Staking Plan

## Overview

The lay betting adaptation of the Whitaker staking plan. A conservative approach: stake increases by a small fixed amount after each winning lay bet, and never decreases. Designed for steady, low-risk lay betting growth.

## How It Works

- Start with a base lay stake
- After each **winning** lay (selection loses): Increase stake by a small increment
- After each **losing** lay (selection wins): Stake stays the same (never decreases)
- Growth is slow but one-directional

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting lay stake |
| `increment` | number | 0.50 | Amount to increase after each winning lay |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** Similar to lay level stakes — no escalation after losses
- **Recommended Bankroll:** 30–50× base stake
- **Ruin Risk:** Very low

## When to Use

- Conservative lay betting approach
- Long-term, slow bankroll building
- You want something slightly more dynamic than flat lay staking

## When to Avoid

- Quick growth expectations
- You want to capitalize on hot streaks more aggressively

## Betfair Exchange Notes

- For lay betting, ensure the increment is manageable at your typical lay odds
- Consider whether the increment applies to stake or liability

## Related Plans

- [Whitaker](./whitaker.md) — Back betting original
- [Lay Level](./lay-level.md) — Even simpler (no increments)
- [Lay Percentage](./lay-percentage.md) — Proportional alternative

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
