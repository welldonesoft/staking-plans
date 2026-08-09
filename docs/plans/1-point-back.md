---
id: 1-point-back
name: 1 Point Back
category: back
type: flat
risk: low
betfair_compatible: true
aliases:
source: tsm
  - One Point Back
---

# 1 Point Back Staking Plan

## Overview

A minimalist staking plan using a single unit (1 point) for every back bet. The simplest possible approach — identical to level stakes with a unit of 1.

## How It Works

Bet exactly 1 point on every selection. Track profit/loss in points rather than currency. The absolute simplest staking plan possible.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `point_value` | number | 1 | The monetary value of 1 point (for currency conversion) |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** 1 point × consecutive losses
- **Recommended Bankroll:** 20–50 points
- **Ruin Risk:** Very low

## When to Use

- Absolute beginners
- Testing a new selection system
- You want to track in points, not currency

## When to Avoid

- You want any kind of compounding or progression
- Your bankroll is very small relative to point value

## Betfair Exchange Notes

- Works identically for back and lay (1 point lay means 1 point stake, liability varies)
- Ideal for testing systems on exchange before committing real money

## Related Plans

- [Level Stakes](./level-stakes.md) — Same concept, explicit currency amount
- [Lay 1 Point](./lay-1-point.md) — Lay equivalent

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
