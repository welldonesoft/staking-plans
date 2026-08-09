---
id: lay-liability
name: Lay Fixed Liability
category: lay
type: flat
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Lay Liability Staking
  - Fixed Risk Lay
---

# Lay Fixed Liability

## Overview

Instead of fixing the lay stake, fix your **liability** (the amount you risk losing). Your stake adjusts based on odds so that every losing lay bet costs you the same amount. This is the safer, recommended approach for lay betting at varied odds.

## How It Works

$$Stake = \frac{Fixed\ Liability}{Odds - 1}$$

**Example:** Fixed liability = £100. At odds of 3.0: stake = £100/2 = £50. At odds of 10.0: stake = £100/9 = £11.11. In both cases, a loss costs exactly £100.

## Formula

$$S = \frac{L}{o - 1}$$

Where:
- $S$ = lay stake (backer's amount)
- $L$ = fixed liability (your maximum loss)
- $o$ = decimal lay odds

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `liability` | number | 100 | Fixed amount at risk per losing lay bet |

## Risk Assessment

- **Risk Level:** Low (controlled, predictable risk)
- **Max Drawdown:** Liability × consecutive losses (very predictable)
- **Recommended Bankroll:** 20–50× liability
- **Ruin Risk:** Low — risk is fixed per bet

## When to Use

- Your lay selections have widely varying odds
- You want predictable, consistent risk per bet
- Bankroll management is a priority
- **Recommended for most lay bettors**

## When to Avoid

- Very short lay odds (near 1.01) — stake becomes enormous relative to winnings
- You prefer consistent winnings rather than consistent losses

## Comparison: Fixed Stake vs Fixed Liability

| Scenario | Fixed Stake (£10) | Fixed Liability (£100) |
|----------|-------------------|------------------------|
| Lay at 2.0, lose | Lose £10 | Lose £100 |
| Lay at 10.0, lose | Lose £90 | Lose £100 |
| Lay at 2.0, win | Win £10 | Win £100 |
| Lay at 10.0, win | Win £10 | Win £11.11 |

## Betfair Exchange Notes

- This is the **recommended default** for exchange lay betting
- Winnings vary with odds (higher odds = smaller stake = smaller win), but risk is constant
- Commission on winnings: profit = stake × (1 − commission)

## Related Plans

- [Lay Level](./lay-level.md) — Fixed stake (variable risk)
- [Lay % Liability](./lay-percentage-liability.md) — Liability as % of bankroll
- [Fixed Stake](./fixed-stake.md) — Back betting equivalent (fixed profit target)

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
