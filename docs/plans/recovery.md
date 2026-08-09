---
id: recovery
name: Recovery Staking Plan
category: back
type: recovery
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Loss Recovery
---

# Recovery Staking Plan

## Overview

A straightforward recovery plan: after any loss, increase the next stake to recover the lost amount. The goal is to return to the starting position after every loss, plus earn a small target profit.

## How It Works

1. Start with a base stake
2. **Win:** Reset to base stake (cycle complete)
3. **Loss:** Next stake = (previous stake + loss amount) / (odds − 1), aiming to recover everything in one bet

**Example:** £10 base at 2.0 odds. Lose £10. Next stake = £10 (to win £10 back). Lose again (£20 total loss). Next stake = £20. Win → recover all £30 lost + base profit.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting stake |
| `target_profit` | number | 0 | Additional profit per cycle (optional) |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Exponential growth during losing streaks
- **Recommended Bankroll:** 500+ units
- **Ruin Risk:** High — pure loss-chasing without caps

## When to Use

- Very high strike rate (>60%)
- Large bankroll
- Short-term use with strict stop-loss

## ⚠️ Critical Warning

Unchecked recovery staking is one of the most dangerous approaches. Without a stop-loss or maximum stake cap, a long losing streak will deplete any bankroll. **Always set a maximum number of recovery steps.**

## Betfair Exchange Notes

- For lay betting, recovery staking is extremely dangerous — liability grows with both the recovery amount and the odds
- See [Lay % Recovery](./lay-percentage-recovery.md) for a slightly safer lay variant

## Related Plans

- [Pro](./pro.md) — Similar recovery with fixed target profit
- [Stop at a Winner](./stop-at-a-winner.md) — Recovery that stops after any winner
- [Recovery Type 2](./recovery-type-2.md) — Variant
- [Recovery Type 3](./recovery-type-3.md) — Variant

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
