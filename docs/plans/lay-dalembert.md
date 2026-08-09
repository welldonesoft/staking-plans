---
id: lay-dalembert
name: Lay D'Alembert
category: lay
type: negative-progression
risk: medium
betfair_compatible: true
aliases:
  - Lay D'Alembert System
source: marketfeeder
---

# Lay D'Alembert Staking Plan

## Overview

The D'Alembert system adapted for lay betting. Increase liability by 1 unit after a losing lay, decrease by 1 unit after a winning lay. The moderate linear progression makes it one of the safer negative progression options for lay betting.

## How It Works

1. Start with a base liability unit
2. **Lose lay (selection wins):** Increase liability by 1 unit
3. **Win lay (selection loses):** Decrease liability by 1 unit (never below base)
4. Theory: over time, wins and losses balance, each pair producing +1 unit profit

## Formula

$$L_{i+1} = \begin{cases} L_i + 1 & \text{if lay lost (selection won)} \\ \max(L_i - 1, L_0) & \text{if lay won (selection lost)} \end{cases}$$

Where $L_i$ is the liability for bet $i$, measured in units.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_liability` | number | 1 | Starting liability (units) |
| `increment` | number | 1 | Units to increase/decrease |

## Risk Assessment

- **Risk Level:** Medium
- **Max Drawdown:** Linear — 10 consecutive losing lays = 55 units lost
- **Recommended Bankroll:** 100–200 units

## ⚠️ Lay-Specific Warning

D'Alembert for lay betting escalates **liability**, not stake. Each additional unit of liability at odds of 5.0 means the stake only increases by 0.25 units — but the financial risk is explicit and controlled. This makes lay D'Alembert **safer** than back D'Alembert at equivalent unit sizing, because you control the liability directly.

## Betfair Exchange Notes

- **Use liability-based D'Alembert** (not stake-based) for predictable risk
- At short lay odds, liability and stake are similar; at long odds, stake is much smaller than liability

## Related Plans

- [D'Alembert](./dalembert.md) — Back betting original
- [Lay Ladder](./lay-ladder.md) — Structured lay progression
- [Incremental Loss Recovery](./incremental-loss-recovery.md) — Similar linear approach

---

## Sources

- **Plan source:** [MarketFeeder — Lay D'Alembert](https://marketfeeder.co.uk/learn/triggers/lay-dalembert/)
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
