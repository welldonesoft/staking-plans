---
id: recovery-type-3
name: Recovery Type 3
category: back
type: recovery
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Recovery V3
---

# Recovery Type 3

## Overview

A third variant of the Recovery staking plan with further modified recovery mechanics. Incorporates a divisor-style calculation for even more controlled loss recovery compared to Types 1 and 2.

## How It Works

1. Uses a divisor to spread target recovery across bets
2. After a loss, lost amount is added to a recovery pool
3. Recovery pool is divided by a configurable divisor for the next stake
4. Wins reduce the recovery pool; pool empty = reset to base

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting stake |
| `divisor` | number | 4 | Controls how aggressively to recover |
| `max_divisor` | number | 10 | Maximum divisor (caps stake size) |

## Risk Assessment

- **Risk Level:** High (most controlled of the three Recovery types)
- **Max Drawdown:** Limited by divisor — slower escalation
- **Recommended Bankroll:** 200+ units
- **Ruin Risk:** High — still chases losses

## When to Use

- You want the most controlled version of recovery staking
- You accept loss-chasing with built-in speed limits

## When to Avoid

- You haven't thoroughly tested it with your system's historical data
- You're risk-averse (use a non-recovery plan)

## Comparison: Recovery Types

| | Type 1 | Type 2 | Type 3 |
|---|---|---|---|
| Recovery speed | Fastest | Medium | Slowest |
| Stake escalation | Highest | Medium | Lowest |
| Risk | Highest | High | High (controlled) |
| Mechanism | Full recovery next bet | Fractional recovery | Divisor-based recovery |

## Betfair Exchange Notes

- Type 3's divisor approach is the most suitable for lay betting among Recovery variants
- Still exercise caution with lay liability

## Related Plans

- [Recovery](./recovery.md) — Type 1 (fastest)
- [Recovery Type 2](./recovery-type-2.md) — Type 2 (medium)
- [6 Point Divisor](./6-point-divisor.md) — Related divisor concept

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
