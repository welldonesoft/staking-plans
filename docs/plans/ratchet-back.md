---
id: ratchet-back
name: Ratchet Staking Plan (Back)
category: back
type: positive-progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Back Ratchet
  - Ratchet Back Staking
---

# Ratchet Staking Plan (Back)

## Overview

The back-betting version of the Ratchet staking plan. Divide your bank into a fixed number of points. Every time your bank reaches a new high, the point value increases — and stakes ratchet up. During drawdowns, stakes stay flat at their last high. Never goes down.

## How It Works

1. Divide bank into N points (e.g., 100 points = 1% each)
2. Bet 1 point per selection
3. **Bank hits a new high →** Point value increases → Stakes increase (ratchet up)
4. **Bank drops →** Stakes stay at the last level (never ratchet down)
5. Set profit target and stop-loss

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `num_points` | number | 100 | Points to divide bank into |
| `stop_profit` | number | — | Stop at this total profit |
| `stop_loss` | number | — | Stop at this total loss |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Stakes don't decrease during losing runs
- **Recommended Bankroll:** 100× initial point value

## When to Use

- Long-term, conservative growth (back betting)
- You like the psychology of "stakes only go up"

## When to Avoid

- You want stakes to decrease during drawdowns (use percentage staking)

## Comparison: Ratchet Back vs Ratchet Lay

The mechanism is identical; the difference is whether you bet back or lay. Both use the same points-based ratchet logic.

## Betfair Exchange Notes

- For back betting, the stake IS your liability — simpler than lay ratchet
- Works naturally with exchange back bets

## Related Plans

- [Ratchet Lay](./ratchet-lay.md) — Lay equivalent
- [Whitaker](./whitaker.md) — Similar "never decrease" philosophy, different mechanics

---

## Sources

- **Plan mechanics:** Classic betting system (public domain)
- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
