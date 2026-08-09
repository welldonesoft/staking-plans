---
id: up-x-down-y
name: Up X Down Y
category: back
type: progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Up X / Down Y
  - Asymmetric Progression
---

# Up X Down Y Staking Plan

## Overview

An asymmetric progression plan where stakes increase by X units after a loss but decrease by Y units after a win — with X and Y independently configurable. Typically X > Y, making the plan a mild negative progression (faster up, slower down).

## How It Works

- **After a loss:** Increase stake by X units
- **After a win:** Decrease stake by Y units (never below base)
- Choose X and Y to control recovery speed vs risk

**Example (X=2, Y=1):** Start at 10. Lose → 12. Lose → 14. Win → 13. Win → 12. Lose → 14...

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting and minimum stake |
| `X` | number | 2 | Units to increase after a loss |
| `Y` | number | 1 | Units to decrease after a win |

## Risk Assessment

- **Risk Level:** Medium (X > Y), Low (X = Y), Low (Y > X — positive progression)
- **Max Drawdown:** Linear growth at rate X per loss
- **Recommended Bankroll:** 100+ units
- **Ruin Risk:** Medium if X > Y

## When to Use

- You want fine-grained control over progression speed
- You prefer moderate negative progression (X slightly larger than Y)
- Or you want positive progression (Y > X)

## When to Avoid

- Large X values — linear growth becomes aggressive over many losses
- You want simple, fixed rules

## Betfair Exchange Notes

- For lay betting, apply X and Y to liability, not stake (safer)
- See [Lay % Up Down](./lay-percentage-up-down.md) for the lay variant

## Related Plans

- [D'Alembert](./dalembert.md) — Special case where X = Y = 1
- [Lay % Up Down](./lay-percentage-up-down.md) — Lay variant

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
