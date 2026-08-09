---
id: lay-maria-liability
name: Lay Maria Liability
category: lay
type: recovery
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Maria Liability Plan
---

# Lay Maria Liability Staking Plan

## Overview

A safer variant of Lay Maria that operates on **liability** rather than stake. After a loss, the liability escalates — but stakes are calculated to keep liability controlled. More predictable risk than standard Lay Maria.

## How It Works

1. Set a base liability (your maximum loss per bet initially)
2. **Lose (selection wins):** Increase the target liability for the next bet
3. **Win (selection loses):** Reduce or reset liability toward base
4. Stake is derived: Stake = Liability / (Odds − 1)

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_liability` | number | 100 | Starting liability per bet |
| `escalation` | number | 1.5 | Liability multiplier after a loss |

## Risk Assessment

- **Risk Level:** High (but more controlled than standard Lay Maria)
- **Max Drawdown:** Predictable — you control liability, not stake
- **Recommended Bankroll:** 50× base liability
- **Ruin Risk:** Medium-high — liability grows, but it's explicit

## When to Use

- You want lay recovery but prefer liability-based control
- Your lay odds vary and you want consistent risk sizing

## When to Avoid

- Standard Lay Maria caveats apply — still a recovery plan
- Use a stop-loss

## Betfair Exchange Notes

- This is the **recommended** version of Lay Maria for exchange betting
- Liability is explicit and manageable

## Related Plans

- [Lay Maria](./lay-maria.md) — Stake-based variant (riskier)
- [Lay % Liability](./lay-percentage-liability.md) — Non-recovery proportional alternative

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
