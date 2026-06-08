# Poker Math

The handful of formulas that actually drive decisions. All of these are verified identities — the arithmetic checks out.

## Pot odds & required equity
**Pot odds** = the price you're getting to call (pot : cost-of-call). To turn that into a decision:

> **Required equity to call = call / (pot + call)**

*Example:* calling $10 into a $30 pot → `10/(30+10) = 25%`. If your hand has ≥25% equity, calling is profitable. This is the threshold a [bluff-catcher](glossary.md) must clear.

## MDF & Alpha (the defensive pair)
When you face a bet, how much of your range must you continue with so the bettor can't just print money bluffing?

> **MDF (Minimum Defense Frequency) = pot / (pot + bet)**
> **Alpha (required fold frequency) = bet / (pot + bet)**
> **MDF + Alpha = 1**

*Derivation:* a 0%-equity bluff has EV `= f·pot − (1−f)·bet`. Set to 0 → fold freq `f = bet/(pot+bet)` = Alpha; so you must defend `pot/(pot+bet)` = MDF.

| Bet (into pot of 100) | MDF (you defend) | Alpha (you fold) |
|---|---|---|
| ½ pot (50) | **67%** | 33% |
| ⅔ pot (66) | 60% | 40% |
| Pot (100) | **50%** | 50% |
| 2× pot overbet (200) | **33%** | 67% |

**Bigger bets → you fold more.** That's the mathematical engine behind [overbetting](concept-bet-sizing.md) with a polarized range.

!!! warning "MDF is a baseline, not a law"
    MDF assumes bluffs have **zero equity** and ignores **rake** and **blockers**. In practice you defend based on your hands' actual equity and removal — MDF is the floor that stops *pure* bluffs from auto-profiting, and a starting point you deviate from when you have reads.

## Bluff-to-value ratio
A polarizing bettor includes enough bluffs to make the caller's bluff-catchers **indifferent**. Mechanically, the **bluff share of the betting range = Alpha = bet/(pot+bet)** — the same fold-equity threshold. On the **river**, by size:

| River bet | Value : Bluff |
|---|---|
| ½ pot | ~2 : 1 |
| Pot | ~1 : 1 |
| 2× pot | ~1 : 2 |

Bigger bets → *more* bluffs allowed. On **earlier streets you can bluff more** because your "bluffs" still have equity/outs to improve (they're not pure bluffs), so the mix is more bluff-heavy on the flop/turn and **tightens toward the river** as equity crystallizes.

!!! note "These are the textbook ratios"
    The 2:1 / 1:1 / 1:2 figures are the standard *consequence* of Alpha — the Alpha/MDF math is exact, but real solver river ratios **deviate slightly** due to card removal and range composition. Use them as anchors, not gospel.

## EV, equity, fold equity
- **EV (Expected Value)** — the probability-weighted average outcome; everything else is in service of making +EV decisions.
- **Equity** — your share of the pot = chance of winning given both ranges.
- **Fold equity** — extra EV from the chance your bet folds out a better hand. Total bet EV ≈ (fold equity) + (equity when called).
- **Implied odds** — money you expect to win *later* when you hit (improves a draw's price). **Reverse implied odds** — money you expect to *lose* later with a second-best hand.

## Combinatorics
Counting combos is the basis of [hand reading](hand-reading.md) and bluff/value selection.

- **Pocket pair = 6 combos** · **Unpaired = 16** (4 suited + 12 offsuit) · **1,326 total** starting combos.
- **Card removal (blockers)** reduces combos multiplicatively:
    - Unpaired = (copies of card A left) × (copies of card B left)
    - Paired = `n(n−1)/2` for `n` unseen copies
    - *Examples:* an Ace out → AQ = `3×4 = 12`; holding KQ on K-T-4 → AK = `4×2 = 8`; TT on K-T-4 → `(3×2)/2 = 3`.

## SPR (stack-to-pot ratio) & commitment
**SPR = effective stack ÷ pot** at the start of a street. The equity you need to profitably stack off **rises with SPR** as `risk/(risk+pot)`:

| SPR | Equity to stack off | What can commit |
|---|---|---|
| **1** | ~33% | almost any pair / draw |
| **2** | ~40% | **any top pair** (+ most 2nd pairs, a few lower pairs) |
| **3** | ~43% | top pair, strong draws |
| **5** | higher | top pair gets **dicey**; OESDs become **pure folds** |
| **16 (deep)** | — | even **top pairs & nut flush draws are only *indifferent*** |

So **3-bet pots (low SPR)** play for stacks with one pair; **deep/limped pots (high SPR)** demand much stronger hands and reward implied odds + playability.

## Exploitability & Nash distance
**Nash Distance (dEV)** measures how far a strategy is from equilibrium = the most EV the best counter-strategy could win off it (0 = perfect equilibrium). At equilibrium, **every mixed action has equal EV** (the indifference condition).
- Reported as a **% of pot** → convertible to bb/hand (e.g., 0.3% of a 5.5bb pot ≈ **0.017 bb/hand** exploitable).
- **Solvers converge to ~0.2–0.3% of pot** — far more precise than any human. The **EV-loss** of one of your decisions is this same idea applied to a single action: how much you concede vs the best response. (It's exactly what the GTO Wizard trainer scores.)

## Rake
**Rake is paid by the player closing the action**, which **worsens the caller's pot odds** (like virtually enlarging the bet).
- Effect: the **defender tightens** (the BB calls less everywhere, shifting to folds and check-raises), while the **aggressor can bluff *more*** — e.g. an NL100 BTN-vs-BB flop where BTN bets trash **45% raked vs 36% unraked**.
- The **rake cap** limits this once pots grow large, so the distortion is **biggest in small/marginal pots** — which is why rake quietly **tightens opening ranges** and trims the profit of steals, light 3-bets, and thin pots.

---
*Sources: [Pot odds](https://en.wikipedia.org/wiki/Pot_odds) · [MDF & Alpha](https://blog.gtowizard.com/mdf-alpha/) · [Combinatorics](https://blog.gtowizard.com/a-beginners-guide-to-poker-combinatorics/) · [Card removal](https://www.thepokerbank.com/strategy/mathematics/hand-combinations/) · [SPR](https://blog.gtowizard.com/stack-to-pot-ratio/) · [Nash distance](https://blog.gtowizard.com/understanding-nash-distance/) · [Rake](https://blog.gtowizard.com/customizable-raked-solutions-with-gto-wizard-ai/)*
