---
id: oscars-grind
name: Oscar's Grind
category: back
type: positive-progression
risk: low
betfair_compatible: true
aliases:
source: tsm
  - Oscar's System
  - The Grind
---

# Oscar's Grind

## Overview

A slow, grinding positive progression: increase your stake by 1 unit after a win — but ONLY if the resulting bet wouldn't produce more than 1 unit of profit for the entire sequence. The goal is to "grind out" exactly 1 unit of profit per cycle. One of the most conservative progression systems ever devised.

## How It Works

1. Start at 1 unit. The goal is to end the sequence +1 unit.
2. **Win:** If the next bet (at current stake + 1) would produce a sequence profit of ≤ 1 unit, increase stake by 1. Otherwise, keep stake the same (or reduce to exactly target +1 unit profit).
3. **Loss:** Keep stake the same.
4. When the sequence reaches +1 unit profit, reset to 1 unit and start a new cycle.

**Example (1 unit base, even-money bets):**
- Bet 1: 1 unit, Lose (−1). Sequence: −1
- Bet 2: 1 unit, Lose (−1). Sequence: −2
- Bet 3: 1 unit, Win (+1). Sequence: −1 (stake stays at 1 because 2 would overshoot +1)
- Bet 4: 1 unit, Win (+1). Sequence: 0
- Bet 5: 1 unit, Win (+1). Sequence: +1 → Reset. Cycle complete.

## Key Rule

The golden rule: **never bet more than needed to achieve exactly +1 unit profit for the sequence.** If you're at −3 and bet 1 unit, a win at evens brings you to −2 — still not +1, so the stake could increase to 2 for the next bet (2 × evens = +2 profit, −3 + 2 = −1, still below +1).

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `unit` | number | 1 | Base unit size |
| `target_profit` | number | 1 | Profit target per cycle (typically 1 unit) |

## Risk Assessment

- **Risk Level:** Low
- **Max Drawdown:** Very slow stake growth — stakes only increase after wins, and only when it won't overshoot the 1-unit target
- **Recommended Bankroll:** 50+ units
- **Ruin Risk:** Very low — one of the safest progression systems

## When to Use

- You have extreme patience (cycles can be very long)
- Capital preservation is paramount
- You enjoy the intellectual elegance of "never bet more than you need"

## When to Avoid

- You want fast results (the "grind" is real — cycles with many losses can take dozens of bets)
- Low odds selections (harder to reach +1 with small wins)
- You find the calculation tedious

## Betfair Exchange Notes

- The +1 target should account for commission: effective target ≈ 1 / (1 − commission)
- Works for both back and lay

## Related Plans

- [Paroli](./paroli.md) — Aggressive positive progression (opposite philosophy)
- [D'Alembert](./dalembert.md) — Moderate negative progression
- [Whitaker](./whitaker.md) — Another conservative, slow-growth plan

---

## Sources

- **Plan mechanics:** Classic casino/betting system (public domain)
- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
