# Database Review & Leak-Finding

Your tracker tells you **what to study in the first place.** Studying random spots is guessing; studying *your actual leaks* is [deliberate practice](../deliberate-practice.md). This is how you find them — and how to avoid being fooled by small samples.

## Find leaks by comparing to *winners*, not the pool

Pull your core stats (VPIP, PFR, 3-bet, fold-to-3bet, c-bet flop/turn, fold-to-c-bet, WWSF, WTSD, W$SD, aggression) and compare them against **the biggest winners at your stake** — **not** the pool average.

> The average player is a *losing* player, so matching pool averages is worthless. Match (and understand) what the winners do.

## Stats alone lie — filter to the actual hands

A "60% turn-barrel" number means nothing without context. Use your tracker's filters (PokerTracker's **Actions & Opportunities**, HM3's filter editor) to pull the **specific hands** behind a suspicious stat — which boards, which opponents, which lines. The stat flags a *maybe*; the hands tell the story.

## Sample size: trust opportunities, not raw hands

A stat is only as reliable as the number of times its *situation* came up:

| Reliability | Opportunities |
|---|---|
| Working minimum | ~10 |
| Solid | 10–30 |
| Trustworthy | **30+** |

**Preflop frequency stats** (VPIP, PFR, RFI) stabilize fast. **Turn/river stats** need far more — fold-to-turn-cbet ~300+ hands, river stats ~1,000+. A flashy read on a tiny sample is noise.

## Population reads (no solver needed)

Your database *is* a population model. Build a report across **all players** in your DB (grouped by stake) to get pool-wide tendencies — how often the field folds to 3-bets, calls steals, etc. These **population reads** are how you exploit unknown opponents, and they feed [node-locking](solver-study.md) and [hand reading](hand-reading.md).

## The variance reality check

You cannot read your *results* over short samples — variance is enormous. Standard deviation in 6-max NLHE is ~**90–100 bb/100**, which means:

!!! warning "Even 100,000 hands isn't certain"
    At 100k hands, your true winrate is pinned only to about **±5.6 bb/100**. A measured 5 bb/100 could really be anywhere from ~0 to ~11. So **never change your strategy off a downswing** within a normal sample — judge your *decisions*, not your graph. → [Mental Game & Variance](mental-game.md)

*(Compute your own confidence intervals with a variance calculator: `95% CI = winrate ± 1.96 × SD ÷ √(hands/100)`.)*

## Key takeaway

**Diagnose before you study.** Compare to winners, filter to real hands, trust 30+ opportunities (not raw hands), mine population reads — and never let a small-sample graph dictate strategy.

---
*Sources: [HUD stat sample sizes](https://www.blackrain79.com/2017/11/poker-hud-stat-sample-size.html) · [database review method](https://www.blackrain79.com/2014/03/how-to-conduct-poker-database-review.html) · [variance](https://www.primedope.com/poker-variance-calculator/)*
