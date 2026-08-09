---
id: divide-by-n-recovery
name: Divide-by-N Recovery
category: lay
type: recovery
risk: high
betfair_compatible: true
aliases:
  - Split Recovery
  - Win-N-in-a-Row Recovery
source: community
---

# Divide-by-N Recovery

## Overview

A two-phase recovery plan: after accumulating losses, divide the total loss by N and then aim to win N consecutive bets at that calculated stake. If you lose during the N-win streak, recalculate and restart. Clever, but demands discipline and a reasonable strike rate.

## How It Works

**Phase 1 — Initial bet:** Bet at base stake. If it loses, attempt one recovery bet to recoup. If that also loses:

**Phase 2 — Divide-and-conquer:**
1. Calculate total loss from the failed recovery sequence
2. Divide total loss by N (e.g., 4)
3. The result is your new stake
4. Place this stake on the next N bets — you need to win ALL N in a row
5. **If you win N in a row:** Total loss is recovered → return to Phase 1
6. **If you lose during the N-win streak:** Recalculate total loss (including the new losses), divide by N again, restart the N-win attempt

**Example (N=4, £10 base):**
- Bet 1: £10 lay. Lose (−£30). Bet 2: Recovery stake. Lose (−£60 more). Total = −£90.
- Divide £90 by 4 = £22.50. Need 4 consecutive winning lays at £22.50 each.
- Win, Win, Lose on 3rd. New total loss = £90 + £22.50 (loss on 3rd) = £112.50.
- Divide £112.50 by 4 = £28.13. Need 4 consecutive wins at £28.13.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting stake |
| `N` | number | 4 | Divisor and consecutive wins needed |
| `max_stake` | number | — | Optional absolute stake cap |
| `max_cycles` | number | — | Maximum divide-and-conquer attempts before giving up |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Can escalate if N is small (larger stake per bet) or if losing streaks persist during N-win attempts
- **Recommended Bankroll:** 50× (expected max total loss / N)
- **Ruin Risk:** High — the "N consecutive wins" requirement is steep

## ⚠️ Critical Warning

Winning N consecutive bets is **geometrically harder** than winning any single bet. At a 70% strike rate, the probability of 4 consecutive wins is 0.7⁴ = 24%. At 50%, it's just 6.25%. This plan can enter very long recovery cycles.

## When to Use

- Very high strike rate (>75%)
- You have a large bankroll and steel nerves
- You're willing to set a hard max_cycles and accept the loss if exceeded

## When to Avoid

- Strike rate below 65% (N=4) — you'll rarely complete a streak
- Small bankrolls
- You can't tolerate long losing/recovery sequences

## Betfair Exchange Notes

- Originally proposed for lay betting on greyhounds
- For lay, the stake is the lay stake; liability = stake × (odds−1)
- Consider using liability-based calculations instead of stake-based

## Related Plans

- [Recovery](./recovery.md) — Single-bet recovery (no divide-and-conquer)
- [Stop at a Winner](./stop-at-a-winner.md) — Reset on any winner (only needs 1 win)
- [Diluted Loss Recovery](./diluted-loss-recovery.md) — Spread loss across many bets (opposite philosophy)

---

## Sources

- **Plan source:** [WellDone Community Forum — "Greyhound trigger"](https://community.welldonesoft.com/index.php?topic=15908.0) — user-contributed concept by Dace
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
