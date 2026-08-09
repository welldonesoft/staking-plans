---
id: kelly-criterion
name: Kelly Criterion
category: back
type: proportional
risk: high
betfair_compatible: true
aliases:
source: tsm
  - Full Kelly
  - Kelly Staking
---

# Kelly Criterion

## Overview

The mathematically optimal staking fraction for maximizing long-term bankroll growth, given a known edge. Developed by John L. Kelly Jr. at Bell Labs (1956). Full Kelly is aggressive; most practitioners use **Fractional Kelly** (½ or ¼).

## How It Works

Kelly compares your estimated true probability with the implied probability of the odds. When you have an edge, it tells you what fraction of bankroll to stake to maximize compound growth.

## Formula

$$f = \frac{bp - q}{b} = \frac{p(b + 1) - 1}{b}$$

Where:
- $f$ = fraction of bankroll to stake
- $b$ = net odds received (decimal odds − 1)
- $p$ = your estimated true probability of winning
- $q$ = probability of losing ($1 - p$)

**Betfair-adjusted (with commission $c$):**

$$f = \frac{bp - q}{b(1 + c)}$$

**Example:** You estimate a true 60% win probability. Odds are 2.0 (even money, $b = 1$). Full Kelly: $f = (1 × 0.6 - 0.4) / 1 = 0.20$ — bet 20% of bankroll.

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `edge` | number | — | Your estimated edge (requires true probability estimate) |
| `commission` | number | 0.05 | Betfair commission rate (5% default, adjustable with discount) |
| `fraction` | number | 1.0 | Kelly fraction: 1.0 = full Kelly, 0.5 = half, 0.25 = quarter |

## Risk Assessment

- **Risk Level:** High (Full Kelly), Medium (Half), Low-Medium (Quarter)
- **Max Drawdown:** 50%+ drawdowns common with Full Kelly
- **Recommended Bankroll:** 100× average stake for Full Kelly
- **Ruin Risk:** Low mathematically, but high practically if edge is overestimated

## When to Use

- You can reliably estimate your edge (true probability vs market)
- Long-term growth is the primary goal
- You can tolerate high volatility
- Use **Quarter Kelly** for practical, sustainable betting

## When to Avoid

- You can't estimate true probabilities accurately ("garbage in, garbage out")
- You have a small bankroll (relative swings too large)
- You need emotional stability (volatility is stressful)
- Your bets are correlated (Kelly assumes independence)

## Betfair Exchange Notes

- **Always use the commission-adjusted formula** — otherwise you'll systematically overbet
- Lay Kelly formula differs; see [Lay Kelly](./lay-kelly.md)
- Commission discount (e.g., 2% instead of 5%) significantly improves effective growth rate

## Related Plans

- [Fractional Kelly](./kelly-criterion.md#fractional-kelly) — Half/Quarter Kelly (same formula, multiplied by fraction)
- [Percentage Staking](./percentage-staking.md) — Simpler proportional approach
- [Square Root](./square-root.md) — Slower-scaling alternative
- [Lay Kelly](./lay-kelly.md) — Lay-specific Kelly variant

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
