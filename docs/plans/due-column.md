---
id: due-column
name: Due Column Staking Plan
category: back
type: target-based
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - Due-Column System
  - Two-Column Plan
---

# Due Column Staking Plan

## Overview

A target-based plan using two columns: a **profit column** and a **loss column**. The stake is the sum of entries in both columns divided by odds−1. After a win, cross off entries from both columns. After a loss, add to the loss column. The goal is to clear both columns.

## How It Works

1. Set up a **profit column** with your desired profit target split into numbers (e.g., 10-10-10 = £30 target)
2. Set up an empty **loss column**
3. Stake = (sum of profit column + sum of loss column) / (odds − 1)
4. **Win:** Cross off the first entry from the profit column AND remove an equivalent amount from the loss column
5. **Loss:** Add the lost stake to the loss column
6. Target reached when the profit column is empty (loss column should also clear)

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `profit_targets` | number[] | [10,10,10] | Profit target broken into entries |
| `max_loss_entries` | number | — | Maximum entries in loss column before giving up |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Loss column can grow during losing streaks, inflating stakes
- **Recommended Bankroll:** 5× total profit target
- **Ruin Risk:** Medium

## When to Use

- You want a structured, two-column approach to profit targeting
- You prefer visual tracking of profit and loss separately

## When to Avoid

- Simple profit targets (use Retirement or 6 Point Divisor instead)
- Low strike rates (loss column grows quickly)

## Betfair Exchange Notes

- Works for both back and lay
- For lay, base columns on liability targets

## Related Plans

- [Labouchere](./labouchere.md) — Single-sequence approach (simpler)
- [Retirement](./retirement.md) — Divisor-based targeting (simpler)

---

## Sources

- **Plan mechanics:** Classic betting system (public domain)
- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
