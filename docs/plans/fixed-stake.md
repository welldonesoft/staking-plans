---
id: fixed-stake
name: Fixed Stake
category: back
type: flat
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Fixed Return
  - Target Profit Staking
---

# Fixed Stake (Target Profit)

## Overview

Stake whatever amount is needed to achieve a fixed profit target, given the odds. Unlike level stakes (fixed outlay), this adjusts the stake based on odds so that every winning bet returns the same profit.

## How It Works

$$Stake = \frac{Target\ Profit}{Odds - 1}$$

**Example:** Target profit = £10. At odds of 2.0, stake = £10 / 1 = £10. At odds of 5.0, stake = £10 / 4 = £2.50. Both winning bets return £10 profit.

## Formula

$$S = \frac{T}{o - 1}$$

Where:
- $S$ = stake
- $T$ = target profit
- $o$ = decimal odds

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target_profit` | number | 10 | Desired profit per winning bet |

## Risk Assessment

- **Risk Level:** Low (profit-side), Variable (stake-side)
- **Max Drawdown:** Stake × losing streak length — higher at short odds
- **Recommended Bankroll:** 50× target profit (covers high-stake short-odds bets)
- **Ruin Risk:** Low with sensible targets

## When to Use

- You want consistent profit per winner regardless of odds
- Your selections vary widely in odds but have similar confidence
- Simpler than Kelly for odds-based stake adjustment

## When to Avoid

- Very short odds (near 1.01) — stake becomes extreme
- Very long odds — stake becomes tiny, almost pointless
- You don't care about consistent profit amounts

## Betfair Exchange Notes

- Adjust target profit downward by commission rate: effective target = target × (1 − commission)
- For lay betting, the equivalent is **Fixed Liability** (risk the same liability regardless of odds) — see [Lay Liability](./lay-liability.md)

## Related Plans

- [Level Stakes](./level-stakes.md) — Fixed outlay, variable profit
- [Lay Liability](./lay-liability.md) — Lay equivalent (fixed risk per bet)

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
