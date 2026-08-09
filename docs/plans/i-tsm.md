---
id: i-tsm
name: i-TSM
category: back
type: custom
risk: variable
betfair_compatible: true
aliases:
source: tsm
  - Intelligent TSM
---

# i-TSM Staking Plan

## Overview

An intelligent, adaptive staking plan that adjusts stakes based on recent performance metrics. The "i" stands for intelligent — it dynamically modifies stake sizing based on strike rate, ROI, and other performance indicators.

## How It Works

1. Monitor recent betting performance (last N bets)
2. Calculate performance metrics (strike rate, ROI, profit/loss)
3. Adjust stake size based on metrics:
   - **Good performance:** Gradually increase stakes
   - **Poor performance:** Gradually decrease stakes
4. The adjustment is continuous and data-driven

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting/reference stake |
| `lookback` | number | 20 | Number of recent bets to analyze |
| `sensitivity` | number | 0.5 | How aggressively to adjust stakes |

## Risk Assessment

- **Risk Level:** Variable (depends on sensitivity and lookback)
- **Max Drawdown:** Self-correcting — reduces stakes during poor runs
- **Recommended Bankroll:** 50× base stake
- **Ruin Risk:** Low-medium — adaptive reduction provides protection

## When to Use

- You believe recent performance predicts near-future performance
- You want a plan that "learns" from results
- You're comfortable with data-driven approaches

## When to Avoid

- Your edge is consistent regardless of recent results (use fixed staking)
- You want simple, predictable stake sizes
- Short-term variance misleads the adaptive mechanism

## Betfair Exchange Notes

- The adaptive nature works well on exchange where you can adjust stakes fluidly
- Ensure lookback period is long enough to distinguish signal from noise

## Related Plans

- [Percentage Staking](./percentage-staking.md) — Responds to bankroll, not performance
- [Kelly Criterion](./kelly-criterion.md) — Responds to edge, not recent results

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
