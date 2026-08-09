---
id: fibonacci
name: Fibonacci
category: back
type: negative-progression
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Fibonacci Sequence
  - Fibonacci Staking
---

# Fibonacci Staking Plan

## Overview

A negative progression system using the Fibonacci sequence (1, 1, 2, 3, 5, 8, 13, 21...). After a loss, move one step forward in the sequence. After a win, move two steps back. The goal is to recover losses through progressively larger stakes.

## How It Works

- Start at the first number in the sequence (1 unit)
- **After a loss:** Move forward one step in the sequence
- **After a win:** Move back two steps
- When you return to the start (or before), any winning sequence should produce a net profit

## Formula

The Fibonacci sequence:

$$F_0 = 1, \quad F_1 = 1, \quad F_n = F_{n-1} + F_{n-2}$$

Sequence: 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144...

**Stake:** $S = F_n \times \text{unit}$, where $n$ is your current position in the sequence.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `unit` | number | 1 | Base unit size for the sequence |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Potentially very large — 10 consecutive losses requires 89 units (sum of stakes = 231 units lost)
- **Recommended Bankroll:** 500+ units
- **Ruin Risk:** High — long losing streaks cause exponential stake growth (though slower than Martingale)

## When to Use

- You accept the risk of progressive staking
- You have a very large bankroll relative to unit size
- Your selections have a reasonable strike rate (avoid with very low win rates)

## When to Avoid

- Limited bankroll — long losing streaks will exhaust it
- Low strike-rate systems — losses compound dangerously
- You're uncomfortable with escalating stakes after losses
- Exchange betting with high-odds selections (lay liability can become extreme)

## Betfair Exchange Notes

- For **lay betting** with Fibonacci, consider liability rather than stake — escalating lay stakes at high odds means exponentially growing liability
- Commission on wins slightly reduces the recovery effect (you need slightly more than 2 steps back)

## Comparison with Martingale

| | Fibonacci | Martingale |
|---|---|---|
| Growth rate | Moderate | Exponential |
| Recovery steps | 2 steps back per win | Reset to start per win |
| 10-loss sequence stake | 89 units | 1,024 units |
| Risk | High | Very High |

## Related Plans

- [D'Alembert](./dalembert.md) — Slower negative progression
- [Labouchere](./labouchere.md) — Sequence-based but user-defined
- [Recovery](./recovery.md) — More aggressive recovery approach

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
