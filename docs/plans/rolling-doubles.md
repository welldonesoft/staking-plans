---
id: rolling-doubles
name: Rolling Doubles
category: back
type: accumulator
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Rolling Accumulators
---

# Rolling Doubles

## Overview

A staking plan based on rolling double bets. The stake and any profit from a winning double rolls onto the next double. Capitalizes on consecutive pairs of winners with compounding, but resets after any losing leg.

## How It Works

1. Place a **double** (two selections, both must win)
2. **Both win:** Stake + profit rolls onto the next double
3. **Any loss:** Reset to base stake

The plan exploits clusters of consecutive winning doubles. A few successful rolls can produce significant returns.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting stake for each rolling sequence |
| `max_rolls` | number | 5 | Maximum consecutive rolls before reset |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Base stake × number of failed doubles
- **Recommended Bankroll:** 30+ base stakes
- **Ruin Risk:** Medium — stakes don't escalate after losses, but doubles are low-probability

## When to Use

- Your selections tend to come in pairs/clusters
- You enjoy accumulator-style betting
- You can accept many small losses for occasional large wins

## When to Avoid

- Low strike-rate selections — doubles have squared probability (e.g., 40% each leg = 16% double)
- Bankroll preservation is the priority

## Betfair Exchange Notes

- Rolling doubles on exchange require placing each double sequentially (not as a single bet)
- If the first leg wins, you must manually place the second leg
- Commission applies to each winning leg, reducing compounding effect

## Related Plans

- [Parlay](./parlay.md) — Single-bet rolling (let it ride)
- [1-3-2-6](./1326.md) — Structured progressive staking

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
