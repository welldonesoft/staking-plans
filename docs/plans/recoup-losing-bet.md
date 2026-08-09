---
id: recoup-losing-bet
name: Loss Recoupment (Single Bet)
category: lay
type: recovery
risk: medium
betfair_compatible: true
aliases:
  - Single Bet Recovery
  - Individual Bet Recoupment
source: marketfeeder
---

# Loss Recoupment for a Losing Bet Only

## Overview

A unique recovery approach: unlike most recovery plans that recoup **cumulative** losses, this plan only recoups the loss from a **single losing bet**. If you lay multiple selections in one market and one loses, only that specific loss is carried forward — other winning bets in the same market are not affected.

## How It Works

1. Lay on multiple selections per market (e.g., 3 selections)
2. Each selection has its own fixed stake
3. **If a specific selection loses (wins the race):** Add that single loss to the recovery pool
4. **If a selection wins (loses the race):** No change — that profit is kept
5. The recovery pool is divided across the next market's bets

**Example:** Lay 3 selections at £10 each. Two win (you profit), one loses (you pay out £30). Only the £30 loss is carried forward and split across the next 3 bets (+£10 each).

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `num_selections` | number | 3 | Number of selections to lay per market |
| `base_stake` | number | 10 | Fixed stake per selection |
| `max_stake` | number | 50 | Maximum stake cap per selection |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Controlled — only single-bet losses accumulate, not cumulative
- **Recommended Bankroll:** 30× (num_selections × base_stake)
- **Ruin Risk:** Medium-low — max_stake cap provides protection

## When to Use

- Multi-selection lay strategies (dutching-style laying)
- You want recovery that doesn't snowball from cumulative losses
- You have a mix of winning and losing selections per market

## When to Avoid

- Single-selection strategies (standard recovery works fine)
- Very high lay odds on individual selections (single loss can be large)

## Betfair Exchange Notes

- Particularly suited to exchange lay dutching — lay multiple horses in a race
- The isolation of losses per selection prevents one bad pick from ruining the whole strategy
- Commission on winning lays is kept, not absorbed into recovery

## Related Plans

- [Recovery](./recovery.md) — Cumulative loss recovery (more aggressive)
- [Lay Dutching with loss recovery](./lay-dutching-recovery.md) — Dutching-specific recovery

---

## Sources

- **Plan source:** [MarketFeeder — Loss Recoupment for a Losing Bet](https://marketfeeder.co.uk/learn/triggers/recoup-losing-bet/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
