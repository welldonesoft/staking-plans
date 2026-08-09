---
id: each-way-level
name: Each-Way Level Stakes
category: each-way
type: flat
risk: low
betfair_compatible: false
aliases:
source: tsm
  - EW Level
  - Each Way Flat Staking
---

# Each-Way Level Stakes

## Overview

Flat staking for each-way bets — the same fixed amount on both the win and place portions of every each-way bet. The simplest approach to each-way staking.

## How It Works

An each-way bet is two bets in one:
1. **Win portion:** Stakes on the selection to win
2. **Place portion:** Stakes on the selection to place (typically 1/4 or 1/5 odds for top 3–4)

With each-way level staking, both portions use the same fixed stake.

**Example:** £5 each-way = £5 on win + £5 on place = £10 total outlay. Both portions are fixed, every bet.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `ew_stake` | number | 5 | Stake for each portion (win AND place) |
| `place_terms` | string | "1/4 1-2-3" | Place fraction and number of places |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** Total outlay × consecutive losses (each-way = 2× stake per bet)
- **Recommended Bankroll:** 40× total outlay per bet
- **Ruin Risk:** Low

## When to Use

- Beginner each-way betting
- Consistent, predictable staking
- Testing each-way selection systems

## When to Avoid

- You want to vary stake between win and place portions
- You want compounding

## Each-Way Specific Notes

- Total outlay per bet = 2 × ew_stake (win + place)
- Place returns depend on place terms (1/4 odds for top 3 is common in UK horse racing)
- Both portions can win (selection wins), one can win (selection places), or both can lose

## Betfair Exchange Notes

- Each-way betting is primarily a bookmaker product, not natively available on Betfair Exchange
- You can simulate each-way on exchange by placing separate back bets on win and place markets, but place markets have limited liquidity

## Related Plans

- [Each-Way Combined](./each-way-combined.md) — Proportional each-way approach
- [Level Stakes](./level-stakes.md) — Back-only equivalent

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
