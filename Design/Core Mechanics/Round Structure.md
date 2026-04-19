# Round Structure

> Each round is a small death and a small resurrection. Do not waste it.

## Overview

A round in Altar of Life has three phases, in strict order:

```
DRAW PHASE  →  ACQUISITION PHASE  →  ACTION PHASE
```

---

## Phase 1: Draw Phase

*"Shed what no longer serves you. Take what the threshold offers."*

Players refine their hands and draw mana before anything else.

### Steps:

1. **Discard** — Players may discard any number of cards from their hand that they do not want. There is no penalty for discarding; this is how you cycle toward what you need.
2. **Draw to 7** — Players draw cards until their hand reaches **7 cards** (the hand limit).
3. **Mana Draw** — Players draw mana tokens blind from the mana deck.

### Notes:
- The hand limit of 7 is the target at the *start* of the round. Cards played during the Action Phase bring this below 7; you will refill next Draw Phase.
- Mana draw count and the mana hand cap are TBD (see [[Mana System]]).
- **Decks are shared.** There are three communal decks all players draw from: the **Mana Deck**, the **Souls & Rites Deck**, and the **Relics Deck**.

---

## Phase 2: Acquisition Phase

*"The Altar presents. You decide the cost."*

Players may acquire new cards during this phase. There are two separate acquisition tracks:

### Track A: Auction (Souls & Rites)
A set of cards is revealed from the deck into the market zone. Players participate in an **ascending clockwise auction** for each card, bidding health. The winner permanently loses that much health and adds the card to their hand.

- See [[Bidding System]] for full auction mechanics
- See [[Auction Initiator Variants]] for proposed rule variants on initiator advantage

### Track B: Direct Purchase (Relics)
Relics are not auctioned. They are available at a **fixed health cost** and may be purchased by any player during the Acquisition Phase — first come, first served, or in turn order (TBD).

- Players may buy a Relic **instead of** participating in the auction, or possibly **in addition to** it (TBD)
- Fixed pricing removes social conflict from Relic acquisition; their power comes from planning, not bidding

### Skipping
A player may skip the Acquisition Phase entirely and preserve their health. This is a valid strategic choice — especially for players with strong hands or critically low health.

### ⚠️ Designer Note — Timing of Health Loss
Health spent in the Acquisition Phase is **permanently lost before the Action Phase begins**. This means:
- You may overbid and die before playing a single card this round
- You are committing future resources based on what you *intend* to do in the Action Phase — not what you've already done
- This is intentional. It creates dramatic tension and meaningful commitment.

---

## Phase 3: Action Phase

*"Now spend what you have."*

Players take turns performing actions using their hand of cards and mana.

### Turn Order
Clockwise from the round's starting player (rotates each round — TBD how starting player is determined).

### Actions per Turn
On your turn, you may:
- **Play a Soul** — pay its mana cost, place it on your field
- **Cast a Rite** — pay its mana cost, resolve its effect, discard it
- **Activate a Relic** — trigger an equipped Relic's activated ability (if it has one)
- **Attack** — direct a Soul to attack an opponent's Soul or the opponent directly
- **Pass** — take no action this turn

### End of Action Phase
- Unused mana above the hand cap is discarded (see [[Mana System]])
- "End of round" triggered effects resolve
- Play passes to the Draw Phase of the next round

---

## Round Tracker (Dataview)

For playtesting notes — track observations per round:

```dataview
TABLE round AS "Round", notes AS "Notes", date AS "Date"
FROM "Playtesting"
WHERE round != null
SORT date DESC
```

---

## Open Questions

- How is the starting player determined and rotated?
- How many cards are revealed in the market zone each Acquisition Phase?
- Can a player both auction and buy a Relic in the same Acquisition Phase?
- Do unsold auctioned cards carry over to the next round or get discarded?
- When do "beginning of round" vs "end of round" triggered effects resolve exactly?
