# Mana System

> Mana is the blood of the world. You draw what fate gives you, and you spend it before it fades.

## Overview

Mana is the **activation resource** — used to play and trigger cards acquired through the [[Bidding System]]. Unlike health, mana replenishes each round, but what you draw is blind and what you don't spend is lost.

The mana system has two distinct categories: **Typed Mana** and **Generic Mana**.

---

## Typed Mana

Typed mana is tied to specific schools or elements of the game world (exact types TBD with lore, e.g. Fire, Shadow, Nature, Arcane, etc.).

- **Stable and reliable** — typed mana does exactly what it says
- **Required for school-specific cards** — powerful cards in a given school require their matching mana type
- **Encourages identity** — building around one or two types gives synergy and focus
- **Drawn from the blind mana deck** alongside generics — you don't control what you pull

### Design Intent
Typed mana rewards commitment. A player who builds a Fire deck wants to draw Fire mana. When they don't, they feel the chaos of the world working against them.

---

## Generic Mana

Generic mana is flexible but unstable. It can be used for any card cost, but it comes with conditions and riders drawn blind from the mana deck.

### Charged Generics
Each generic mana token has a **charge type** that modifies how it behaves when used:

| Charge Type | Effect |
|---|---|
| **Pure** | Standard generic mana, no rider. Use freely. |
| **Cracked** | Costs 1 health to use. Powerful but dangerous. |
| **Surge** | Grants +1 to the next action or ability it contributes to. |
| **Void** | Expires at the end of the phase it's drawn in — must be used immediately or lost. |
| *(more TBD)* | Additional charge types to be designed during card development |

### Design Intent
Generic mana feels like pulling something volatile out of the aether. Even a "free" resource can bite you. The charge variety means your mana hand is never boring — it's a mini puzzle each round.

---

## Convertible Mechanic

Players may **burn multiple generic mana tokens to forge one typed mana**:

- Spend **2–3 generics** → produce **1 typed mana** of a chosen school
- The exact conversion rate (2:1 or 3:1) is TBD via playtesting
- Charged generics (Cracked, Surge, Void) can be used in conversion — their riders do **not** carry over to the resulting typed mana
- This gives players a safety valve when typed draws are dry, but at an efficiency cost

### Design Intent
Conversion makes generic mana a genuine alternative path rather than a fallback junk pile. It also creates interesting decisions: do you convert now, or hold generics and hope for a better draw?

---

## Round Structure (Mana)

1. **Draw phase** — players draw mana tokens blind from the mana deck
2. **Action phase** — mana is spent to play/activate cards
3. **End of round cap** — any mana exceeding the hand cap is discarded

### Hand Cap
- Maximum mana held at end of round: TBD (suggested: 3–5 tokens)
- Unused mana above the cap is lost — **use it or lose it**
- Cap may be modified by certain cards or abilities

---

## Future Considerations

- **Valued Generics** — assigning numeric values (1, 2, 3) to generic tokens for variable power. Deferred until after playtesting baseline. *See [[Future Considerations]].*
- Mana deck composition (ratio of typed to generic, charge type frequency) TBD
- Possible mechanic: cards that let you peek at or manipulate the top of the mana deck
