---
id: back-multi-link-doubles
name: Back Multi-Link Doubles
category: back
type: cycle-based
risk: medium
betfair_compatible: true
aliases:
  - Multi-Link Doubles
  - Cycle Doubles
source: marketfeeder
---

# Back Multi-Link Doubles Plan

## Overview

A cycle-based staking plan where bets are placed in cycles of decreasing percentages of bank. Each winning bet's profit is partially redistributed ("linked") across remaining bets in the cycle, creating a compounding effect within each cycle.

## How It Works

1. A cycle has N bets (default 6)
2. Bet 1: 5% of starting bank
3. Bet 2: 4% of starting bank + fraction of Bet 1's winnings
4. Bet 3: 3% of starting bank + fraction of cumulative winnings
5. Continue down to Bet N: 1% + accumulated winnings
6. Cycle ends → restart with new starting bank

The "linking" means winning profits feed into remaining bets, accelerating growth within each cycle.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `starting_bank` | number | — | Bank at cycle start |
| `cycle_length` | number | 6 | Number of bets per cycle |
| `starting_pct` | number | 5 | First bet as % of starting bank |
| `ending_pct` | number | 1 | Last bet as % of starting bank |

## Percentages Per Step (6-bet cycle)

| Step | Base % of Bank | + Accumulated Winnings |
|------|---------------|----------------------|
| 1 | 5% | — |
| 2 | 4% | + fraction of Step 1 profit |
| 3 | 3% | + fraction of cumulative profit |
| 4 | 2% | + fraction of cumulative profit |
| 5 | 1.5% | + fraction of cumulative profit |
| 6 | 1% | + fraction of cumulative profit |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Decreasing stakes within cycle — later losses hurt less
- **Recommended Bankroll:** 20× first bet size
- **Ruin Risk:** Low-medium — no loss chasing

## When to Use

- Your selections have consistent moderate strike rates
- You want structured cycle-based betting
- You enjoy the mechanics of profit redistribution

## When to Avoid

- Very low strike rates (cycles rarely produce enough winners to link)
- You prefer simple, non-cyclic plans

## Betfair Exchange Notes

- Commission (5%) must be factored into the profit redistribution calculations
- The MarketFeeder implementation includes commission adjustment

## Related Plans

- [Rolling Doubles](./rolling-doubles.md) — Simpler doubles-based approach
- [Parlay](./parlay.md) — Let-it-ride accumulation

---

## Sources

- **Plan source:** [MarketFeeder — Back Multi-Link Doubles](https://marketfeeder.co.uk/learn/triggers/back-multi-link-doubles/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
