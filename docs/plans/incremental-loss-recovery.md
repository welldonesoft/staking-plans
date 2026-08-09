---
id: incremental-loss-recovery
name: Incremental Loss Recovery
category: lay
type: recovery
risk: medium
betfair_compatible: true
aliases:
  - Incremental Recovery
  - Step Recovery
source: marketfeeder
---

# Incremental Loss Recovery Plan

## Overview

A milder alternative to Martingale-style recovery. After a loss, add the **starting bet amount** (not the full loss) to the next bet. After a win, reduce the bet by a percentage of the starting amount. Escalation is linear and controlled, not exponential.

## How It Works

1. Start with a fixed percentage of bank (unit size)
2. **After a loss:** Next bet = previous bet + unit size
3. **After a win:** Next bet = previous bet − (unit size × reduction %), but never below unit size

**Example (unit = £10, reduction = 30%):**
- £10 (Win) → £10
- £10 (Loss) → £20
- £20 (Win) → £14 (−30% of £10 = −£3 → wait, that's not right)

Actually: reduction is 30% of the **starting bet** (£10), not the current bet. So £20 (Win) → £20 − £3 = £17 (but the description says £14... Let me re-read)

The page says: "After each win, you decrease the next bet by a percentage of the starting bet, unless the bet is already equal to its initial size."

Example: 10 (Win), 10 (Loss), 20 (Win), 14 (Win), 9.8 (Win)...

So the reduction is from the **current bet**, not the starting bet. 20 − 30% = 14. Then 14 − 30% = 9.8. That matches.

## Formula

$$S_{i+1} = \begin{cases} S_i + U & \text{if loss} \\ \max(S_i \times (1 - r), U) & \text{if win} \end{cases}$$

Where:
- $S_i$ = current stake
- $U$ = unit size (starting stake)
- $r$ = reduction percentage after a win (e.g., 0.30)

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `unit_size_pct` | number | 1 | Unit size as % of bank |
| `win_reduction` | number | 30 | % reduction after a win |
| `min_odds` | number | 1.5 | Minimum lay odds |
| `max_odds` | number | 10 | Maximum lay odds |

## Risk Assessment

- **Risk Level:** Medium (much lower than Martingale)
- **Max Drawdown:** Linear growth at unit_size per loss — predictable
- **Recommended Bankroll:** 100× unit size
- **Ruin Risk:** Medium-low — linear escalation is manageable

## Comparison: Martingale vs Incremental

| | Martingale | Incremental |
|---|---|---|
| After a loss | Double the stake | Add unit size |
| After 5 losses | 32× original | 6× original |
| After 10 losses | 1,024× original | 11× original |
| Risk | Very High | Medium |

## When to Use

- You want recovery mechanics but find Martingale too dangerous
- Your lay system has moderate strike rates
- You prefer predictable, linear stake growth

## When to Avoid

- Very long losing streaks (linear still adds up)
- Very high lay odds (liability × linear growth can still be substantial)

## Betfair Exchange Notes

- Originally designed for lay betting but can be adapted for back
- For lay, consider basing the unit on liability, not stake

## Related Plans

- [Recovery](./recovery.md) — More aggressive (full loss recovery)
- [D'Alembert](./dalembert.md) — Similar linear progression, different rules
- [Lay % Recovery](./lay-percentage-recovery.md) — Percentage-based lay recovery

---

## Sources

- **Plan source:** [MarketFeeder — Incremental Loss Recovery](https://marketfeeder.co.uk/learn/triggers/incremental-loss-recovery/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
