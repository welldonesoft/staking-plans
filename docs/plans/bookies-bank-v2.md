---
id: bookies-bank-v2
name: Bookies Bank V2
category: back
type: target-based
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Bookmaker's Bank V2
---

# Bookies Bank V2

## Overview

A modified version of the Bookies Bank staking plan with adjusted divisor rules. The divisor decreases differently after wins and has different reset conditions compared to V1.

## How It Works

Same core concept as Bookies Bank V1 (target-based with divisor) but:
- Divisor reduces by the **odds value** (not by 1) after a win
- Different reset/increment rules when a cycle completes
- May use a dynamic divisor floor

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target` | number | 100 | Profit target |
| `divisor` | number | 4 | Starting divisor |
| `increment` | number | 10 | Target increase per completed cycle |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Slightly different profile from V1 due to divisor rules
- **Recommended Bankroll:** 5× target

## When to Use

- You found V1's divisor rules too aggressive or too conservative
- You want to experiment with divisor variants

## Betfair Exchange Notes

- Same exchange considerations as V1

## Related Plans

- [Bookies Bank](./bookies-bank.md) — Original (V1)
- [Bookies Bank V3](./bookies-bank-v3.md) — Further variant

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
