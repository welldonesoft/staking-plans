---
id: xyz
name: XYZ Staking Plan
category: back
type: custom
risk: variable
betfair_compatible: true
aliases:
source: tsm
  - XYZ Custom Staking
---

# XYZ Staking Plan

## Overview

A highly customizable staking plan with "infinite settings" — allowing the user to define custom stake progression rules along three axes (X, Y, Z). The flexibility makes it adaptable to almost any betting style but requires careful configuration.

## How It Works

The plan uses three configurable parameters:
- **X:** Base stake or percentage
- **Y:** Progression rule (increase after loss/win, amount, cap)
- **Z:** Reset condition (after win, after target reached, after N bets)

Because of infinite configurability, XYZ can mimic many other staking plans or create entirely custom approaches.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `X` | number/string | — | Base stake (fixed or % of bankroll) |
| `Y_rule` | string | — | Progression direction and amount |
| `Y_step` | number | — | Size of each progression step |
| `Z_condition` | string | — | Reset trigger |

## Risk Assessment

- **Risk Level:** Variable (depends entirely on configuration)
- **Max Drawdown:** Configurable through caps and reset rules
- **Recommended Bankroll:** Depends on configuration

## When to Use

- You have a specific, custom staking strategy in mind
- You want to experiment with different progression rules
- No existing plan fits your exact needs

## When to Avoid

- You're looking for a simple, predefined plan
- You don't fully understand the implications of your configuration (easy to create a dangerous setup)

## Betfair Exchange Notes

- XYZ can be configured for back or lay betting
- For lay, ensure Y rules operate on liability, not stake

## Related Plans

- [Lay XYZ](./lay-xyz.md) — Lay-specific variant

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
