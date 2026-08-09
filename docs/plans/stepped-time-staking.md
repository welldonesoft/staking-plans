---
id: stepped-time-staking
name: Stepped Time-Based Staking
category: back
type: progression
risk: medium
betfair_compatible: true
aliases:
  - Time-Based Escalation
  - Cycle Count Staking
source: community
---

# Stepped Time-Based Staking

## Overview

A unique staking plan where escalation is based on **time/number of bets** rather than wins or losses. Bet a fixed amount for N races, then increase to the next level for the next N races — always resetting to the base level on any win. Combines flat staking's safety with a gentle incentive to eventually find a winner.

## How It Works

1. Start at **Level 1**: bet 1 unit for up to N races
2. **Win at any point:** Reset to Level 1 (1 unit)
3. **N consecutive losses at Level 1:** Move to Level 2 (2 units) for the next N races
4. **N consecutive losses at Level 2:** Move to Level 3 (3 units)
5. Continue escalating by 1 unit every N losses
6. **Any win at any level:** Immediately reset to Level 1

**Example (N=5):** £1 × 5 races (all lose) → £2 × 5 races (all lose) → £3 × 5 races (win on 3rd) → Reset to £1

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_unit` | number | 1 | Starting stake per bet |
| `bets_per_level` | number | 5 | Number of bets at each level before escalating |
| `increment` | number | 1 | Units to add per level |
| `max_level` | number | — | Optional maximum level cap |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Predictable — each level lasts exactly N bets at a known stake
- **Recommended Bankroll:** (bets_per_level × max_level × (max_level+1) / 2) units
- **Ruin Risk:** Low-medium — escalation is slow and capped if max_level is set

## When to Use

- You want a gradual, predictable escalation pace
- Your strike rate is low but consistent (you WILL hit winners, just not frequently)
- You prefer the psychological comfort of "I have 5 chances at this level"

## When to Avoid

- Very high strike rates (you'll rarely leave Level 1 — might as well use flat staking)
- You want aggressive recovery (this is deliberately slow)

## Comparison: Stepped vs Martingale

| | Stepped Time-Based | Martingale |
|---|---|---|
| After N losses | Stake = N+1 | Stake = 2^N |
| 10 losses in | Stake = 3 (if N=5) | Stake = 1,024 |
| Reset trigger | Any win | Any win |
| Philosophy | Patience | Aggression |

## Betfair Exchange Notes

- Works identically for back and lay
- For lay betting, apply the level to liability rather than stake

## Related Plans

- [Level Stakes](./level-stakes.md) — Flat staking (no escalation)
- [Martingale](./martingale.md) — Aggressive doubling (opposite philosophy)
- [Whitaker](./whitaker.md) — Small increments after wins (different direction)

---

## Sources

- **Plan source:** [WellDone Community Forum — "Back recovery strategy"](https://community.welldonesoft.com/index.php?topic=16579.0) — user-contributed concept by Gordon
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
