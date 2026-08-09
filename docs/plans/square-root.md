---
id: square-root
name: Square Root Staking
category: back
type: proportional
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Root Staking
---

# Square Root Staking Plan

## Overview

A proportional staking system that scales stake with the **square root** of bankroll growth — slower than percentage staking, faster than level stakes. Provides a middle ground between flat and proportional approaches.

## How It Works

Stake is proportional to √(current bankroll / initial bankroll). When bankroll doubles, stake increases by √2 ≈ 1.41× (not 2× as with percentage staking).

## Formula

$$S_i = S_0 \times \sqrt{\frac{B_i}{B_0}}$$

Where:
- $S_i$ = current stake
- $S_0$ = initial stake
- $B_i$ = current bankroll
- $B_0$ = initial bankroll

**Example:** Start with £10 stakes on £1,000 bankroll. When bankroll = £4,000 (4×), stake = £10 × √4 = £20.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `initial_stake` | number | 10 | Starting stake amount |
| `initial_bankroll` | number | 1000 | Starting bankroll |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Slower recovery than percentage staking, faster than level
- **Recommended Bankroll:** 50× initial stake
- **Ruin Risk:** Low — growth is dampened compared to percentage staking

## When to Use

- You want some compounding but find percentage staking too aggressive
- Long bankroll-building phase expected
- Conservative growth with partial compounding

## When to Avoid

- You have a strong edge and want maximum compounding (use Kelly)
- Simplicity is paramount (use level stakes)

## Comparison

| Staking Plan | Double Bankroll → Stake Multiplier |
|--------------|-------------------------------------|
| Level Stakes | 1.0× (no change) |
| Square Root | 1.41× |
| Percentage (2%) | 2.0× |
| Full Kelly | Variable (edge-dependent) |

## Betfair Exchange Notes

- Works identically for back and lay — use the same formula
- Square root scaling is gentle enough that commission impact is negligible for stake sizing purposes

## Related Plans

- [Percentage Staking](./percentage-staking.md) — Linear proportional staking
- [Kelly Criterion](./kelly-criterion.md) — Optimal edge-based proportional staking
- [Level Stakes](./level-stakes.md) — Zero-growth flat staking

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
