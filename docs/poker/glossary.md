# Glossary

A quick-reference of NLHE cash terms. For the concepts that deserve real depth, follow the links to the **concept pages** ([Poker Math](concept-math.md), [Ranges & Advantage](concept-ranges.md), [Bet Sizing](concept-bet-sizing.md), [C-Betting & Lines](concept-cbetting.md)).

!!! tip "Use search"
    Fastest way to find a term is the search box (top bar). This page is grouped by category for browsing.

## Positions
- **UTG (Under the Gun)** — first to act preflop; tightest opening range.
- **MP / LJ (Middle / Lojack)** — early-middle position.
- **HJ (Hijack)** — two off the button.
- **CO (Cutoff)** — one off the button; wide stealing range.
- **BTN (Button)** — last to act postflop; widest range, highest winrate seat.
- **SB (Small Blind)** — posts the small blind; OOP postflop, worst seat.
- **BB (Big Blind)** — posts the big blind; gets a discount to defend, but plays OOP.
- **Position / In Position (IP) / Out of Position (OOP)** — acting last (IP) is a structural advantage: more information, better pot control, higher [equity realization](concept-ranges.md).
- **Initiative** — being the player who made the last aggressive action; lets you [continuation bet](concept-cbetting.md).

## Preflop actions & plays
- **RFI (Raise First In) / open-raise** — the first voluntary raise into an unopened pot.
- **Limp** — just calling the big blind preflop (rarely correct in modern NLHE; sometimes used in SB).
- **Limp-reraise** — limping intending to re-raise; a trapping line.
- **3-bet** — the first re-raise (the open is the "2-bet"). Can be **value** or **bluff/light**.
- **4-bet / 5-bet** — the next re-raises; 5-bet is usually all-in at 100bb.
- **Cold-call / flat** — calling a raise (not having already invested).
- **Squeeze** — a 3-bet after an open **plus at least one caller** — leverages dead money and the caller's capped range.
- **Isolation raise (iso)** — raising to play heads-up against a weak limper.
- **Set-mining** — calling preflop with a small pocket pair hoping to flop a set (~11.8%; needs [implied odds](concept-math.md) ≈ 15–20× the call). → [Preflop](concept-preflop.md)
- **Blind defense** — calling/3-betting from the blinds vs a steal; the BB's price (already posted) justifies a wide defending range, but realize it OOP. → [Preflop & Blind Defense](concept-preflop.md)
- **Linear vs polarized 3-bet** — see [Ranges & Advantage](concept-ranges.md).

## Postflop bet types & lines
- **C-bet (continuation bet)** — a bet by the player who led the prior street (canonically the PFR betting the flop). → [C-Betting](concept-cbetting.md)
- **Double / triple barrel** — continuing to bet the turn / river after c-betting.
- **Delayed c-bet** — the PFR's turn bet after the flop checked through.
- **Check-raise** — checking, then raising a bet behind.
- **Donk bet** — an OOP bet by the player who was *not* the prior-street aggressor (e.g., a flop check-caller leading the turn). Flop donks are rarely correct; turn donks can be. → [C-Betting](concept-cbetting.md)
- **Probe bet** — an OOP turn/river bet after the would-be c-bettor checked back.
- **Float** — calling a bet with a weak/marginal hand intending to take the pot away on a later street, often IP.
- **Float bet** — an IP bet after calling the raiser's prior-street bet.
- **Block / blocking bet** — a small bet (usually OOP) to set a cheap price and avoid facing a larger bet.
- **Stab** — betting when opponents show weakness by checking.
- **Check-back** — checking IP to end the street (pot control / give-up / trap).
- **Give-up** — abandoning a bluff line and checking/folding.

## Board & texture
- **Dry / static board** — uncoordinated, few draws (e.g., K72r); equities are "locked," favors small/frequent c-bets.
- **Wet / coordinated / dynamic board** — many draws/connectivity (e.g., T98ss); equities shift street-to-street, favors polarized/larger bets.
- **Rainbow / two-tone / monotone** — three suits / two of a suit / all one suit.
- **Paired board** — contains a pair (e.g., K K 4); c-bet often but small.
- **Board coverage** — how well your range contains the strong combos a board enables.
- **Range-favoring vs caller-favoring card** — a turn/river that helps the aggressor's range vs the caller's; drives barreling and [donk](concept-cbetting.md) decisions.

