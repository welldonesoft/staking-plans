---
id: each-way-combined
name: Each-Way Combined Staking
category: each-way
type: proportional
risk: medium
betfair_compatible: false
aliases:
source: tsm
  - EW Combined
---

# Each-Way Combined Staking Plan

## Overview

A proportional staking plan for each-way betting where the stake adjusts based on bankroll and the relationship between win and place odds. The combined stake is calculated to optimize returns across both portions.

## How It Works

Rather than splitting the stake equally between win and place, the Combined plan adjusts the allocation based on:
- Current bankroll
- Win odds
- Place terms and place odds
- Relative value between win and place markets

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `total_stake_pct` | number | 5 | Total outlay as % of bankroll |
| `win_weight` | number | 0.6 | Proportion of total stake on win portion |
| `place_terms` | string | "1/4 1-2-3" | Place fraction and number of places |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Proportional to bankroll — self-adjusting
- **Recommended Bankroll:** 20× total outlay

## When to Use

- You want to optimize each-way stake allocation
- Your selections have different win/place profiles
- You prefer proportional staking

## When to Avoid

- Simplicity is important (use Each-Way Level)
- You're new to each-way betting

## Each-Way Specific Notes

- The win/place allocation ratio is the key parameter — it determines how much goes on each portion
- At long odds, place returns become more important; at short odds, win returns dominate
- Some configurations allocate more to place when place terms are generous

## Betfair Exchange Notes

- Each-way betting is primarily a bookmaker product
- Simulating on exchange requires separate win and place market bets

## Related Plans

- [Each-Way Level](./each-way-level.md) — Simpler flat approach
- [Percentage Staking](./percentage-staking.md) — Back-only proportional equivalent

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
