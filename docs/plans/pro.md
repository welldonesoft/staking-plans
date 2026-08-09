---
id: pro
name: Pro Staking Plan
category: back
type: recovery
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Professional Staking
---

# Pro Staking Plan

## Overview

An aggressive recovery-based staking plan designed to recoup losses quickly. After a loss, the stake increases significantly to recover the lost amount plus a target profit. High risk, high potential reward — suitable only for experienced punters with large bankrolls.

## How It Works

- Set a target profit per betting cycle
- After a **loss:** Increase the next stake to cover all previous losses plus the target profit
- After a **win:** Reset to the base stake
- The stake after $n$ consecutive losses grows to recover: $\text{sum of losses} + \text{target}$

## Formula

$$S_{i+1} = \frac{\sum_{j=1}^{i} L_j + T}{o_{i+1} - 1}$$

Where:
- $S_{i+1}$ = next stake
- $\sum L_j$ = sum of all losses so far in this cycle
- $T$ = target profit
- $o_{i+1}$ = decimal odds of next selection

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `target_profit` | number | 10 | Desired profit per completed cycle |
| `base_stake` | number | 10 | Starting stake for each cycle |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Potentially severe — stakes grow with cumulative losses
- **Recommended Bankroll:** 500+ units
- **Ruin Risk:** High — a long losing streak escalates stakes dangerously

## When to Use

- You have a very large bankroll
- Your strike rate is high (>50%)
- You accept the possibility of large drawdowns

## When to Avoid

- Limited bankroll
- Low strike-rate systems
- You're uncomfortable with loss-chasing
- Betfair lay betting (liability compounds even faster)

## Betfair Exchange Notes

- For back betting, the formula is straightforward
- **Not recommended for lay betting** — the liability escalation is extreme
- Commission reduces effective recovery slightly

## Related Plans

- [Recovery](./recovery.md) — Similar aggressive recovery approach
- [Stop at a Winner](./stop-at-a-winner.md) — Recovery variant that stops after any winner
- [Secure](./secure.md) — Opposite philosophy (conservative)

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