## Hands, draws & categories
- **Value (bet)** — betting a hand that wants worse hands to call.
- **Bluff** — betting a hand that wants better hands to fold.
- **Semi-bluff** — bluffing with a draw that can improve to the best hand.
- **Bluff-catcher** — a medium hand that only beats bluffs (calls to capture the opponent's bluffs).
- **Made hand** — a complete hand (pair or better) needing no improvement.
- **Nutted / the nuts** — the best possible hand (or close); **air** — no made hand and little equity.
- **Flush draw** — four to a flush. **OESD (open-ended straight draw)** — 8 outs. **Gutshot** — inside straight draw, 4 outs.
- **Combo draw** — a hand with two draws (e.g., flush draw + straight draw), high equity.
- **Backdoor draw** — needs *both* turn and river to complete (e.g., backdoor flush); adds small equity + bluff potential.
- **Equity** — your share of the pot = chance of winning at showdown given ranges. → [Poker Math](concept-math.md)
- **Outs** — cards that improve you to the likely best hand.

## Ranges → see [Ranges & Advantage](concept-ranges.md)
- **Range** — the full set of hands a player can have in a spot (think ranges, not single hands).
- **Polarized** — nuts + bluffs, no medium hands → larger sizing.
- **Linear / merged** — top-down value, strongest to medium → smaller sizing.
- **Condensed / capped** — concentrated in medium hands, lacking the nuts; an **uncapped** range still contains the strongest hands.
- **Range advantage** vs **nut advantage** — stronger overall equity vs an edge at the top of the range.
- **Equity realization (R)** — the fraction of raw equity you actually convert to winnings.
- **Balance** — mixing value and bluffs so you can't be exploited.

## Math & theory → see [Poker Math](concept-math.md)
- **EV (Expected Value)** — the probability-weighted average result of a decision.
- **Pot odds** — the price you're getting to call; **required equity = call / (pot + call)**.
- **Implied / reverse implied odds** — money won on later streets when you hit / lost when you make a second-best hand.
- **Fold equity** — EV gained from the chance your bet makes a better hand fold.
- **MDF (Minimum Defense Frequency) = pot/(pot+bet)** — minimum share of range you must continue to deny auto-profit bluffs.
- **Alpha = bet/(pot+bet)** — required fold frequency for a bluff to break even (Alpha = 1 − MDF).
- **Bluff-to-value ratio** — the mix of bluffs to value bets that makes opponents indifferent (shifts with bet size & street).
- **SPR (stack-to-pot ratio)** — effective stack ÷ pot; low SPR commits top-pair-type hands, high SPR demands stronger hands. → [Poker Math](concept-math.md), [Multiway & Stack Depth](concept-multiway.md)
- **Multiway pot** — 3+ players; MDF doesn't apply (folds are multiplicative) → bluff far less, value tighter. → [Multiway & Stack Depth](concept-multiway.md)
- **Combinatorics** — pair = 6 combos, unpaired = 16 (4 suited + 12 offsuit), 1,326 total. → [Poker Math](concept-math.md)
- **Blockers / removal** — cards you hold that reduce the combos an opponent can have.
- **GTO / Nash equilibrium** — an unexploitable strategy; can't be beaten, but doesn't maximally punish mistakes.
- **Geometric / pot geometry** — equal pot-fraction bets each street to be all-in by the river. → [Bet Sizing](concept-bet-sizing.md)
- **Overbet** — a bet larger than the pot; unlocked by [nut advantage](concept-ranges.md) + polarization.
- **Rake** — the house's cut; tightens correct ranges and lowers the value of marginal pots.

## Solver & study
- **Solver** — software that computes the GTO strategy for a spot (PioSOLVER, GTO+, GTO Wizard).
- **Node-locking** — fixing one player's strategy to a (sub-optimal) line and re-solving to find the exploit.
- **Aggregation report** — solver output across all 1,755 flops at once; the tool for extracting cross-board heuristics.
- **EV loss** — how much expected value a decision gives up vs the solver's best action; the trainer's scoring metric.
- **Sim** — a solved scenario.

## Exploitative & population
- **GTO vs exploitative** — playing the unexploitable baseline vs deviating to punish a specific opponent's mistakes (they're complementary — GTO is the baseline you deviate *from*).
- **Population read / tendency** — a pool-wide pattern (e.g., the field over-folds rivers) used to exploit unknowns.
- **Leveling** — reasoning about what the opponent thinks you have ("level" 1/2/3 thinking).
- **Thin value** — value-betting a marginal hand that gets called by worse just often enough.
- **Bluff-catch** — calling with a bluff-catcher to capture bluffs at the [MDF](concept-math.md)-implied frequency.

## Results & mental game → see [Mental Game & Variance](mental-game.md)
- **Variance** — the swing of results around your true winrate; huge in poker.
- **Resulting** — judging a decision by its outcome instead of its quality (a thinking error).
- **Tilt** — any deviation from your A-game caused by emotion.
- **bb/100** — big blinds won per 100 hands; the standard winrate unit.
- **EV (in your tracker) / all-in adjusted winrate** — your results adjusted to remove all-in luck.

---
*Definitions reflect modern solver-era consensus (GTO Wizard, Upswing, Red Chip, Run It Once, 888poker). Concept pages carry the formulas, examples, and citations.*
