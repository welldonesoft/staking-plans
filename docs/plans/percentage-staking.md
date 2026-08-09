---
id: percentage-staking
name: Percentage Staking
category: back
type: proportional
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Proportional Staking
  - % of Bankroll
---

# Percentage Staking

## Overview

Stake a fixed percentage of your current bankroll on each bet. Stakes grow as you win and shrink as you lose — providing natural bankroll protection since you can never bet 100% of what remains.

## How It Works

Before each bet, calculate `percentage%` of your current bankroll.

```
Stake = Bankroll × (percentage / 100)
```

**Example:** £1,000 bankroll at 2% = £20 stake. After a win at 2.0 odds, bankroll = £1,020. Next stake = £20.40.

## Formula

$$S_i = B_i \times \frac{p}{100}$$

Where:
- $S_i$ = stake for bet $i$
- $B_i$ = current bankroll before bet $i$
- $p$ = percentage to stake (typically 1–5%)

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `percentage` | number | 2 | Percentage of bankroll to stake (1–5 recommended) |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** Theoretical maximum is 100% but approached asymptotically (never reaches zero)
- **Recommended Bankroll:** Any — plan scales automatically
- **Ruin Risk:** Mathematically impossible to go broke (you only ever bet a fraction of remainder)

## When to Use

- You want automatic compounding of profits
- You want automatic stake reduction during losing runs
- Long-term growth with bankroll protection
- You prefer a "set and forget" percentage

## When to Avoid

- Very small bankrolls (tiny absolute stakes may not meet minimum bet requirements)
- You need quick recovery from drawdowns (slow and steady)

## Betfair Exchange Notes

- For lay betting, consider whether the percentage should apply to stake or liability (see [Lay % Liability](./lay-percentage-liability.md))
- Commission reduces effective growth rate — a 2% net stake may effectively be ~1.9% after commission

## Related Plans

- [Level Stakes](./level-stakes.md) — Simpler flat alternative
- [Kelly Criterion](./kelly-criterion.md) — Edge-based proportional staking
- [Square Root](./square-root.md) — Slower-scaling proportional variant
- [Lay Percentage](./lay-percentage.md) — Lay-specific variant

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
