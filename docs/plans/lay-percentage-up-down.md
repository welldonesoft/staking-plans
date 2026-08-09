---
id: lay-percentage-up-down
name: Lay % Up Down
category: lay
type: progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Lay Percentage Up/Down
---

# Lay % Up Down Staking Plan

## Overview

The lay betting adaptation of the Up X Down Y plan — but operating on percentages rather than absolute amounts. After a losing lay, increase the percentage; after a winning lay, decrease it.

## How It Works

- Stake = Bankroll × current percentage
- **Lose lay (selection wins):** Increase percentage by X%
- **Win lay (selection loses):** Decrease percentage by Y%
- Typically X > Y (faster up, slower down) for mild negative progression

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_pct` | number | 1 | Starting percentage of bankroll |
| `X` | number | 0.5 | Percentage points to increase after a loss |
| `Y` | number | 0.25 | Percentage points to decrease after a win |
| `max_pct` | number | 5 | Maximum percentage cap |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Controlled by max_pct cap
- **Recommended Bankroll:** 100× initial stake

## When to Use

- You want progressive lay staking with percentage-based control
- You prefer caps on escalation

## When to Avoid

- You want flat or fixed staking

## Betfair Exchange Notes

- Base the percentage on **liability** rather than stake for safer sizing
- max_pct is critical — without it, percentage can drift dangerously high

## Related Plans

- [Up X Down Y](./up-x-down-y.md) — Absolute-unit back equivalent
- [Lay % Liability](./lay-percentage-liability.md) — Non-progressive alternative

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
