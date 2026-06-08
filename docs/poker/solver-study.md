# Solver Study & Heuristics

How to turn a solver from a thing you *stare at* into a thing you *learn from*. The goal is never to memorize outputs — it's to extract **a few transferable rules** you can actually use at the table.

## Read range-first, not hand-first

When you open a solution, resist looking up "what does my hand do?" Instead, zoom out:

1. **Aggregate first:** what % of the *range* bets vs checks? At what sizes?
2. **Then the pure strategies:** which hands *always* do one thing? (e.g., "nutted hands always bet"). These are your anchors.
3. **Treat mixed strategies as indifference, not instructions.** A hand that bets 50% means both lines are about equal EV — **do not** try to memorize the percentage. Understanding *why* it's indifferent is the lesson.

## Aggregation reports = the heuristic machine

The single most valuable solver feature for learning. An **aggregation report** shows the strategy across *all 1,755 distinct flops* at once, sortable and filterable. Instead of studying one board, you see the **pattern across textures** — which is exactly the [transferable principle](../transfer-and-sleep.md) you want, not a memorized board.

Use it to answer questions like: *"How does my turn-barrel frequency change by turn card?"* — then write down the rule.

## Node-locking for exploits

To study how to beat a *specific* tendency (your pool over-folds turn, say), **node-lock** the opponent's strategy to that mistake and re-solve. The solver shows you the **maximally exploitative response.** This is how you turn population reads into concrete adjustments. → see [Hand Reading & Reads](hand-reading.md)

## The weekly solver loop

1. **Target a high-frequency, recurring spot** (not the random big pot you lost).
2. If it's new to you, **study the solution first** (it's complex — [worked examples beat struggling when you're new](../cognitive-load.md)).
3. Run the **aggregation report**; find the cross-board pattern.
4. **Distill 3–5 heuristics** — write the *rule + the why*.
5. **Card them** in [Anki](anki-for-poker.md), then **drill them closed-book** ([Drilling](drilling.md)), then **test in play.**

!!! tip "The output is rules, not memories"
    A good solver session ends with **3–5 written heuristics**, each with a reason. If you finish a session having "looked at a lot of sims" but can't state the rules you extracted, you studied the wrong way.

## Key takeaway

**Study ranges, extract rules, ignore the noise.** Read aggregate-first, treat mixed strategies as indifference, and leave every session with a handful of *why*-backed heuristics you can drill and test — not a pile of memorized frequencies.

---
*Sources: [GTO Wizard — aggregation reports](https://blog.gtowizard.com/introducing_custom_aggregated_reports/) · [PioSOLVER — node locking](https://piosolver.com/docs/viewer/node_locking/) · [Using a solver effectively](https://thinkgto.com/blog/how-to-use-a-poker-solver-effectively)*
