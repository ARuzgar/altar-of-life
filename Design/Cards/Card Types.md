# Card Types

> Three kinds of power wait at the Altar. Choose carefully — everything you claim costs something.

## Overview

There are three card types in Altar of Life. Each has a different **acquisition method**, a different **lore identity**, and a different **mechanical role**.

| Type | Sub-type | Acquired Via | Role | Lore Identity |
|---|---|---|---|---|
| **Souls** | — | Auction | Persistent field presence | Spirits of the previously dead |
| **Rites** | — | Auction | One-time or triggered effects | Ancient words, prayers, curses |
| **Remnants** | Relic | Direct purchase | Passive / equipped — found objects | Objects of power left at the Altar |
| **Remnants** | Charm | Direct purchase | Passive / equipped — personal items | Things the dead carried from their lives |

---

## Souls

*"They were here before you. They will serve you, for now."*

**Lore:** Souls are entities — fragments of those who came before, echoes of the dead who passed through the Altar and left something behind. To acquire a Soul is to make a bargain with it. To lose one is not necessarily to lose it forever.

**Mechanics:**
- Remain in play on the field until destroyed
- Cost mana to summon (play from hand to field) after being acquired at auction
- Can attack, defend, or trigger ongoing effects
- Some Souls may have health-drain costs to sustain

### Soul Death States

Souls have two distinct states after leaving the field:

| State | Name | Location | Can Return? |
|---|---|---|---|
| Destroyed but not gone | **Dead** | Liminal Zone | Yes — controller pays mana to re-summon |
| Permanently removed | **Forgotten** | Void / Purgatory / Chaos (TBD) | No — extinguished from the game |

What causes a Soul to move from Dead → Forgotten is TBD. Candidates:
- A specific card effect ("Condemn", "Erase", "Cast into the Void")
- Dying a second time while already in the Liminal Zone
- A player-triggered sacrifice

*See [[Notes & Ideas — Death and Forgetting Terminology]] for full exploration.*

**Open questions:**
- Do Souls have attack/defense stats, or effect-based power?
- Can Souls be sacrificed intentionally by their controller for effects?
- Are there named legendary Souls with unique lore?

---

## Rites

*"The old words still carry weight in this place."*

**⚔️ Name TBD — current candidates: Rites / Calls**
> Both are viable. "Rites" = ceremonial, altar-coded. "Calls" = raw, summoning-coded. Decide during playtesting or lore development.

**Lore:** Rites are invocations — prayers to things older than the Altar, curses inherited from the living world, calls sent into the void that something always answers.

**Mechanics:**
- Played directly from hand, consumed on use (unless stated otherwise)
- Cost mana to cast
- Effects are immediate or triggered
- Some Rites may cost health instead of (or in addition to) mana

---

## Remnants

*"What remains of a life is never nothing."*

**Confirmed:** Remnants is the card type. **Relics** and **Charms** are its two sub-types.

### Relics *(sub-type)*

*"Someone left this here. You're not sure you should pick it up."*

**Lore:** Objects of power that pre-exist the current players — artifacts left by those who passed through the Altar before, or things woven into the threshold itself. Impersonal, weighty, arcane.

**Mechanics:**
- Purchased directly at a fixed health cost
- Persist in play (equipped to the player or in a relic zone)
- Provide passive bonuses, ongoing effects, or activated abilities
- May have maintenance costs (health or mana per round)
- May be cursed — power with a passive drawback

### Charms *(sub-type)*

*"You carried it with you. You don't know why. You do know why."*

**Lore:** Personal objects — things a soul brought from their living life. A locket. A letter. A child's shoe. A knife. Objects that remember who you were and why you refused to stay dead.

**Mechanics:**
- Purchased directly at a fixed health cost (same acquisition as Relics)
- Persist in play — personal, equipped to the player
- May interact with the player's soul identity or backstory
- Foundation for the Starting Charm optional system — *see [[Starting Charms & Merit-Flaw System]]*

---

## Card Index (Dataview)

All individual card files should use the following frontmatter format:

```yaml
---
card-type: Soul              # Soul / Rite / Remnant
remnant-sub-type: Charm      # Relic / Charm (only if card-type is Remnant)
mana-type: Shadow            # Shadow / Flame / Verdant / Aether / etc. (TBD)
mana-cost: 3
health-cost: 0               # For Remnants (purchase cost) or drain effects
rarity: Common               # Common / Rare / Legendary
status: concept              # concept / in-development / playtested / final
tags: [card, soul]
---
```

### All Cards by Type

```dataview
TABLE card-type AS "Type", remnant-sub-type AS "Sub-type", mana-type AS "Mana", mana-cost AS "Cost", rarity AS "Rarity", status AS "Status"
FROM "Design/Cards"
WHERE card-type != null
SORT card-type ASC, rarity DESC
```

### Souls

```dataview
TABLE mana-type AS "Mana", mana-cost AS "Cost", rarity AS "Rarity", status AS "Status"
FROM "Design/Cards"
WHERE card-type = "Soul"
SORT rarity DESC
```

### Rites

```dataview
TABLE mana-type AS "Mana", mana-cost AS "Cost", rarity AS "Rarity", status AS "Status"
FROM "Design/Cards"
WHERE card-type = "Rite"
SORT rarity DESC
```

### Remnants — All

```dataview
TABLE remnant-sub-type AS "Sub-type", health-cost AS "Health Cost", rarity AS "Rarity", status AS "Status"
FROM "Design/Cards"
WHERE card-type = "Remnant"
SORT remnant-sub-type ASC, rarity DESC
```

### Relics

```dataview
TABLE health-cost AS "Health Cost", rarity AS "Rarity", status AS "Status"
FROM "Design/Cards"
WHERE card-type = "Remnant" AND remnant-sub-type = "Relic"
SORT rarity DESC
```

### Charms

```dataview
TABLE health-cost AS "Health Cost", rarity AS "Rarity", status AS "Status"
FROM "Design/Cards"
WHERE card-type = "Remnant" AND remnant-sub-type = "Charm"
SORT rarity DESC
```

### Cards In Development

```dataview
TABLE card-type AS "Type", remnant-sub-type AS "Sub-type", status AS "Status"
FROM "Design/Cards"
WHERE status = "in-development" OR status = "concept"
SORT card-type ASC
```
