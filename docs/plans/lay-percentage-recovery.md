---
id: lay-percentage-recovery
name: Lay % Recovery
category: lay
type: recovery
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Lay Percentage Recovery
---

# Lay % Recovery Staking Plan

## Overview

A lay recovery plan that escalates stakes as a percentage of the loss amount (rather than full recovery). After a losing lay, the next stake aims to recover a percentage of the loss, making it less aggressive than full recovery systems.

## How It Works

1. Start with a base lay stake
2. **Lose (selection wins):** Next stake aims to recover X% of the loss
3. **Win (selection loses):** Reset or step down
4. The recovery percentage (e.g., 50%) controls aggression

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting lay stake |
| `recovery_pct` | number | 50 | Percentage of loss to recover per step |
| `max_steps` | number | 8 | Maximum recovery steps before forced reset |

## Risk Assessment

- **Risk Level:** High (but lower than full recovery)
- **Max Drawdown:** Partial recovery = slower escalation
- **Recommended Bankroll:** 200+ units

## When to Use

- You want recovery staking but find full recovery too aggressive
- Your lay system has moderate strike rate

## When to Avoid

- Still a recovery plan — all the standard warnings apply
- You don't have a max_steps limit

## Betfair Exchange Notes

- Recovery percentage applies to the **financial loss** (liability paid out), not the stake
- A 50% recovery after losing £100 liability means next bet aims to win £50

## Related Plans

- [Lay Maria](./lay-maria.md) — More aggressive lay recovery
- [Recovery](./recovery.md) — Back betting equivalent

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
