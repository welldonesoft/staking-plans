---
id: lay-kelly
name: Lay Kelly Criterion
category: lay
type: proportional
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Kelly for Lay Betting
---

# Lay Kelly Criterion

## Overview

The Kelly Criterion adapted for lay betting. Determines the optimal fraction of bankroll to risk as liability when you have an edge on a lay selection. As with back Kelly, most practitioners should use fractional Kelly.

## How It Works

For a lay bet, your "edge" comes from the selection losing more often than the odds imply. Kelly tells you what fraction of bankroll to risk as liability.

## Formula

$$f = \frac{q - p \times b}{b}$$

Where:
- $f$ = fraction of bankroll to risk as **liability**
- $b$ = net odds (decimal odds − 1) — this is what you pay per unit won
- $p$ = probability the selection WINS (you lose the lay)
- $q$ = probability the selection LOSES (you win the lay) = $1 - p$

**Betfair-adjusted (with commission $c$):**

$$f = \frac{q - p \times b}{b \times (1 + c)}$$

**Example:** You estimate only a 30% chance the selection wins. Lay odds are 3.0 ($b = 2$). $f = (0.7 - 0.3 × 2) / 2 = 0.05$ — risk 5% of bankroll as liability.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `edge` | number | — | Requires true win probability estimate (selection winning = you losing) |
| `commission` | number | 0.05 | Betfair commission rate |
| `fraction` | number | 0.25 | Kelly fraction (quarter recommended for lay) |

## Risk Assessment

- **Risk Level:** High (Full), Medium (Quarter)
- **Max Drawdown:** Significant at full Kelly
- **Recommended Bankroll:** 200× average liability for quarter Kelly
- **Ruin Risk:** Higher than back Kelly — lay odds typically longer, meaning more volatility

## When to Use

- You can accurately estimate the probability of selections winning (you losing)
- You specialize in lay betting with a proven edge
- Always use **fractional** (quarter or less)

## When to Avoid

- You're new to Kelly or lay betting
- Your edge estimates are rough
- The recommended fraction exceeds your comfort zone

## Betfair Exchange Notes

- The lay Kelly formula differs from back Kelly — make sure you use the right one
- Commission significantly impacts lay profitability at scale
- Consider using Lay % Liability as a simpler, safer alternative

## Related Plans

- [Kelly Criterion](./kelly-criterion.md) — Back betting equivalent
- [Lay % Liability](./lay-percentage-liability.md) — Simpler proportional lay staking
- [Lay Liability](./lay-liability.md) — Fixed liability (no edge estimation)

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
