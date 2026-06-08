# Preflop & Blind Defense

The preflop decisions that come up most — and the math behind them.

## Why the Big Blind defends so wide
The BB defends a *huge* range vs a steal for two structural reasons: it has **already posted the blind** (a price discount) and it **closes the action** (no one can re-raise behind).

*Example* — $1/$2, 100bb, vs a **2.5x button open**: the BB defends **~51.7%** of hands, continuing down to ~K7o/Q8o.

**Pot odds:** a 2.5bb open means the BB calls 1.5 into a 4bb pot = 2.67:1 = only **~27% break-even equity** (≈28.6% after rake).

!!! warning "But equity ≠ what you can call"
    That ~27% pot-odds number **understates** the real bar, because the BB realizes equity poorly out of position ([low EQR](concept-ranges.md)). So the *actual* defending range is **tighter** than raw pot odds suggest — you need hands that can actually realize their equity OOP, not just clear the 27% line.

## Small Blind: 3-bet-or-fold
In **raked** games, play the SB almost always as **3-bet-or-fold** (no flatting range). Why:
- A flatting range is **capped** (middling pairs, offsuit broadways, suited wheel aces) and gets **squeezed relentlessly** by the BB.
- A wide flat **can't beat the rake**, and the SB **doesn't close the action** — flatting invites a multiway pot from the worst seat.
- Flatting only becomes viable in **unraked** games (where the flat range is very wide) or vs weak/passive players.

## Limping & the limp-reraise
- **Open-raising > open-limping** as a rule (generates fold equity, builds value, avoids a capped/face-up range, reduces multiway pots). Narrow exceptions: loose-passive games, SB completes, some speculative hands.
- **Limp-reraise** = a trap: limp to look weak, induce a raise, then re-raise. Best from **early position (UTG)** with **premiums (AA/KK/QQ, sometimes AK)** when aggressive players sit behind.

## Set-mining
Calling a raise with a small pocket pair to flop a set:
- **You flop a set (or better) ~11.8%** of the time — about **1 in 8.5** (~7.5:1 against). You miss ~88%.
- **Implied-odds rule of thumb:** you want effective stacks ≈ **10–20× the call** behind:
    - ~8× = bare break-even · **10×** = loose floor · **12–15×** = conservative.
    - The **"5–10 rule" / "Call-20":** risk **≤5% of your stack** (up to 10% in special cases) — i.e. need ~20× — is the standard safe figure.
    - Modern solver-era theory trends **higher (15×+)** because you win a smaller fraction of stacks than old literature assumed.

## Key takeaway
**Defend the BB wide but realistically (EQR, not just pot odds); play the SB as 3-bet-or-fold in raked games; raise rather than limp (save the limp-reraise for premiums in EP); and set-mine only with ~15–20× behind.**

---
*Sources: [BB defense](https://upswingpoker.com/big-blind-defend-strategy-mtt-vs-cash/) · [SB preflop](https://upswingpoker.com/podcast/ep16-small-blind-preflop/) · [Limp-reraise](https://www.pokernews.com/strategy/10-more-hold-em-tips-should-you-ever-limp-reraise-25574.htm) · [Set-mining](https://upswingpoker.com/set-mining-poker-tips/) · [Flop odds](https://pokercoaching.com/blog/odds-of-flopping-poker-hands/)*
