# Multiway & Stack Depth

Two situations where the heads-up solver intuition breaks down — and you must adjust.

## Multiway pots (3+ players)

### MDF does NOT apply per-player
This is the big one. With multiple defenders, folding frequencies are **multiplicative**, not per-person. Two defenders can **each fold ~70%** and still *jointly* meet a 50% [MDF](concept-math.md) (`0.7 × 0.7 = 49%`). So **each player defends only ~30% of range vs ~50% heads-up.**

And the split is **unequal**: the **middle player** (someone still to act behind) folds **more** (~80%); the **player closing the action** folds **less** (~60%). *(Average fold frequency per player ≈ Alpha^(1/n).)*

### How to adjust as the bettor
Because everyone is continuing tighter, multiway you must:

- **Bluff far less** — almost never bluff a hand **without solid drawing equity**.
- Carry a **stronger value range** and **value-bet more carefully / thinner only when justified**.
- **C-bet less often** overall.
- Need **more equity** to keep firing on later streets.

> Intuition: one extra player roughly *squares* the chance someone has a real hand. Pure bluffs that print heads-up are lighting money on fire multiway.

## Stack depth (100bb vs deep)

**Deep = >100bb** (150–200bb are the usual "deep" examples). As stacks get deeper:

- **Speculative & implied-odds hands gain value** — suited connectors, small pairs (**set-mining improves**) — because you can win a bigger stack when you hit.
- **Position becomes more valuable** (more streets of post-flop maneuvering = more chances for the IP player to [over-realize](concept-ranges.md)).
- **Sizing shifts:**
    - OOP **3-bets grow** to ~**10–11bb** (vs ~9bb standard).
    - IP **4-bets** go from ~**2× the 3-bet at 100bb** to ~**3× at 200bb** (giving callers worse odds).
- **4-betting reduces the value of position** — it either ends the hand preflop or **slashes the [SPR](concept-math.md)**, removing the IP player's room to out-play the opponent post-flop.

## Key takeaway
**Multiway: tighten up, bluff almost only with equity, MDF doesn't apply. Deep: lean into speculative/IP hands and set-mining, size 3-bets/4-bets up — and remember 4-betting trades away your positional edge by crushing SPR.**

---
*Sources: [Multiway MDF](https://www.mypokercoaching.com/playing-profitably-in-mutliway-pots-mdf/) · [Multiway tips](https://blog.gtowizard.com/10-tips-multiway-pots-in-poker/) · [Deep-stack strategy](https://upswingpoker.com/deep-stack-strategy-tips/) · [IP 4-betting deep](https://blog.gtowizard.com/ip-4-betting-in-deep-stacked-cash-games/)*
