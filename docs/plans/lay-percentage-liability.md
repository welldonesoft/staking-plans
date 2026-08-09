---
id: lay-percentage-liability
name: Lay % Liability
category: lay
type: proportional
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Lay Percentage Liability
  - Proportional Liability Lay
---

# Lay Percentage Liability

## Overview

Stake such that your **liability** (not your stake) equals a fixed percentage of your bankroll. This is the safer proportional approach for lay betting — your risk scales predictably regardless of odds.

## How It Works

$$Stake = \frac{Bankroll \times (percentage / 100)}{Odds - 1}$$

**Example:** £1,000 bankroll at 2% liability. At odds of 3.0: stake = £20/2 = £10, liability = £20. At odds of 10.0: stake = £20/9 = £2.22, liability = £20. In both cases, risk = 2% of bankroll.

## Formula

$$S = \frac{B \times p}{o - 1}$$

Where:
- $S$ = lay stake
- $B$ = current bankroll
- $p$ = liability percentage (as decimal, e.g., 0.02)
- $o$ = decimal lay odds

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `percentage` | number | 2 | Percentage of bankroll to risk as liability |

## Risk Assessment

- **Risk Level:** Medium (consistent % risk per bet)
- **Max Drawdown:** Similar to back % staking — controlled by the percentage
- **Recommended Bankroll:** 50× liability (50× 2% = 100% of bankroll, i.e., any bankroll works)
- **Ruin Risk:** Low — risk is always a fixed fraction

## When to Use

- **Recommended for most lay bettors** using proportional staking
- Your lay selections have widely varying odds
- You want bankroll protection with compounding growth

## When to Avoid

- Very short lay odds (near 1.01) — stake becomes very large for a tiny win
- You want consistent winnings rather than consistent risk

## Betfair Exchange Notes

- This is the lay equivalent of back percentage staking and is the most sensible default for proportional lay betting
- Winnings vary: lower odds = larger stake = larger win; higher odds = smaller stake = smaller win

## Related Plans

- [Lay Liability](./lay-liability.md) — Fixed liability (non-compounding)
- [Lay Percentage](./lay-percentage.md) — % of stake, not liability (riskier)
- [Percentage Staking](./percentage-staking.md) — Back betting equivalent

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
