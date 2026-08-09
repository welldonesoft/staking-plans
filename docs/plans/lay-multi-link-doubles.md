---
id: lay-multi-link-doubles
name: Lay Multi-Link Doubles
category: lay
type: cycle-based
risk: medium
betfair_compatible: true
aliases:
  - Lay Cycle Doubles
source: marketfeeder
---

# Lay Multi-Link Doubles Plan

## Overview

The lay betting adaptation of the Multi-Link Doubles plan. Uses the same cycle-based decreasing-percentage structure, but for lay bets with liability-based sizing. Winning lay profits are partially redistributed across remaining bets in the cycle.

## How It Works

1. Cycle of N bets with decreasing liability percentages
2. Bet 1: 5% of starting bank as liability
3. Bet 2: 4% of starting bank + fraction of Bet 1's profit
4. Continue decreasing to Bet N: 1% + accumulated winnings
5. Cycle restarts with new bank

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `starting_bank` | number | — | Bank at cycle start |
| `cycle_length` | number | 6 | Number of bets per cycle |
| `starting_pct` | number | 5 | First liability as % of bank |
| `ending_pct` | number | 1 | Last liability as % of bank |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Decreasing within cycle; liability-based sizing controls risk
- **Recommended Bankroll:** 20× first liability

## When to Use

- Lay strategies with consistent results
- You want structured, cycle-based lay betting

## When to Avoid

- Inconsistent lay strike rates
- You prefer simpler lay plans

## Betfair Exchange Notes

- Liability-based sizing is safer for lay betting
- Commission adjustment built into profit redistribution

## Related Plans

- [Back Multi-Link Doubles](./back-multi-link-doubles.md) — Back equivalent
- [Lay Accumulator](./lay-accumulator.md) — Positive progression alternative

---

## Sources

- **Plan source:** [MarketFeeder — Lay Multi-Link Doubles](https://marketfeeder.co.uk/learn/triggers/lay-multi-link-doubles/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
