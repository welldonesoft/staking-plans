---
id: ratchet-lay
name: Ratchet Staking Plan (Lay)
category: lay
type: positive-progression
risk: medium
betfair_compatible: true
aliases:
  - Lay Ratchet
  - Ratchet Lay Staking
source: marketfeeder
---

# Ratchet Staking Plan (Lay)

## Overview

A lay staking plan that only increases stakes — never decreases. The "ratchet" mechanism: every time your bank balance reaches a new high, the stake ratchets up. During drawdowns, stakes stay flat (they never go down). Designed for conservative, one-directional growth.

## How It Works

1. Divide your bank into a number of "points" (e.g., 100 points)
2. Each point = Bank ÷ number of points
3. Bet 1 point per selection
4. **Bank increases →** Points increase → stakes increase (ratchet up)
5. **Bank decreases →** Stakes stay at the last high level (never ratchet down)
6. Reset only at profit target or stop-loss

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `num_points` | number | 100 | Number of points to divide bank into |
| `liability_mode` | boolean | true | Use liability (true) or stake (false) |
| `stop_profit` | number | — | Maximum profit then stop |
| `stop_loss` | number | — | Maximum loss then stop |
| `max_odds` | number | 10 | Maximum lay odds |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Stakes don't decrease — sustained losses at elevated stakes hurt more
- **Recommended Bankroll:** 100× point value
- **Ruin Risk:** Medium — the ratchet never releases, but growth is slow

## When to Use

- Long-term, conservative lay betting
- You want automatic compounding without manual recalculation
- You prefer the psychological comfort of "stakes only go up"

## When to Avoid

- You want stakes to decrease during losing runs (use percentage staking)
- Short-term trading (ratchet takes time to build)

## Betfair Exchange Notes

- Two modes: **fixed liability** (recommended) or **fixed stake**
- Fixed liability mode: you always know your maximum loss per bet
- The ratchet applies to whichever mode you choose

## Comparison: Ratchet vs Percentage Staking

| | Ratchet | % Staking |
|---|---|---|
| After win | Stake increases | Stake increases |
| After loss | Stake stays flat | Stake decreases |
| Recovery | Slow (no reduction) | Automatic |
| Psychology | Positive (only up) | Neutral |

## Related Plans

- [Whitaker](./whitaker.md) — Similar philosophy (never decrease), different mechanics
- [Lay Whitaker](./lay-whitaker.md) — Lay version of Whitaker
- [Lay % Liability](./lay-percentage-liability.md) — Proportional alternative (goes down on losses)

---

## Sources

- **Plan source:** [MarketFeeder — Ratchet Lay Staking](https://marketfeeder.co.uk/learn/triggers/ratchet-lay/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
