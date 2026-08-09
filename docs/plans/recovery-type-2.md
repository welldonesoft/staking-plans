---
id: recovery-type-2
name: Recovery Type 2
category: back
type: recovery
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Recovery V2
---

# Recovery Type 2

## Overview

A variant of the Recovery staking plan with modified rules for stake calculation after losses. Provides an alternative recovery pattern — designed to spread recovery across multiple bets rather than aiming for a single recovery win.

## How It Works

Similar to standard Recovery but with different loss-absorption mechanics:

1. After a loss, the next stake recovers a **portion** of the loss (not all)
2. Recovery is spread across the next few bets
3. This makes stake escalation slower than standard Recovery

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting stake |
| `recovery_fraction` | number | 0.5 | Portion of loss to recover per bet (0–1) |
| `max_recovery_bets` | number | 5 | Maximum bets to spread recovery over |

## Risk Assessment

- **Risk Level:** High (but lower than standard Recovery)
- **Max Drawdown:** Slower escalation than Recovery V1
- **Recommended Bankroll:** 300+ units
- **Ruin Risk:** High — still chases losses, just more gradually

## When to Use

- You want recovery staking but find standard Recovery too aggressive
- You prefer spreading recovery across multiple bets

## When to Avoid

- Same cautions as standard Recovery — loss-chasing is inherently dangerous
- You don't have a stop-loss in place

## Betfair Exchange Notes

- For lay betting, apply recovery fraction to liability recovery, not stake
- Still risky for lay — consider [Lay % Recovery](./lay-percentage-recovery.md)

## Related Plans

- [Recovery](./recovery.md) — Original (more aggressive)
- [Recovery Type 3](./recovery-type-3.md) — Another variant
- [Stop at a Winner](./stop-at-a-winner.md) — Reset on any winner

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
