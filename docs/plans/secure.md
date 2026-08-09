---
id: secure
name: Secure Staking Plan
category: back
type: flat
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Secure Staking
---

# Secure Staking Plan

## Overview

A very conservative staking plan where the stake is a fixed, very small percentage of the starting bankroll — and **never changes**. Unlike percentage staking, it does not compound growth. Unlike level stakes, it's explicitly tied to bankroll size at the start.

## How It Works

Set a very conservative initial percentage (typically 1% or less). The resulting stake becomes your permanent fixed stake.

$$Stake = Initial\ Bankroll \times Percentage$$

**Example:** £1,000 bankroll at 1% = £10 stake. That £10 is used for every bet, forever, regardless of bankroll changes.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `initial_bankroll` | number | 1000 | Starting bankroll |
| `percentage` | number | 1 | Conservative percentage (1% or less) |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** Very controlled — small fixed stakes
- **Recommended Bankroll:** 100× stake (built into the formula at 1%)
- **Ruin Risk:** Extremely low

## When to Use

- You want the absolute safest staking approach
- Your bankroll is large relative to your goals
- You're risk-averse or new to betting
- Capital preservation is more important than growth

## When to Avoid

- You want meaningful bankroll growth
- Your bankroll is small (1% may be below minimum bet)

## Betfair Exchange Notes

- The simplicity and safety make it ideal for learning exchange betting
- Fixed stakes mean lay liability is predictable at all odds

## Related Plans

- [Level Stakes](./level-stakes.md) — Similar but not explicitly tied to bankroll %
- [Percentage Staking](./percentage-staking.md) — Same concept but recalculates (compounds)
- [Whitaker](./whitaker.md) — Another conservative approach with small increments

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
