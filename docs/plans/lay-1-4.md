---
id: lay-1-4
name: Lay 1-4 Staking Plan
category: lay
type: progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Lay 1 to 4
  - Lay One to Four
---

# Lay 1-4 Staking Plan

## Overview

A structured lay progression plan using a sequence from 1 to 4 units. After a losing lay bet, move up the sequence. After a win, move down or reset. Similar in concept to the 1-3-2-6 system but adapted for lay betting with different sequence logic.

## How It Works

Sequence: 1 → 2 → 3 → 4 units

- Start at 1 unit
- **Lose (selection wins):** Move up one step
- **Win (selection loses):** Move down one step or reset
- Reset to 1 after completing the sequence or after a win at step 4

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `unit` | number | 10 | Base unit size |
| `reset_on_win` | boolean | true | Whether to fully reset after a win |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Capped by the 4-unit maximum
- **Recommended Bankroll:** 30+ units

## When to Use

- Structured progression appeals to you
- You want a mechanical, easy-to-follow plan
- Moderate lay strike rates

## When to Avoid

- Very long losing streaks (you'll sit at 4 units for extended periods)
- You prefer flat staking

## Betfair Exchange Notes

- Define your unit in terms of liability for safer lay betting
- A 4-unit lay stake at odds of 10.0 = 36 units of liability — size accordingly

## Related Plans

- [1326](./1326.md) — Back betting sequence plan (different sequence)
- [Lay Ladder](./lay-ladder.md) — Similar concept, user-defined sequence

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
