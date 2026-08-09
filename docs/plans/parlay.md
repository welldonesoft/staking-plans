---
id: parlay
name: Parlay
category: back
type: positive-progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Let It Ride
  - Accumulator Staking
  - Paroli (Reverse Martingale)
---

# Parlay Staking Plan

## Overview

A positive progression where you reinvest winnings into the next bet — "let it ride." After a win, stake the original stake **plus** the profit on the next selection. After a loss, return to base stake. The goal is to compound during winning streaks.

## How It Works

- Start with your base unit
- **Win:** Stake = previous stake + profit from that win
- **Loss:** Reset to base unit
- Optionally set a cap (e.g., stop parlaying after 3 consecutive wins)

**Example (3-win streak at 2.0 odds, £10 base):**
1. Bet £10 at 2.0 → win £10 profit → bank +£10
2. Bet £20 at 2.0 → win £20 → bank +£30
3. Bet £40 at 2.0 → win £40 → bank +£70
4. Reset to £10

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting stake |
| `max_steps` | number | 3 | Maximum consecutive parlays before reset |
| `odds_min` | number | — | Minimum odds to parlay (optional filter) |

## Risk Assessment

- **Risk Level:** Medium (controlled by max_steps)
- **Max Drawdown:** Base stake per losing bet (no escalation after losses)
- **Recommended Bankroll:** 20× base stake
- **Ruin Risk:** Low — you never chase losses

## When to Use

- Your selections tend to cluster in winning streaks
- You want to compound during hot runs without chasing losses
- You prefer conservative money management (never increase after losses)

## When to Avoid

- Your winners are isolated (no streaks) — you'll rarely benefit from compounding
- Low strike rate — you'll mostly reset to base without compounding
- High odds selections — parlaying high-odds wins compounds risk dramatically

## Betfair Exchange Notes

- Parlaying on exchange is straightforward: manually place the next bet with the compounded amount
- Commission reduces the effective compounding — each win is taxed, so the parlay amount is slightly less than full reinvestment
- For lay parlays, you parlay the **profit** (not the liability), making it safer

## Related Plans

- [1-3-2-6](./1326.md) — Structured positive progression with predefined sequence
- [Rolling Doubles](./rolling-doubles.md) — Parlay variant for doubles

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
