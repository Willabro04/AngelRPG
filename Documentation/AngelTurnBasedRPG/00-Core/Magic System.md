# Magic System

#core #system #tentative

---

## Overview

Magic is the secondary combat system unlocked through ascension upgrades. The Angel rank has no magic — the guardian fights purely physically at first. From Archangel onward, certain upgrade slots offer a magic attack instead of a stat boost or passive. Magic attacks cost MANA, deal damage using the MAG stat, and some enemies have elemental weaknesses that increase magic damage against them.

MANA restores passively — both during battle each turn and outside of battle during exploration. This creates a meaningful choice between spending MANA on magic attacks now versus conserving it for a bigger moment later in the floor.

---

## Damage Formula

```
magic damage = attacker MAG - defender DEF
minimum damage = 1
```

> DEF applies to both physical and magic attacks. There is no separate magic defense stat.
> Elemental weaknesses multiply damage — see Elemental Weaknesses section below.

---

## MANA

**What it is:** The resource spent to use magic attacks. Starts at 10 at Angel rank and grows with Divine Light milestones and upgrades.

**Passive restoration:**
- Restores a small amount each turn during battle
- Restores a small amount during exploration between battles
- Fully restores at each Sphere checkpoint (on entering a new floor)

**The tension this creates:** The player can lean on magic frequently if they accept arriving at a gate demon with lower MANA reserves, or play conservatively and bank MANA for a burst of magic attacks against a tougher fight. Upgrades that boost passive restoration shift this calculation.

**MANA costs per magic attack:** [TBD during balancing — set a flat cost per attack or tier-based cost]

---

## How Magic Is Learned

- **Angel rank:** No magic available. Physical combat only.
- **Archangel and above:** Each rank's upgrade screen may include one magic attack as one of the three options. Choosing it permanently unlocks that attack for the rest of the run.
- Magic upgrades carry into NG+ runs like all other upgrades.
- A player who never chooses magic upgrades will never have magic — it is opt-in, not automatic.

---

## Magic Attacks by Rank (Tentative)

One magic option per rank from Archangel onward. These are starting suggestions — finalize in each rank's upgrade file.

| Rank | Magic Upgrade Option | Element | Notes |
|------|---------------------|---------|-------|
| Archangel | [Weak fire attack] | Fire | First magic available — low cost, low damage, teaches the system |
| Principality | [TBD] | [TBD] | |
| Power | [TBD] | [TBD] | |
| Virtue | [Heal — restores HP] | Holy | Non-damaging — spend MANA to restore health instead |
| Dominion | [TBD] | [TBD] | |
| Throne | [TBD] | [TBD] | |
| Cherubim | [TBD] | [TBD] | |
| Seraphim | [TBD] | [TBD] | Highest tier — should feel appropriately overwhelming |

> Fill in TBD entries when writing each rank's upgrade file. Each magic attack should feel thematically tied to the angel's rank — a Throne attack should feel heavier and more authoritative than an Archangel attack.

---

## Elements

**Decided elements (tentative — expand or trim as needed):**

| Element | Description |
|---------|-------------|
| Fire | Burning, consuming — associated with lower Sphere ranks |
| Holy | Radiant, purifying — associated with mid Sphere ranks |
| [TBD] | [Third element — consider Storm, Dark, or Void for Sphere 3] |

> Decide the full element list before writing individual demon weakness entries. Every demon file will reference this table.

---

## Elemental Weaknesses

Some enemies take increased damage from specific elements. Weakness multiplies magic damage by [X] — exact multiplier TBD during balancing (1.5× or 2× are common starting points).

| Enemy | Weakness | Notes |
|-------|----------|-------|
| [Demon name] | [Element] | [Why this fits their lore] |

> Fill this table in as each demon file is written. Cross-reference with the source material — a demon associated with water might be weak to fire, a demon associated with deception might be weak to holy, and so on.

---

## Mana Restoration Upgrades

Some upgrades boost passive MANA restoration rather than offering a new magic attack. These are worth designing as alternatives at ranks where the magic attack option exists — a player who already has fire but wants more consistent magic access would choose restoration over a second element.

Examples of what restoration upgrades might look like:
- Passive restoration rate increased by [X] per turn
- Restoration triggers on physical hit as well as passively
- MANA restored on gate demon defeat

> Finalize specific restoration upgrades in the relevant rank upgrade files.

---

## Design Notes

Magic should feel like a layer on top of physical combat, not a replacement for it. A full-magic build and a full-physical build should both be viable — magic upgrades are powerful but so are the stat and passive options competing for the same slots. The MANA cost and passive restoration rate are the primary balancing levers here.

Heal (Virtue rank) deserves special attention during balancing — a magic heal is powerful enough that its MANA cost should feel significant, and enemies in Sphere 2 and 3 should be threatening enough that spending MANA on survival rather than damage feels like a real trade-off rather than an obvious choice.

---

## Related Notes

- [[Combat System]] — damage formula context, DEF applies to magic
- [[Divine Light System]] — MANA growth at milestones
- [[Upgrades Overview]] — magic upgrades in the full upgrade list
- [[Archangel Upgrades]] through [[Seraphim Upgrades]] — individual magic upgrade entries
- [[Demon Roster Overview]] — enemy elemental weaknesses
