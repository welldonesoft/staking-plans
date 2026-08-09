---
id: lay-level
name: Lay Level Stakes
category: lay
type: flat
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Lay Flat Staking
  - Lay Fixed Stake
---

# Lay Level Stakes

## Overview

The simplest lay staking plan: stake the same fixed amount on every lay bet. Your **liability** varies with odds, but your **stake** (the backer's amount you stand to win) is constant.

## How It Works

Bet the same amount on every lay selection. If the selection loses (you win), you gain the stake minus commission. If the selection wins (you lose), you pay out stake × (odds − 1).

```
Stake = Fixed Amount
Liability = Stake × (Odds − 1)
```

**Example:** £10 lay stake. At odds of 3.0: win £10 (less commission) or lose £20. At odds of 10.0: win £10 or lose £90.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `stake` | number | 10 | Fixed lay stake (backer's amount) |

## Risk Assessment

- **Risk Level:** Low (stake-side), Variable (liability-side)
- **Max Drawdown:** Depends on odds — high odds = large liability per loss
- **Recommended Bankroll:** Must cover worst-case liability × consecutive losses
- **Ruin Risk:** Low if stakes are sized for worst-case odds

## When to Use

- Beginners learning lay betting
- Your lay selections have consistently low odds (< 5.0)
- You want predictable winnings per successful lay

## ⚠️ Critical Warning

Unlike back betting where your stake IS your liability, lay betting decouples them. A £10 lay stake at odds of 10.0 risks £90. **Always calculate liability, not stake, when sizing for bankroll.**

## Betfair Exchange Notes

- Commission (default 5%) deducted from winnings: profit = stake × (1 − commission)
- Ensure sufficient balance to cover liability before placing lay bets

## Related Plans

- [Lay Liability](./lay-liability.md) — Fixed liability instead of fixed stake (safer at high odds)
- [Lay Percentage](./lay-percentage.md) — Stake a % of bankroll
- [Level Stakes](./level-stakes.md) — Back betting equivalent

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
