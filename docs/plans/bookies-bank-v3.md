---
id: bookies-bank-v3
name: Bookies Bank V3
category: back
type: target-based
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Bookmaker's Bank V3
---

# Bookies Bank V3

## Overview

A further variant of the Bookies Bank staking plan with different increment and reset mechanics. Designed for more aggressive compounding across cycles compared to V1 and V2.

## How It Works

Same core concept as Bookies Bank V1/V2 but:
- Different target increment calculation after cycle completion
- Modified reset conditions
- May incorporate a "ratchet" mechanism where targets never decrease

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target` | number | 100 | Profit target |
| `divisor` | number | 4 | Starting divisor |
| `increment_type` | string | "compound" | How targets grow ("compound", "fixed", "percentage") |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Depends on configuration
- **Recommended Bankroll:** 5× target

## When to Use

- More aggressive compounding goals
- You've tested V1/V2 and want different mechanics

## Betfair Exchange Notes

- Same exchange considerations as V1

## Related Plans

- [Bookies Bank](./bookies-bank.md) — Original (V1)
- [Bookies Bank V2](./bookies-bank-v2.md) — V2 variant
- [Coup Master](./coup-master.md) — Similar compounding target approach

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
