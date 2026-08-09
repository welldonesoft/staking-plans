---
id: lay-maria
name: Lay Maria
category: lay
type: recovery
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Maria Lay Plan
---

# Lay Maria Staking Plan

## Overview

An aggressive lay recovery staking plan. After a losing lay bet (selection wins), stakes escalate to recover the loss. Named after a popular betting forum strategy, it's designed for high-strike-rate lay systems.

## How It Works

1. Start with a base lay stake
2. **Lose (selection wins):** Increase stake to recover the loss + target profit
3. **Win (selection loses):** Reset or reduce toward base stake
4. The escalation can be aggressive — designed for lay systems with very high strike rates

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting lay stake |
| `recovery_multiplier` | number | 1.5 | How aggressively to escalate after losses |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Significant — lay losses are expensive (liability = stake × (odds−1))
- **Recommended Bankroll:** 500+ units
- **Ruin Risk:** High — escalation compounds with lay liability

## ⚠️ Critical Warning

Lay recovery plans are among the most dangerous staking approaches. A lay loss means you pay out the backer's stake × (odds−1). Escalating after lay losses multiplies an already-large liability. Use extreme caution and tight stop-losses.

## When to Use

- Very high lay strike rate (>80%)
- Low lay odds (<3.0)
- You have a very large bankroll

## When to Avoid

- Lay odds above 5.0 (liability is too large)
- Strike rate below 70%
- You don't have a strict stop-loss

## Betfair Exchange Notes

- Always calculate liability, not stake, when sizing for bankroll
- Consider [Lay Maria Liability](./lay-maria-liability.md) for a liability-based variant

## Related Plans

- [Lay Maria Liability](./lay-maria-liability.md) — Liability-based variant (safer)
- [Lay Ladder](./lay-ladder.md) — More controlled lay progression

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
