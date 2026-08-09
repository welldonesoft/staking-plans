---
id: lay-ladder
name: Lay Ladder
category: lay
type: progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Lay Staking Ladder
---

# Lay Ladder Staking Plan

## Overview

A structured progression system for lay betting. After each loss, move up the ladder (increase stake). After each win, move down or reset. The ladder is predefined with escalating stake levels.

## How It Works

Define a ladder of stake levels (or liability levels). Start at the bottom:

- **Lose (selection wins):** Move up one rung (higher stake)
- **Win (selection loses):** Move down one or more rungs (lower stake) or reset to bottom

**Example ladder (stakes):** £10 → £15 → £25 → £40 → £65 → £105...

The exact ladder can be fixed amounts, percentages, or follow a sequence (Fibonacci-like).

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `ladder` | number[] | [10,15,25,40,65,105] | The stake ladder sequence |
| `steps_down` | number | 1 | How many rungs to drop after a win |

## Risk Assessment

- **Risk Level:** Medium (depends on ladder design)
- **Max Drawdown:** Controlled by ladder length and step sizes
- **Recommended Bankroll:** Must cover the sum of all ladder rungs
- **Ruin Risk:** Medium — predefined ladder limits runaway escalation

## When to Use

- You want more structure than ad-hoc progression
- Your lay strike rate is reasonable
- You prefer mechanical rules to discretionary staking

## When to Avoid

- The ladder is poorly calibrated to your strike rate and odds
- Your lay selections have very high odds (liability escalates fast)

## Betfair Exchange Notes

- **Recommendation:** Build your ladder based on **liability**, not stake. A stake-based ladder at high odds creates dangerous liability jumps.
- Example liability ladder: £50 → £75 → £125 → £200 → £325...

## Related Plans

- [Fibonacci](./fibonacci.md) — A natural ladder (1,1,2,3,5,8...)
- [Lay Labouchere](./lay-labouchere.md) — Sequence-based lay progression
- [Lay Maria](./lay-maria.md) — More aggressive lay recovery

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
