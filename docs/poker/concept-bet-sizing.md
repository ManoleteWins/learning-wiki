# Bet Sizing

How big to bet is mostly downstream of your [range shape](concept-ranges.md). Here's the theory, then the practical heuristics.

## Geometric sizing (pot geometry)
**Bet an equal fraction of the pot on each remaining street so your final river bet is exactly all-in.**

For a **perfectly polarized, static-equity range**, geometric sizing is **EV-optimal** — it maximizes the total money the opponent contributes by forcing the widest *cumulative* defense.

!!! example "Why geometric beats jamming"
    Pot $100, $1,300 behind. Three pot-sized bets → opponent defends `0.5³ = 12.5%` of range, contributing **~$162.50**. A single $1,300 shove → MDF `100/1400 ≈ 7%`, contributing **~$91**. The smooth geometric line extracts **nearly double**.

*Caveat:* this maximization is exact only for perfectly polarized, static ranges — which **rarely occur**. Most real solver spots are non-geometric.

## Larger-than-geometric (overbets) on early streets
Solvers sometimes bet **>geometric** (even 150% pot on the flop). Why? **Strong-but-vulnerable** hands want to **frontload** their value — get money in *now*, while they're ahead, because future cards will erode their equity. Overbetting also leans on [nut advantage](concept-ranges.md): only a range full of nutted hands can credibly bet that big.

## Practical c-bet sizing heuristics (single-raised pots, IP)
From solver aggregate data:

- **Dry/static boards → small & frequent** (e.g., ~⅓ pot). Equities are locked; you deny equity cheaply and bet a wide range.
- **Wet/dynamic boards → bigger & more polarized, less often.** Fold equity is valuable when draws are live; you bet your strong hands + good draws bigger and check more medium hands.
- **Paired boards → c-bet often, but small.**
- **Boards that complete straights/flushes in the caller's range → size down and bet less** (your nut advantage shrank).

## The unifying principle
> **Big bets require a credible top of range.** Size up when you're **polarized** and hold the **nut advantage**; size down (or check) when your range is **capped** or **medium-heavy**. Sizing is a *consequence* of range shape, not a free choice.

---
*Sources: [Pot geometry](https://blog.gtowizard.com/pot-geometry/) · [Larger-than-geometric sizing](https://blog.gtowizard.com/why-so-much-an-exploration-of-larger-than-geometric-bet-sizing/) · [c-bet sizing mechanics](https://blog.gtowizard.com/the-mechanics-of-c-bet-sizing/) · [IP c-bet heuristics](https://blog.gtowizard.com/flop-heuristics-ip-c-betting-in-cash-games/)*
