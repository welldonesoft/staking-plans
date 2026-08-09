---
id: hollandish
name: Hollandish Staking Plan
category: back
type: negative-progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Dutch System
  - Hollandish System
---

# Hollandish Staking Plan

## Overview

A structured negative progression system that operates in **blocks of 3 bets**. Within each block, the stake stays constant. If a block of 3 produces a net loss, double the stake for the next block. If a block produces a net profit, reset to base. Named after its supposed Dutch origins.

## How It Works

1. Divide bets into blocks of 3
2. Within each block, use the same stake for all 3 bets
3. **After 3 bets — if the block is net negative:** Double the stake for the next block of 3
4. **After 3 bets — if the block is net positive (or break-even):** Reset to base stake
5. A single winning block can recover losses from multiple losing blocks

**Example:** £10 × 3, all lose (−£30). Next: £20 × 3, win 2, lose 1 (+£20 at evens − £20 = £0 break-even). Next: still £20. Next: £20 × 3, win all 3 (+£60). Net: −£30 + £0 + £60 = +£30. Reset.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting stake per bet |
| `block_size` | number | 3 | Number of bets per block |
| `multiplier` | number | 2 | Stake multiplier after a losing block |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Slower escalation than Martingale — doubling only after 3 bets, not after each loss
- **Recommended Bankroll:** 100+ units (to survive 3–4 losing blocks)
- **Ruin Risk:** Medium — slower than Martingale but still exponential over many losing blocks

## When to Use

- Your strike rate is consistent enough that most 3-bet blocks will be profitable
- You want structured progression with built-in "pauses" between escalations
- You prefer block-based thinking over individual bet chasing

## When to Avoid

- Very low strike rates (most blocks will lose, doubling compounds)
- You want simple rules (block tracking adds complexity)

## Betfair Exchange Notes

- For lay betting, consider doubling liability rather than stake
- Block-based approach works well for exchange — less frantic than bet-by-bet adjustments

## Related Plans

- [Martingale](./martingale.md) — Doubles after every loss (faster, more dangerous)
- [Fibonacci](./fibonacci.md) — Moderate negative progression
- [Stepped Time-Based](./stepped-time-staking.md) — Similar block-based thinking, different mechanics

---

## Sources

- **Plan mechanics:** Classic betting system (public domain)
- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
