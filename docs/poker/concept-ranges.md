# Ranges & Advantage

Advanced poker is played with **ranges**, not hands. These are the concepts that let you reason about an entire range at once.

## Range morphology (shape)

| Shape | What's in it | Typical sizing | When |
|---|---|---|---|
| **Polarized** | Nuts + bluffs ("nuts/napkins"), **no medium hands** | **Large / geometric / overbet** | IP, rivers; when you have a [nut advantage](#range-advantage-vs-nut-advantage) |
| **Linear / merged** | Top-down value (strongest → medium), **no air** | **Small** | When the opponent can **only fold or call** (one continuation action) |
| **Condensed / capped** | Concentrated in **medium** hands, lacks the nuts | Check / call-heavy | The flat-caller's range; can't credibly make big bets |
| **Uncapped** | Still contains the **strongest** hands | Can bet big | The aggressor / 3-bettor's range |

**Why shape dictates sizing:** you can only bet big *credibly* when your range contains the nuts (polarized/uncapped). A capped range that bets big is bluffing too often and gets punished.

!!! note "Linear backfires vs folders"
    A linear (value-heavy) range works against players who **over-call**, but loses value against players who **over-fold** — you're betting hands that wanted calls into people who won't call. Match the shape to the opponent.

## Range advantage vs nut advantage
These are **different**, and the difference decides your sizing:

- **Range advantage** = your *overall* equity distribution is stronger on the board.
- **Nut advantage** = you hold *disproportionately more of the strongest* hands (the top of the range).

You can have one without the other. **Nut advantage — not mere range advantage — is what justifies large bets and overbets**, because the threat of the nuts is what makes big bets credible and pressures the opponent's capped range.

*Example:* on K-J-3, the preflop raiser has both range and nut advantage → can bet large/often. On 8-5-4, the raiser may keep a slight range edge but **loses the nut advantage** (the caller has more sets and two-pair) → must check far more.

## Equity realization (R / EQR)
**R = the fraction of your raw equity you actually convert into winnings** = `pot-share ÷ equity` = `EV ÷ (pot × equity)`. (So `equity × R × pot = EV`.) Win 70% of the pot on 40% raw equity → R = `0.7/0.4` = **175%**.

- **R > 100% (over-realize)** — strong made hands, draws with implied odds, and **hands played IP with initiative**.
    - AA vs 72o (~88% eq) → **114%** if villain folds, up to **186%** all-in.
    - A flush/straight draw can realize **~148%** of its raw equity via implied odds.
- **R < 100% (under-realize)** — weak, capped, marginal, offsuit, **OOP** hands.
    - A marginal KJs (~55% eq) → ~**77%** (reverse implied odds — it plays like a bluff-catcher).

!!! note "Position dominates R"
    The *same hand* (A2s) can realize **~100% in position** but **<2% out of position** on a given board. That's *why* position is worth so much — it's not just information, it's equity you actually get to **keep**.

*(Caveat: those are verified single-spot illustrations, not class averages — under-realization is directional, not a universal "OOP = low R" law.)*

## Balance
A **balanced** range mixes value and bluffs in the right ratio ([see the math](concept-math.md)) so an opponent can't exploit you by always-calling or always-folding. Balance is the GTO baseline; you deliberately *unbalance* (deviate) to [exploit](hand-reading.md) specific opponents.

---
*Sources: [Range morphology](https://blog.gtowizard.com/range-morphology/) · [Range advantage](https://gtowizard.com/en/glossary/range-advantage/) · [Nut advantage](https://pokercoaching.com/blog/dominating-with-nut-advantage-a-key-edge-in-poker-strategy/) · [Polarized vs linear](https://upswingpoker.com/polarized-vs-linear-ranges/)*
