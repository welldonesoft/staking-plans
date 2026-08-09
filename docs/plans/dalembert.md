---
id: dalembert
name: D'Alembert
category: back
type: negative-progression
risk: medium
betfair_compatible: true
aliases:
source: tsm
  - D'Alembert System
  - Pyramid System
---

# D'Alembert Staking Plan

## Overview

A moderate negative progression system: increase stake by 1 unit after a loss, decrease by 1 unit after a win. Much less aggressive than Martingale or Fibonacci. Based on the (mathematically false) "law of equilibrium" — the belief that wins and losses eventually balance out.

## How It Works

- Start with a base stake (e.g., 1 unit)
- **After a loss:** Increase next stake by 1 unit
- **After a win:** Decrease next stake by 1 unit (never below base stake)
- Theory: over time, wins and losses should roughly balance, and each win-lose pair produces +1 unit profit

## Formula

$$S_{i+1} = \begin{cases} S_i + 1 & \text{if bet } i \text{ lost} \\ \max(S_i - 1, 1) & \text{if bet } i \text{ won} \end{cases}$$

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_unit` | number | 1 | Starting and minimum stake |
| `increment` | number | 1 | Amount to increase/decrease (default 1 unit) |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Linear growth — 10 consecutive losses = 55 units lost (1+2+3+...+10)
- **Recommended Bankroll:** 100–200 units
- **Ruin Risk:** Medium — slower stake growth than Fibonacci, but still vulnerable to long losing streaks

## When to Use

- You want a progression system but find Martingale/Fibonacci too aggressive
- Your system has a roughly 50% strike rate
- You have a moderate bankroll

## When to Avoid

- Low strike-rate systems — even linear growth becomes unsustainable over many losses
- High-odds betting — wins are infrequent and the "1 unit per pair" profit logic breaks down
- You're uncomfortable with any form of loss-chasing

## Betfair Exchange Notes

- For lay betting, be cautious: increasing stake after a loss means increasing liability. At odds of 5.0, each additional unit of stake = 4 additional units of liability.
- Commission on wins reduces the net profit from win-lose pairs — the 1-unit-per-pair profit may become ~0.9 units after commission

## Comparison

| Plan | Stake After 5 Losses | Stake After 10 Losses | Recovery Style |
|------|----------------------|------------------------|----------------|
| D'Alembert | 6 units | 11 units | Linear |
| Fibonacci | 8 units | 89 units | Exponential-ish |
| Martingale | 32 units | 1,024 units | Doubling |

## Related Plans

- [Fibonacci](./fibonacci.md) — Faster negative progression
- [Labouchere](./labouchere.md) — More aggressive sequence-based plan
- [Contra D'Alembert](./parlay.md) — Reverse (increase after wins, decrease after losses)

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
