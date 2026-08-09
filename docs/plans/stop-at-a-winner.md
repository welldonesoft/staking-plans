---
id: stop-at-a-winner
name: Stop at a Winner (SAW)
category: back
type: recovery
risk: high
betfair_compatible: true
aliases:
source: tsm
  - SAW
  - Stop At Winner
---

# Stop at a Winner (SAW)

## Overview

A recovery staking plan that escalates stakes after losses but resets completely after **any** winner. The idea: you only need one win to wipe out all accumulated losses and return to profit. Riskier than standard recovery because it aims to recover everything in a single win.

## How It Works

1. Start with a base stake
2. **Loss:** Calculate next stake to recover all losses + target profit at the upcoming odds
3. **Win:** Reset entirely to base stake
4. Continue until a winner occurs, then restart

## Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `base_stake` | number | 10 | Starting stake for each cycle |
| `target_profit` | number | 0 | Additional profit target per cycle |

## Risk Assessment

- **Risk Level:** High
- **Max Drawdown:** Escalates with each consecutive loss
- **Recommended Bankroll:** 500+ units
- **Ruin Risk:** High — one long losing streak can be catastrophic

## When to Use

- Very high strike rate (>60%)
- Short losing streaks are the norm for your system
- You have a very large bankroll

## When to Avoid

- Low strike-rate systems
- Long-odds betting (fewer winners = longer streaks)
- Lay betting (liability compounds dangerously)
- You don't have a hard stop-loss

## Comparison: SAW vs Standard Recovery

| | SAW | Standard Recovery |
|---|---|---|
| After a win | Full reset | Full reset |
| Stake growth | Must recover all losses in one bet | Can spread recovery |
| Risk | Higher (fewer bets to recover) | Slightly lower |

## Betfair Exchange Notes

- For lay SAW, the liability after a few losses becomes enormous — not recommended
- Back-only is the safer application

## Related Plans

- [Recovery](./recovery.md) — Similar but may spread recovery across bets
- [Pro](./pro.md) — Recovery with fixed target per cycle

---

## Sources

- **Plan catalog reference:** [The Staking Machine](https://thestakingmachine.com/staking-plans/) — staking plan software with 50+ plans
- **Plan mechanics:** Mathematical formulas and plan concepts are in the public domain
