# Bidding System

> The Altar demands payment. Name your price — but so will everyone else.

## Overview

Cards are not dealt, drawn, or bought at fixed cost. They are **auctioned**. Players bid their health in an ascending clockwise auction to acquire the cards they want. Every bid is a permanent health sacrifice.

This is the primary intersection of the [[Health System]] and the card economy.

---

## Auction Flow

### 1. Card Reveal
A set of cards is revealed from the main deck and placed in the **market zone** (exact number TBD — likely 3–5 cards per auction round). These are the cards available for bidding this round.

### 2. Ascending Clockwise Auction
Cards are auctioned one at a time (or in a defined order TBD):

- The player to the left of the active dealer opens bidding
- Play proceeds **clockwise**
- Each player must either **raise the bid** or **pass**
- Once a player passes, they are out of that card's auction
- The last remaining bidder wins the card and **loses that much health permanently**
- Minimum opening bid: TBD (likely 1 HP)

### 3. Next Card
After a card is won (or if all players pass on it), the next card in the market is auctioned.

### 4. Passed Cards
If all players pass on a card without a bid, the card is either discarded or held over to the next round (TBD).

---

## Strategic Dynamics

- **Position matters** — going first gives initiative but also forces your hand early; going last lets you see others commit
- **Bluffing** — bidding high on a card you don't need to drain an opponent's health is a valid strategy
- **Health visibility** — players' current health totals should be visible, creating informed pressure (TBD: exact visibility rules)
- **Low-health players** are dangerous bidders — they have little to lose and may force expensive wins

---

## Design Notes

- The auction should feel social and tense — player interaction is the point
- Consider whether all auctions happen before the action phase, or interleaved
- Consider a "reserve" rule: a player may set a silent max before the round to avoid emotional overbidding (analog mechanic for tabletop, automated in video game)
- Passing should never feel obviously correct — cards should be desirable enough that passing has real cost

---

## Open Questions

- How many cards are revealed per auction round?
- Do unsold cards carry over, or are they discarded?
- Is there a minimum bid per card, or does the auction always start from 1?
- Can players buy multiple cards per auction round, or just one?
