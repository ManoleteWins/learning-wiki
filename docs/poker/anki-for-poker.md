# Anki for Poker

Anki is [spaced retrieval practice](../spaced-practice.md), automated — your daily ~10-minute layer that keeps ranges and heuristics from decaying. It does **not** replace drilling; it *maintains* what drilling builds.

## What Anki is (and isn't) for

- **It is for:** the *why*-backed heuristics you extract, boundary range decisions, and rare-but-important spots the random Trainer draw won't surface often.
- **It is not for:** replicating the Trainer. The Trainer drills the full spot distribution in context; Anki holds the **principles** and **edge cases**. Don't card your whole game.

!!! warning "Keep the deck lean"
    A huge deck of easy recognition cards is the [fluency-illusion trap](../feedback-and-metacognition.md) — it feels productive and isn't. A small deck of atomic, *production-forcing* cards beats a big passive one.

## What to card

- **Heuristic cards:** front = a concrete spot; back = **action + size + one-line why.** Always include the *why* (it's what transfers).
    > *"BTN vs BB SRP, turn is an overcard that favours my range — barrel freq + why?"* → *"High freq, small/med — my range stays uncapped and the card improves me more than the caller."*
- **Boundary range cards:** drill the *marginal* hands where the decision is close (not the obvious nuts/trash). Or use **Image Occlusion** on a range chart (mask a region, recall it).
- **A formation isn't a card** — it's a *tag*. Tag cards `formation::srp-btn-vs-bb`, `node::turn-barrel`, so a formation's cards accumulate as you study its nodes over time.

## Four rules for good cards

1. **Atomic** — one fact per card.
2. **Force production** — the front must make you *generate*, not just recognize.
3. **Decision, not definition** — front is a spot, back is action + why.
4. **Be specific** — exact position, action, size, depth, or cards interfere.

## Settings that match the routine

- **Turn on FSRS**, desired retention **~0.90** (it implements expanding intervals automatically).
- **Learning steps → `1m`** (so one "Good" graduates a card to days, no in-session bouncing).
- **New cards/day ~5–10**, **max reviews/day ~150–200**.
- **Maximum interval ~6–12 months**, so even well-known material resurfaces at least once or twice a year (nothing decays silently).

## How to grade a card

You're scoring **recall of the heuristic**, not solver-perfection (that's the Trainer's job). Use a tolerance band:

- **Again** — blanked or wrong primary action.
- **Hard** — right action but missed the size/why, or struggled.
- **Good** — recalled action + size + why within tolerance, promptly. *(Your default.)*
- **Easy** — instant and trivial (rare).

**Grade honestly** — lenient grading recreates the illusion of competence and tells the scheduler to space cards too far out.

## When to make cards

Make the card **when you extract the heuristic** (during study), while it's fresh — *not* months later when it retires. FSRS then ages it automatically: seen often when new, rarely once mastered. The "long tail" is where old cards *end up*, not where you start adding them.

## Key takeaway

**Small, atomic, *why*-backed cards, made the moment you learn something, graded honestly.** Anki maintains the map daily; the Trainer builds the skill. Don't mix up their jobs.

---
*Sources: [players using Anki for ranges](https://day9.tv/dk30/project/602bf8604b321303ed4e868d) · [FSRS / spaced repetition](https://laplab.ucsd.edu/articles/Cepeda%20et%20al%202008_psychsci.pdf)*
