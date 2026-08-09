---
id: lay-hipro86-sp4
name: Lay HiPro86 SP4
category: lay
type: recovery
risk: high
betfair_compatible: true
aliases:
source: tsm
  - HiPro86 SP4 Lay
---

# Lay HiPro86 SP4 Staking Plan

## Overview

A specialized lay recovery plan with a specific progression structure. The "SP4" designation refers to a 4-step progression designed for high-probability lay systems. Popularized in betting forums for its structured approach to lay recovery.

## How It Works

Uses a 4-step progression sequence for lay stakes. After each losing lay, move to the next step. After a winning lay, reset or step back. The 4-step limit provides a natural boundary.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `step_stakes` | number[] | [10,25,60,150] | Stakes for each of the 4 steps |
| `reset_policy` | string | "full" | Reset after a win ("full" or "step_back") |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Sum of all 4 steps at worst-case odds
- **Recommended Bankroll:** Must cover 4-step sequence × max liability
- **Ruin Risk:** High — but bounded by the 4-step limit

## When to Use

- High-probability lay systems (implied by the name)
- You want a recovery plan with a hard step limit
- You accept the risk of the 4-step sequence failing

## When to Avoid

- Low lay strike rates — the 4-step limit provides a floor but the stakes are large
- You're uncomfortable with the step sizes

## Betfair Exchange Notes

- Calculate the liability for each step at your typical lay odds
- Step 4 at £150 stake and 5.0 odds = £600 liability — size accordingly

## Related Plans

- [Lay Maria](./lay-maria.md) — Alternative lay recovery
- [Lay Ladder](./lay-ladder.md) — User-defined ladder approach

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
