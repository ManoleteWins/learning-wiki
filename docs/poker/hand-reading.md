# Hand Reading & Reads

The skills that let you *use* solver knowledge and *deviate* to exploit — and they work independently of any solver. GTO gives you a baseline; **hand reading and reads are how you actually win money off it.**

## Hand reading is deduction, not magic

Strong players think in **ranges, not specific hands.** You start from all **1,326** possible starting combos and **narrow** the range street by street, eliminating every hand that wouldn't have taken the action you saw — ideally down to a handful by the river.

### The DEAF framework (SplitSuit)
A reusable, solver-free way to build a range:

- **D**efine the action (what exactly did they do?)
- **E**stimate the frequency (how often do they do that?)
- **A**xe out inconsistent hands (remove what doesn't fit)
- **F**actors (player tendencies, stats, history)

The same action from two players means **different** ranges — that's the exploitative edge a solver baseline alone misses.

## Combinatorics by hand

Know these cold — they're the foundation of accurate reads, thin value, and bluff-catches:

- **Pocket pair = 6 combos**
- **Unpaired = 16** (4 suited + 12 offsuit)
- **AK = 16 combos** (not "one hand")
- 169 hand types, **1,326 total combos**

## Blockers (mentally computable)

Holding a card removes combos from your opponent's range:

- An **Ace** cuts AA from 6→3, AK from 16→12.
- **Broadway cards** block much of a tight range's flushes (Q♥J♥ blocks most heart flushes).
- **Action blockers:** "they'd have raised that draw on the flop, so I can remove it."

## GTO and exploit are complementary

This is the resolution of the whole "solvers vs feel" debate: **GTO is the prerequisite that *enables* exploitation.**

- A solver baseline tells you the balanced default.
- **Population/specific reads** ([from your database](database-review.md)) tell you how a real opponent *deviates*.
- You then **deviate from the baseline to punish their deviation** — that's where the money is.

!!! note "Why this matters even if you're solver-literate"
    The biggest edges come from *opponent-specific* deviations, not from playing a perfect GTO baseline against people who aren't. Hand reading + reads are what turn solver knowledge into profit.

## Key takeaway

**Read ranges by deduction, count combos and blockers by hand, and use reads to deviate off your GTO baseline.** The solver is your map; hand reading is how you drive.

---
*Sources: [hand reading as logical deduction](https://www.pokervip.com/strategy-articles/texas-hold-em-no-limit-advanced/hand-reading-a-logical-process) · [DEAF framework](https://www.splitsuit.com/poker-ranges-reading) · [combinatorics & blockers](https://www.getcoach.poker/articles/poker-combinatorics-and-blockers-a-simple-guide/)*
