# Auction Initiator Variants

> ⚔️ **TO ARGUE** — This mechanic is unresolved and needs a proper design debate with Ruzgar before any decisions are made. Do not move to Core Mechanics until settled.

> The one who names the price first should not be punished for it. But they should not be invincible either.

## The Problem

In a standard ascending auction, the initiator has *no mechanical advantage*. They must either bid high from the start (costly and committing) or bid low and risk being sniped at minimal cost by opponents. A player who opens at 1 has essentially done the work of starting the auction and received nothing for it.

The goal: give the initiator something — without making initiating a guaranteed win.

---

## Variant A: Tiered Initiator Threshold *(Original Concept — TBD)*

The initiator's opening bid determines the **protection tier** — how much an opponent must outbid them by to win.

| Opening Bid | Outbid Requirement |
|---|---|
| 1 to [X] | Standard — any raise wins |
| [X+1] to [Y] | Opponent must outbid by at least [a] health |
| [Y+1] and above | Opponent must outbid by at least [b] health (b > a) |

**Example (values placeholder):**
- Open at 1–4: normal auction, any raise wins
- Open at 5–9: opponent must raise by at least 3 to beat you
- Open at 10+: opponent must raise by at least 5 to beat you

**What this does:** Rewards bold initiators. A high open bid is not just expensive — it's protected. Opponents can't snipe with a +1; they must commit to a meaningful jump.

**Co-creator concern:** Three tiers is a lot of mental math mid-game with health already on the line. The thresholds also need to be felt, not just known — if [X] is arbitrary, it won't feel intuitive. This is worth designing *after* you know your health range and average card value. The brackets should feel natural relative to the economy, not imposed on top of it.

**Status:** TBD — needs playtesting context before numbers can be set.

---

## Variant B: Initiator's Right of Refusal *(Alternative — for comparison)*

A simpler model: the initiator gets **one right of refusal** at the end of the auction.

- The auction proceeds normally (ascending, clockwise)
- When the auction ends (all others have passed), the **initiator may match the winning bid** and take the card instead
- If the initiator declines or cannot afford to match, the last bidder wins as normal
- The initiator does **not** get this right if they are also the last remaining bidder

**What this does:** The initiator becomes a guaranteed participant in the endgame of their own auction. Even if sniped by a high bid, they can respond. The sniper must always bid high enough that the initiator *can't* or *won't* match.

**Upside:** Simple rule, one sentence. Creates interesting psychology — bidders must account for the initiator's health total when deciding their final bid.

**Downside:** Makes initiating very powerful for high-health players. A wealthy soul can just match any bid. Might punish low-health players from ever initiating.

---

## Variant C: Initiator's Discount *(Minimal Intervention)*

The simplest possible fix: the initiator pays **1 less health** than the winning bid.

- Auction resolves normally
- If the initiator wins, they pay [winning bid - 1] instead of the full amount
- If someone else wins, they pay the full amount

**What this does:** Makes initiating statistically cheaper. Doesn't add any rules, just a modifier.

**Upside:** Zero cognitive overhead. Works with any auction result.

**Downside:** The discount is small and may not feel meaningful on large bids. Doesn't solve the sniping-at-1 problem.

---

## Ruling (Designer Notes)

> Currently unresolved — all three variants are valid directions. **Variant A** is the most flavourful and creates the most interesting pre-auction decisions; **Variant B** is the most elegant and creates end-of-auction drama; **Variant C** is the safest starting point for playtesting.
>
> **Recommendation:** Start with Variant C in early playtesting (zero friction), and evaluate whether initiating feels undervalued. If yes, move to Variant B before attempting the complexity of Variant A.

---

## Alternative Ruleset System

The initiator mechanic is also the seed of a broader **Alternative Ruleset / Variant Module** system — optional rules that player groups can adopt or ignore.

This could expand to cover:
- Auction variants (see above)
- Team mode modifications
- Hard mode / casual mode health adjustments
- Specific card interaction clarifications for competitive vs. casual play

*See [[Future Considerations]] — Alternative Ruleset System (to be expanded)*
