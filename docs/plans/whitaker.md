---
id: whitaker
name: Whitaker Staking Plan
category: back
type: hybrid
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Whittaker
  - Whitaker System
---

# Whitaker Staking Plan

## Overview

A conservative staking plan combining flat staking with small incremental increases. Increase stake by a small amount after each winner, never decrease. Designed for steady, low-risk growth without the volatility of progression systems.

## How It Works

- Start with a base stake
- After each **winning** bet, increase the stake by a small fixed amount
- **Never decrease** the stake — even after losses
- Growth is slow but one-directional

**Example:** £10 base, £0.50 increment. After first win, stake = £10.50. After second win, stake = £11.00. Losses do not reduce the stake.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting stake |
| `increment` | number | 0.50 | Increase amount after each win |
| `increment_type` | string | "fixed" | "fixed" (absolute) or "percentage" |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** Similar to level stakes — stakes never escalate due to losses
- **Recommended Bankroll:** 30–50× base stake
- **Ruin Risk:** Very low — no negative progression

## When to Use

- Very long-term betting with consistent small edge
- You want gradual, sustainable growth
- Psychological comfort: stakes only ever go up (with wins) or stay flat

## When to Avoid

- Short-term or aggressive growth goals
- Your win rate is very low (increments are too infrequent)

## Betfair Exchange Notes

- Works well for both back and lay
- For lay betting, ensure the increment applies to a manageable metric (stake or liability, not both)

## Related Plans

- [Lay Whitaker](./lay-whitaker.md) — Lay-specific variant
- [Level Stakes](./level-stakes.md) — Same but without increments
- [Secure](./secure.md) — Another conservative staking plan

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
