---
id: bookies-bank
name: Bookies Bank
category: back
type: target-based
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Bookmaker's Bank
---

# Bookies Bank Staking Plan

## Overview

A target-based staking plan designed to capture the "bookmaker's margin" — aiming for steady, consistent profit. Uses a divisor system that resets after reaching the target, then starts a new cycle with an increased target.

## How It Works

1. Set a target and divisor. Stake = Target / Divisor.
2. **Win:** Reduce target by profit. Reduce divisor by the odds of the winner (or 1).
3. **Loss:** Add stake to target. Divisor unchanged.
4. When target ≤ 0, the bank is "broken." Reset with new (potentially higher) target.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target` | number | 100 | Initial profit target |
| `divisor` | number | 4 | Starting divisor |
| `increment` | number | 10 | Amount to increase target after each completed cycle |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Moderate — target inflation after losses
- **Recommended Bankroll:** 5× target
- **Ruin Risk:** Medium

## When to Use

- You want methodical, structured profit accumulation
- You're willing to follow a multi-cycle approach
- Medium-term betting goals

## When to Avoid

- Quick profit expectations (cycles can be long with low strike rates)
- Small bankrolls relative to target

## Variants

The Staking Machine includes three versions:
- **Bookies Bank (V1)** — Standard divisor plan
- **Bookies Bank V2** — Modified divisor adjustment rules
- **Bookies Bank V3** — Different reset and increment mechanics

## Betfair Exchange Notes

- Commission delays reaching the target — factor into planning
- Works for both back and lay

## Related Plans

- [Bookies Bank V2](./bookies-bank-v2.md) — Variant with modified rules
- [Bookies Bank V3](./bookies-bank-v3.md) — Variant with different increment mechanics
- [Retirement](./retirement.md) — Simpler divisor-based plan
- [6 Point Divisor](./6-point-divisor.md) — Related divisor plan

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
