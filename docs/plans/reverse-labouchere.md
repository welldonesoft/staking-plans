---
id: reverse-labouchere
name: Reverse Labouchere
category: back
type: positive-progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Reverse Cancellation
  - Anti-Labouchere
---

# Reverse Labouchere

## Overview

The positive-progression mirror of the Labouchere system: instead of crossing off numbers after wins, you **add** the stake to the sequence after wins. Cross off after losses. This means your stakes grow during hot streaks and shrink during cold ones — the opposite of standard Labouchere.

## How It Works

1. Write a starting sequence (e.g., 1-2-3)
2. Each bet: stake = first + last number
3. **Win:** Add the stake amount to the **end** of the sequence
4. **Loss:** Cross off the first and last numbers
5. When the sequence is empty (all numbers crossed off from losses), accept the loss and restart

**Example (1-2-3, even-money):**
- Bet 1: stake = 1+3 = 4. Win → sequence becomes 1-2-3-4
- Bet 2: stake = 1+4 = 5. Win → 1-2-3-4-5
- Bet 3: stake = 1+5 = 6. Lose → cross 1 and 5 → 2-3-4
- Bet 4: stake = 2+4 = 6. Win → 2-3-4-6

The sequence grows on wins (compounding hot streaks) and shrinks on losses (limiting damage).

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `sequence` | number[] | [1,2,3] | Starting number sequence |
| `cap` | number | — | Optional maximum sequence length |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** The initial sequence sum (e.g., 1+2+3 = 6 units). Losses shrink the sequence.
- **Recommended Bankroll:** 10× initial sequence sum
- **Ruin Risk:** Low — you only lose the initial sequence, and it shrinks during losses

## When to Use

- Your winners cluster in streaks
- You want a positive progression with more structure than Paroli
- You enjoy the sequence-based mechanics

## When to Avoid

- Isolated winners (sequence never grows meaningfully)
- You find sequence tracking tedious

## Comparison: Labouchere vs Reverse

| | Labouchere | Reverse Labouchere |
|---|---|---|
| After win | Cross off numbers | **Add** to sequence |
| After loss | Add to sequence | **Cross off** numbers |
| Stakes during hot streak | Shrink | **Grow** |
| Stakes during cold streak | Grow | **Shrink** |
| Risk | High | Medium |

## Betfair Exchange Notes

- For lay Reverse Labouchere, track sequence based on liability rather than stake
- Commission reduces the effective addition to the sequence after wins

## Related Plans

- [Labouchere](./labouchere.md) — Standard (negative progression) version
- [Lay Labouchere](./lay-labouchere.md) — Lay-specific standard Labouchere
- [Paroli](./paroli.md) — Simpler positive progression (just double, no sequence)

---

## Sources

- **Plan mechanics:** Classic betting system (public domain)
- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
