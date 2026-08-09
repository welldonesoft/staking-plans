---
id: 6-point-divisor
name: 6 Point Divisor Plan
category: back
type: target-based
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Six Point Divisor
  - 6 Point Plan
---

# 6 Point Divisor Staking Plan

## Overview

A target-based staking plan using a divisor that starts at 6. After each win, the divisor decreases. After consecutive losses, the divisor can increase to manage stake escalation. Balances recovery with bankroll protection.

## How It Works

1. Set a profit target. Divisor starts at 6.
2. Stake = Target / Divisor
3. **Win:** Target reduces by profit. Divisor reduces by 1 (minimum 2).
4. **Loss (after 2+ consecutive losses):** Target increases by lost stake. Optionally increase divisor to 6 again to cap stake growth.

## Formula

$$S = \frac{T}{D}$$

Where $D$ adjusts:
- Start: $D = 6$
- After win: $D = \max(D - 1, 2)$
- After sustained losses: $D$ may reset to 6 (cap mechanism)

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target` | number | 60 | Profit target |
| `divisor` | number | 6 | Starting divisor |
| `min_divisor` | number | 2 | Minimum divisor |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Controlled — divisor reset caps stake escalation
- **Recommended Bankroll:** 5–10× target
- **Ruin Risk:** Medium-low — more controlled than Retirement plan

## When to Use

- You want target-based staking with built-in safety mechanisms
- You prefer structured plans with clear rules
- Your system has moderate strike rate and odds

## When to Avoid

- Very low strike rates — frequent divisor resets mean slow progress
- You prefer simpler plans

## Betfair Exchange Notes

- Works for both back and lay
- For lay betting, use liability as the basis for target and stake calculations

## Related Plans

- [Retirement](./retirement.md) — Similar divisor plan without the 6-point mechanism
- [Bookies Bank](./bookies-bank.md) — Another divisor-based target plan

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
