---
id: lay-percentage
name: Lay Percentage Staking
category: lay
type: proportional
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Lay % Staking
  - Proportional Lay
---

# Lay Percentage Staking

## Overview

Stake a fixed percentage of your current bankroll on each lay bet. This means your **stake** (the backer's amount) scales with bankroll, but your **liability** also scales with odds — making it riskier than percentage staking for back bets.

## How It Works

$$Stake = Bankroll \times \frac{percentage}{100}$$

$$Liability = Stake \times (Odds - 1)$$

**Example:** £1,000 bankroll at 2%. At odds of 3.0: stake = £20, liability = £40. At odds of 10.0: stake = £20, liability = £180 (18% of bankroll!).

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `percentage` | number | 1 | Percentage of bankroll to stake (use lower than back % staking) |

## Risk Assessment

- **Risk Level:** Medium (higher than back % staking due to liability multiplier)
- **Max Drawdown:** Accelerated at high odds
- **Recommended Bankroll:** Large — liability can spike at high odds
- **Ruin Risk:** Medium — high-odds losses can take large chunks of bankroll

## ⚠️ Critical Warning

2% of bankroll as a lay stake at odds of 10.0 risks 18% of bankroll. Use a **much lower** percentage for lay betting than you would for back betting. Consider 0.5–1% maximum.

## Betfair Exchange Notes

- For most lay bettors, [Lay % Liability](./lay-percentage-liability.md) is safer — it ties the percentage to liability, not stake
- Always check the liability before confirming a lay bet

## Related Plans

- [Lay % Liability](./lay-percentage-liability.md) — Safer: % of bankroll as liability, not stake
- [Percentage Staking](./percentage-staking.md) — Back betting equivalent
- [Lay Level](./lay-level.md) — Simpler flat alternative

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
