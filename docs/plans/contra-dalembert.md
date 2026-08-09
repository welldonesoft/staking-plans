---
id: contra-dalembert
name: Contra D'Alembert
category: back
type: positive-progression
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Reverse D'Alembert
  - Anti-D'Alembert
---

# Contra D'Alembert

## Overview

The mirror image of the classic D'Alembert: increase stake by 1 unit after a **win**, decrease by 1 unit after a **loss**. A positive progression that compounds winnings and shrinks during losing runs. Much safer than standard D'Alembert.

## How It Works

1. Start with 1 unit
2. **Win:** Increase stake by 1 unit
3. **Loss:** Decrease stake by 1 unit (never below 1)
4. No profit target per se — just ride the waves

**Example:** 1 (Win) → 2 (Win) → 3 (Lose) → 2 (Win) → 3 (Lose) → 2 (Lose) → 1

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_unit` | number | 1 | Starting and minimum stake |
| `increment` | number | 1 | Units to change per result |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** Limited — stakes decrease during losses
- **Recommended Bankroll:** 30+ units

## When to Use

- Your winners cluster in streaks
- You want the safety of decreasing stakes when cold
- You prefer positive progression psychology

## When to Avoid

- Isolated winners (rarely build momentum)
- You want a specific profit target mechanic

## Contra vs Standard D'Alembert

| | Standard | Contra |
|---|---|---|
| After win | Decrease | **Increase** |
| After loss | Increase | **Decrease** |
| Risk profile | Medium | Low |
| Philosophy | Chase losses | Ride winners |

## Betfair Exchange Notes

- For lay Contra D'Alembert, decrease liability after losing lays, increase after winning lays

## Related Plans

- [D'Alembert](./dalembert.md) — Standard (negative progression) version
- [Paroli](./paroli.md) — More aggressive positive progression (doubling)
- [Oscar's Grind](./oscars-grind.md) — Another conservative positive progression

---

## Sources

- **Plan mechanics:** Classic betting system (public domain)
- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
