---
id: level-stakes
name: Level Stakes
category: back
type: flat
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Fixed Stakes
  - Flat Staking
  - Unit Staking
---

# Level Stakes

## Overview

The simplest staking plan: bet the same fixed amount on every selection. No adjustments for confidence, odds, bankroll size, or recent results. Also known as "level staking", "flat staking", or "unit staking".

## How It Works

Choose a fixed monetary amount (your "unit" or "point"). Every bet uses exactly this amount.

```
Stake = Fixed Amount
```

**Example:** £10 per bet, every bet, regardless of anything else.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `stake` | number | 10 | Fixed monetary amount per bet |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** Proportional to losing streak length × stake
- **Recommended Bankroll:** 20–50× stake (£200–£500 for £10 stakes)
- **Ruin Risk:** Very low — can only go broke through prolonged losing at fixed rate

## When to Use

- You're a beginner learning bankroll management
- Your selections have consistent win rates and odds
- You want maximum simplicity and predictability
- You're tracking results in "points" rather than currency

## When to Avoid

- You have a proven edge and want to compound growth
- Your selections vary significantly in confidence/odds
- You want to accelerate recovery after losing streaks

## Betfair Exchange Notes

- Works identically for back and lay betting
- For lay betting, ensure your fixed stake's liability (stake × (odds − 1)) doesn't exceed your comfort zone at higher odds
- No commission adjustment needed — simplicity is the point

## Related Plans

- [Percentage Staking](./percentage-staking.md) — Proportional alternative
- [Fixed Stake](./fixed-stake.md) — Similar concept
- [Lay Level](./lay-level.md) — Lay-specific variant

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
