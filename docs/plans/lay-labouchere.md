---
id: lay-labouchere
name: Lay Labouchere
category: lay
type: negative-progression
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Lay Cancellation System
---

# Lay Labouchere Staking Plan

## Overview

The Labouchere cancellation system adapted for lay betting. Uses a number sequence where each lay stake equals the sum of the first and last numbers. Cross off on winning lays (selection loses), add the stake on losing lays (selection wins).

## How It Works

1. Write a number sequence (e.g., 1-2-3-4, sum = 10 = profit target)
2. Each lay: stake (liability target) = first + last number
3. **Win lay (selection loses):** Cross off first and last numbers
4. **Lose lay (selection wins):** Add the stake to the end of the sequence
5. Clear the sequence = target achieved

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `sequence` | number[] | [1,2,3,4] | Starting number sequence |
| `target_type` | string | "stake" | Whether numbers represent stake or liability |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Sequence grows without bound on losing streaks
- **Recommended Bankroll:** 200+ units
- **Ruin Risk:** High — lay losses add large numbers to the sequence

## ⚠️ Critical Warning

Labouchere for lay betting is extremely dangerous without modifications. Each losing lay adds the stake to the sequence, but the actual loss is stake × (odds−1). This means the sequence understates the true financial damage. **Use a liability-based sequence** and limit sequence length.

## Betfair Exchange Notes

- **Strongly recommend** using the sequence to represent liability targets, not stake amounts
- Consider a maximum sequence length (e.g., stop and reset at 10 numbers)

## Related Plans

- [Labouchere](./labouchere.md) — Back betting original
- [Lay Ladder](./lay-ladder.md) — Less aggressive alternative
- [Lay Maria](./lay-maria.md) — Alternative lay recovery

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
