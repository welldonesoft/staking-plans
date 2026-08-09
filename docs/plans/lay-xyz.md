---
id: lay-xyz
name: Lay XYZ
category: lay
type: custom
risk: variable
betfair_compatible: true
aliases:
source: tsm
  - Lay Custom Staking
---

# Lay XYZ Staking Plan

## Overview

The lay betting adaptation of the XYZ staking plan. Fully customizable along three axes (X, Y, Z) for lay betting, allowing you to define custom stake progression rules, reset conditions, and base sizing.

## How It Works

Same configurable framework as XYZ but optimized for lay betting:
- **X:** Base lay stake or liability
- **Y:** Progression rule after winning/losing lays
- **Z:** Reset conditions

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `X` | number/string | — | Base size (stake or liability) |
| `Y_rule` | string | — | Progression direction and amount |
| `Z_condition` | string | — | Reset trigger |

## Risk Assessment

- **Risk Level:** Variable (depends on configuration)
- **Max Drawdown:** Configurable

## When to Use

- Custom lay staking strategies
- Experimentation with lay-specific progression rules

## When to Avoid

- You're not experienced with lay betting progression
- You haven't thoroughly tested your configuration

## Betfair Exchange Notes

- **Critical:** Configure Y rules around liability, not stake, unless you fully understand the implications

## Related Plans

- [XYZ](./xyz.md) — Back betting original
- [Lay Kelly](./lay-kelly.md) — Edge-based proportional alternative

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
