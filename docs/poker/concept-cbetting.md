# C-Betting & Postflop Lines

The continuation bet is the most common postflop decision. Here's the solver-era theory, plus the non-c-bet lines (donk, probe, float) and the math of bluffing across streets.

## The continuation bet (c-bet)
A **c-bet** is a bet by the player who held the betting lead on the previous street (canonically the preflop raiser betting the flop). Whether and how big to c-bet is governed by [range & nut advantage](concept-ranges.md) on the board.

## C-betting in 3-bet pots
- **High c-bet frequencies are usually correct — even out of position.** The 3-bettor's equity advantage plus the **low SPR** make position matter less.
- **Range-advantaged boards** (King-high / broadway, e.g. KJ3r) → you can **bet your entire range**, OOP, with *zero* checking.
- **Range-disadvantaged boards** (5-to-9-high, e.g. 854r) → the 3-bettor **loses both range and nut advantage** (the caller has more sets, 77–66, suited connectors like 87s/76s) → check far more (~⅔), bet large with the rest. **Unmade hands without backdoor potential → check-fold.**

## Preflop range asymmetries (why the above happens)
- An **OOP 3-bettor structurally has a stronger range than an IP caller** (more risk, closes the action). ~40bb: BB-vs-UTG ≈ 54% vs 46%.
- The **tighter the seat you opened from, the bigger your edge over the blinds** (they defend wide and weak).

## Non-c-bet lines
- **Delayed c-bet** — PFR bets the turn after the flop checked through; picks up the pot when the flop check showed mutual weakness.
- **Donk bet** — the *non-aggressor* (e.g., flop check-caller) leads into the prior aggressor.
    - **Flop donks are rarely correct** — flat-calling the flop *caps* your range and magnifies the raiser's nut advantage.
    - **Turn donks are valid** on cards that **disproportionately promote the caller's medium hands to monsters** (cards more likely in the caller's range than the bettor's).
- **Probe bet** — OOP turn/river bet after the would-be c-bettor checked back (attacking shown weakness).
- **Float** — calling with a weak hand IP planning to take it away later; **float bet** = the IP bet after that call.

## The math of multi-street bluffs
**Evaluate the whole line, not street-by-street.**

- Multi-street bluffs have a **worse risk-reward** than single-street bluffs — you risk more across streets than you stand to gain.
- A **profitable river bluff does not automatically offset** unprofitable flop/turn bluffs — you must compute the **EV of the entire line.**

!!! example "Worked line"
    A turn barrel can be **−0.37 pots** on its own yet sit inside a **+0.528-pot** triple-barrel line — or not. You only know by adding up the streets. *(Against an over-folding population, lines that are −EV vs equilibrium can become +EV — that's an [exploit](hand-reading.md).)*

## The takeaway
> C-bet **frequently and small on boards you own**; **check more on boards that hit the caller**; pick **bluffs with equity/backdoors** and **give up** the rest; and judge a bluff by the **whole line's EV**, not one street.

---
*Sources: [C-betting OOP in 3BP](https://blog.gtowizard.com/c-betting-oop-in-3-bet-pots/) · [Range disadvantage as 3-bettor](https://blog.gtowizard.com/navigating-range-disadvantage-as-the-3-bettor/) · [Turn donk bets](https://blog.gtowizard.com/how-and-why-you-should-use-turn-donk-bets/) · [Math of multi-street bluffs](https://blog.gtowizard.com/the-math-of-multistreet-bluffs/)*
