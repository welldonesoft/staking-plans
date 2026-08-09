---
id: labouchere
name: Labouchere
category: back
type: negative-progression
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Cancellation System
  - Split Martingale
  - American Progression
---

# Labouchere Staking Plan

## Overview

A sequence-based negative progression system. You define a sequence of numbers representing your profit target. Each bet stakes the sum of the first and last numbers. Cross them off on wins, add the stake on losses. Clear the sequence = profit target achieved.

## How It Works

1. Write down a sequence of numbers (e.g., 1-2-3-4) — their sum ($10) is your profit target
2. Each bet: stake = **first number + last number** of the sequence
3. **Win:** Cross off the first and last numbers used
4. **Loss:** Add the stake amount to the end of the sequence
5. Repeat until the sequence is empty (target reached) or you run out of bankroll

**Example (1-2-3-4, target = 10 units):**
- Bet 1: stake = 1+4 = 5. Lose → sequence becomes 1-2-3-4-5
- Bet 2: stake = 1+5 = 6. Win → cross off 1 and 5 → 2-3-4
- Bet 3: stake = 2+4 = 6. Win → cross off → 3
- Bet 4: stake = 3. Win → empty → profit target achieved

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `sequence` | number[] | [1,2,3,4] | The starting number sequence |
| `target` | number | 10 | Total profit target (sum of initial sequence) |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Severe — long losing streaks add many numbers, inflating stakes rapidly
- **Recommended Bankroll:** 200+ units
- **Ruin Risk:** High — sequence can grow without bound during long losing streaks

## When to Use

- You have a specific profit target in mind
- You can tolerate significant volatility
- Your system has a reasonable strike rate (40%+)

## When to Avoid

- Small bankrolls — the sequence grows quickly after consecutive losses
- Low strike-rate systems — sequence expands too fast
- You lack discipline to follow the sequence mechanically

## Betfair Exchange Notes

- For lay betting, the sequence grows dangerously: adding lay stakes to the sequence means future liability compounds
- Consider using a **reverse Labouchere** for lay betting (increase on wins, decrease on losses) — see [Lay Labouchere](./lay-labouchere.md)

## Related Plans

- [Fibonacci](./fibonacci.md) — Fixed sequence, similar risk profile
- [Lay Labouchere](./lay-labouchere.md) — Lay-specific variant
- [Reverse Labouchere](./parlay.md) — Positive progression version (add on wins, cross on losses)

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
