---
id: lay-accumulator
name: Lay Accumulator Staking Plan
category: lay
type: positive-progression
risk: medium
betfair_compatible: true
aliases:
  - Accumulator Staking (Lay)
  - Lay Profit Accumulator
source: marketfeeder
---

# Lay Accumulator Staking Plan

## Overview

The lay betting version of the Accumulator Staking Plan. After each winning lay, accumulate the **liability** by adding the base liability plus a percentage of the profit. Reset after a loss or after completing the cycle. Compounds winnings, never chases losses.

## How It Works

1. Start with a base liability (e.g., £5)
2. **Win lay (selection loses):** Next liability = base liability × step number + % of previous profit
3. **Lose lay (selection wins):** Reset to base liability
4. After N steps, reset regardless

**Example (5-step cycle, £5 base liability, 50% accumulation):**
- Step 1: £5 liability. Win £5. → Step 2: £10 + 50% of £5 = £12.50 liability
- Step 2: £12.50 liability. Win £12.50. → Step 3: £15 + 50% of £12.50 = £21.25 liability
- Step 3: £21.25 liability. Lose (pay out). → Reset to £5

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_liability` | number | 5 | Starting liability |
| `cycle_length` | number | 5 | Steps before forced reset |
| `profit_pct` | number | 50 | % of profit to accumulate |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Base liability per losing lay (controlled)
- **Recommended Bankroll:** 30× maximum cycle liability
- **Ruin Risk:** Low — never chases losses

## When to Use

- Your lay selections cluster in winning streaks
- You want positive progression for lay betting
- Conservative approach (loss = reset, not escalate)

## When to Avoid

- Low lay strike rates
- Isolated winning lays (rarely compound)

## Betfair Exchange Notes

- Uses **liability** as the base, not stake — safer and more predictable
- Profit is stake won (minus commission), not liability
- The lay stake is derived: Stake = Liability / (Odds − 1)

## Related Plans

- [Back Accumulator](./back-accumulator.md) — Back equivalent (stake-based)
- [Ratchet Lay](./ratchet-lay.md) — Similar philosophy, different mechanics
- [Lay % Liability](./lay-percentage-liability.md) — Proportional alternative

---

## Sources

- **Plan source:** [MarketFeeder — Lay Accumulator Staking](https://marketfeeder.co.uk/learn/triggers/lay-accumulator-staking-plan/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
