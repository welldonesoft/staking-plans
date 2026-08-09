---
id: martingale
name: Martingale
category: back
type: negative-progression
risk: very-high
betfair_compatible: true
aliases:
source: tsm
  - Classic Martingale
  - Double After Loss
---

# Martingale Staking Plan

## Overview

The most infamous negative progression system: double your stake after every loss. The theory: when you eventually win, you recover all previous losses plus one unit of profit. In practice, it's extremely dangerous — losing streaks cause exponential stake growth and will exhaust any finite bankroll.

## How It Works

1. Start with 1 unit
2. **Loss:** Double the stake for the next bet
3. **Win:** Reset to 1 unit
4. After any win, you are exactly +1 unit for that cycle

**Example:** £10 → lose → £20 → lose → £40 → lose → £80 → win (+£80). Net: −£10 −£20 −£40 +£80 = +£10 (1 unit profit).

## Formula

$$S_{i+1} = \begin{cases} 2 \times S_i & \text{if loss} \\ S_0 & \text{if win} \end{cases}$$

After $n$ consecutive losses, stake = $S_0 \times 2^n$

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_unit` | number | 1 | Starting stake |
| `max_steps` | number | — | Optional cap on doublings (recommended) |

## Risk Assessment

- **Risk Level:** Very High
- **Max Drawdown:** Exponential — 10 consecutive losses requires 1,024× base unit
- **Recommended Bankroll:** 1,000+ units (to survive 9 consecutive losses)
- **Ruin Risk:** Very high — finite bankroll + infinite doubling = eventual ruin

## The Mathematics of Ruin

| Consecutive Losses | Stake (units) | Cumulative Loss |
|-------------------|---------------|-----------------|
| 1 | 2 | 1 |
| 2 | 4 | 3 |
| 3 | 8 | 7 |
| 4 | 16 | 15 |
| 5 | 32 | 31 |
| 6 | 64 | 63 |
| 7 | 128 | 127 |
| 8 | 256 | 255 |
| 9 | 512 | 511 |
| 10 | 1,024 | 1,023 |

At 10 consecutive losses (not rare in betting), you need over 1,000× your base unit just to place the next bet.

## ⚠️ Critical Warning

**Martingale is mathematically guaranteed to fail** given:
1. A finite bankroll
2. A maximum bet limit (Betfair has one)
3. An unbounded number of bets

The only way Martingale "works" is with infinite wealth and no bet limits — neither exists. Every professional betting resource advises against it.

## When to Use

- Almost never. The one legitimate context: very short-term, tightly stop-lossed sequences where you fully understand and accept the risk.

## When to Avoid

- Always, unless you have a specific, bounded strategy and enormous bankroll relative to base unit
- Lay betting (liability compounds even faster)
- Any serious long-term betting

## Betfair Exchange Notes

- Betfair has maximum liability limits — you will hit them during a Martingale sequence
- For lay Martingale, doubling liability is even more dangerous than doubling stake
- Commission means the "1 unit profit" per cycle is actually less than 1 unit

## Related Plans

- [Fibonacci](./fibonacci.md) — Slower negative progression (Fibonacci sequence)
- [D'Alembert](./dalembert.md) — Linear progression (much safer)
- [Incremental Loss Recovery](./incremental-loss-recovery.md) — Controlled linear recovery
- [Recovery](./recovery.md) — Targets specific loss recovery rather than arbitrary doubling

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
