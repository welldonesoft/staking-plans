---
id: 2-6-staking
name: 2-6 Staking Plan
category: back
type: progression
risk: medium
betfair_compatible: true
aliases:
  - 2-6 System
  - Two from Six
  - Logic System variant
source: marketfeeder
---

# 2-6 Staking Plan

## Overview

A variation of the Logic System: aim to win 2 bets out of a sequence of 6 before restarting. Each bet in the sequence uses a predefined multiplier. Losses are carried forward into subsequent bets. Designed for backing favourites with reasonable strike rates.

## How It Works

The sequence uses fixed multipliers: **1, 2, 4, 6, 8, 12**

1. Start with a target profit (e.g., 1% of bank = £10)
2. Bet 1: stake to win 1× target. If it wins, you have 1 win towards the goal of 2.
3. Bet 2: stake to win 2× target (plus any carried loss). Continue.
4. **Win 2 bets** → restart the cycle with recalculated target based on new bank.
5. **Reach bet 6 without 2 wins** → restart anyway (accept the loss).

## Formula

$$S_n = \frac{M_n \times T + \sum L}{o_n - 1}$$

Where:
- $S_n$ = stake for bet $n$ in the sequence
- $M_n$ = multiplier for position $n$ (1, 2, 4, 6, 8, 12)
- $T$ = target profit per bet
- $\sum L$ = cumulative losses so far in the cycle
- $o_n$ = decimal odds for bet $n$

## Multiplier Sequence

| Position | Multiplier | Target (T=£10) |
|----------|-----------|-----------------|
| 1 | 1× | £10 |
| 2 | 2× | £20 |
| 3 | 4× | £40 |
| 4 | 6× | £60 |
| 5 | 8× | £80 |
| 6 | 12× | £120 |

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target_pct` | number | 1 | Target profit as % of bank |
| `cycle_length` | number | 6 | Number of bets in sequence |
| `win_target` | number | 2 | Wins needed to restart |
| `multipliers` | number[] | [1,2,4,6,8,12] | Multiplier at each position |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Escalates with losses — multipliers grow, and losses are carried forward
- **Recommended Bankroll:** 200+ units
- **Ruin Risk:** Medium — 6-bet cap limits damage, but losses accumulate within cycles

## When to Use

- Backing favourites with decent strike rates (>33%)
- You want a structured, finite recovery cycle
- You prefer mechanical rules with clear endpoints

## When to Avoid

- Low strike-rate systems (won't hit 2 wins in 6 often)
- Lay betting (not designed for it)
- Initial target above 3% of bank (can wipe out bank quickly)

## Betfair Exchange Notes

- Designed for back betting on favourites
- Not suitable for lay betting
- Commission reduces effective profit per winner — factor into target

## Related Plans

- [Pro](./pro.md) — More aggressive recovery with fixed target per market
- [6 Point Divisor](./6-point-divisor.md) — Another finite-cycle target plan

---

## Sources

- **Plan source:** [MarketFeeder — 2-6 Staking Plan](https://marketfeeder.co.uk/learn/triggers/staking-plan-2-6/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
