---
id: diluted-loss-recovery
name: Diluted Loss Recovery
category: lay
type: recovery
risk: medium
betfair_compatible: true
aliases:
  - Spread Loss Recovery
  - Diluted Red Recovery
source: community
---

# Diluted Loss Recovery

## Overview

A unique recovery approach: instead of chasing a loss in the very next bet (or next few bets), spread the loss evenly across **all remaining entries** in your betting list. Each remaining bet gets a small additional amount added to its stake, diluting the impact of any single loss across the entire session.

## How It Works

1. You have a list of selections to bet on (e.g., 30 greyhound races)
2. Each selection starts with a base stake
3. **When a loss occurs:** The lost amount is divided by the number of remaining entries
4. Each remaining bet gets: base stake + (cumulative diluted loss / entries remaining)
5. **When a win occurs:** The profit reduces the diluted loss pool
6. Continue until the list is complete

**Example:** Start with £10 base stake, 30 races in the list.
- Race 3: Lose £30. 27 races remain. Add £30/27 = £1.11 to each remaining bet.
- Race 10: Lose £40. 20 races remain. Total undiluted loss: ~£70. Add £70/20 = £3.50 each.
- Race 15: Win £25. Undiluted loss drops to ~£45. 15 remain. Add £45/15 = £3.00 each.

## Key Insight

Unlike standard recovery where one loss can cascade into escalating stakes over the next few bets, **diluted recovery spreads the pain thinly**. A £100 loss over 50 remaining bets adds just £2 each — barely noticeable. This makes it far more psychologically manageable and bankroll-friendly than traditional recovery.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Base stake per selection |
| `list_size` | number | 30 | Total entries in the list |
| `max_dilution` | number | — | Optional cap on per-bet dilution amount |

## Risk Assessment

- **Risk Level:** Medium (much lower than standard recovery)
- **Max Drawdown:** Spread across many bets — individual bet stakes grow slowly
- **Recommended Bankroll:** 30× (base_stake + expected max dilution)
- **Ruin Risk:** Low-medium — dilution prevents any single bet from ballooning

## When to Use

- You bet from a fixed list/roster of selections daily
- You want loss recovery without the danger of escalating stakes
- You prefer "slow and steady" recovery over aggressive loss-chasing

## When to Avoid

- Short lists (few entries = dilution is less effective — loss is spread over too few bets)
- You don't use a predefined list of selections
- Very low strike rates (losses accumulate faster than they can be diluted)

## Betfair Exchange Notes

- Originally proposed for lay betting with fixed liability
- Works equally well for back betting
- The concept of spreading liability across remaining entries is particularly valuable for lay betting where individual losses can be large

## Related Plans

- [Recovery](./recovery.md) — Traditional aggressive recovery (next bet recovers all)
- [Incremental Loss Recovery](./incremental-loss-recovery.md) — Linear-add recovery (different philosophy)
- [Stop at a Winner](./stop-at-a-winner.md) — Reset on any winner

---

## Sources

- **Plan source:** [WellDone Community Forum — "new trigger"](https://community.welldonesoft.com/index.php?topic=17720.0) — user-contributed concept
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
