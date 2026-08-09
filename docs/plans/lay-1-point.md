---
id: lay-1-point
name: Lay 1 Point
category: lay
type: flat
risk: low
betfair_compatible: true
aliases:
source: tsm
  - One Point Lay
---

# Lay 1 Point Staking Plan

## Overview

The simplest lay staking plan: bet exactly 1 point on every lay selection. The lay equivalent of 1 Point Back — minimalist, predictable, and ideal for testing or tracking.

## How It Works

Lay exactly 1 point on every selection. Track results in points. Convert to currency by setting a point value.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `point_value` | number | 10 | Monetary value of 1 point |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** 1 point × odds adjustment × consecutive losses
- **Recommended Bankroll:** 30–50 points

## When to Use

- Testing lay systems
- Minimalist approach to lay betting
- Tracking results in points

## When to Avoid

- You want growth or compounding

## Betfair Exchange Notes

- 1 point lay means 1 point stake (not 1 point liability) — be aware of the liability at your odds
- For safety at higher odds, consider 1 point of liability instead

## Related Plans

- [1 Point Back](./1-point-back.md) — Back equivalent
- [Lay Level](./lay-level.md) — Same concept, explicit currency

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
