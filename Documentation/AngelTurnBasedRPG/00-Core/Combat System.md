# Combat System

#core #system #decided

---

## Overview

Turn-based combat in a single room. The player controls one angel. Enemies spawn solo or in groups of 2–3 based on the current Sphere tier. Each turn the player and enemies act in SPD order. Combat ends when all enemies are defeated. Between battles, the player explores the current floor area, finds lore tablets, and progresses toward the next gate demon or Sphere boss.

---

## Turn Order

**Speed-based** — highest SPD stat acts first each turn. Ties broken by player priority.

---

## Player Stats

| Stat | Description |
|------|-------------|
| HP | Current and maximum health. Reaching 0 = game over. |
| ATK | Determines physical damage dealt. Modified by upgrades and Divine Light growth. |
| DEF | Reduces incoming damage — applies to both physical and magic attacks. |
| SPD | Determines turn order. Also affects Run success chance. |
| MAG | Determines magic damage dealt. Modified by upgrades and Divine Light growth. |
| MANA | How many times magic attacks can be used. Restores passively — see [[Magic System]]. |

**Base stats at Rank 1 (Angel):**

| HP | ATK | DEF | SPD | MAG | MANA |
|----|-----|-----|-----|-----|------|
| 50 | 15 | 5 | 10 | 5 | 10 |

> Stat growth from Divine Light adds +1 ATK, +2 max HP, +1 MAG, and +2 MANA per 25% milestone. See [[Divine Light System]].
> Upgrades modify these further. See [[Upgrades Overview]].

---

## Player Actions

| Action | Description |
|--------|-------------|
| Attack | Deal physical damage to one enemy. Damage = ATK − enemy DEF (minimum 1). |
| Magic | Use a magic attack tied to the current angel form. Damage = MAG − enemy DEF (minimum 1). Costs MANA. Not available at Angel rank — unlocked through upgrades from Archangel onward. See [[Magic System]]. |
| Defend | Reduce all incoming damage this turn by a flat amount or percentage. TBD during balancing. |
| Run | Attempt to flee the battle. Cannot be used against gate demons or Sphere bosses. See Run mechanic below. |

---

## Run Mechanic

- Success chance is based on the **relative SPD** of the player and the enemy — higher player SPD means better base escape chance
- Each **failed Run attempt increases the next attempt's success chance** by a flat amount — persistence eventually guarantees escape
- **Cannot be used against gate demons or Sphere bosses** — those encounters must be fought to completion or result in game over

---

## Enemy Stats

Each enemy type has its own stat block. See individual demon files for specifics.

| Stat | Description |
|------|-------------|
| HP | Defeated when reduced to 0. Drops Divine Light on death. |
| ATK | Physical damage dealt to player per attack. |
| DEF | Reduces damage from both player physical and magic attacks. |
| SPD | Determines turn order. |
| MAG | Magic damage dealt to player (if the enemy uses magic). |
| MANA | How many times the enemy can use magic attacks. |

**Stat ranges by tier (target values — tune during balancing):**

| Tier | HP Range | ATK Range | DEF Range |
|------|----------|-----------|-----------|
| Tier 1 | [low] | [low] | [low] |
| Tier 2 | [mid] | [mid] | [mid] |
| Tier 3 | [high] | [high] | [high] |
| Boss | [very high] | [high] | [mid-high] |

---

## Damage Formula

**Physical attack:**
```
damage = attacker ATK - defender DEF
minimum damage = 1
```

**Magic attack:**
```
damage = attacker MAG - defender DEF
minimum damage = 1
```

> DEF applies to both physical and magic damage. There is no separate MDEF stat.
> Elemental weaknesses modify the magic formula — a weakness multiplies damage by [X]. See [[Magic System]].
> Exceptions per upgrade (e.g. Smite ignores DEF, Fortify adds flat damage reduction) should each be documented here as they are implemented.

---

## Status Effects

| Effect | Description | Duration |
|--------|-------------|----------|
| Burn | Deals [X] damage at the start of the affected unit's turn | [X] turns |
| Poison | Deals stacking damage each turn — grows stronger over time | Until cured or end of battle |
| Silence | Locks out one player action option | 1–2 turns |
| Discord | Buffs enemy ATK while active — Andras mechanic | [X] turns |
| Fear | Reduces effectiveness of attacks or defense | [X] turns |
| Steal | Temporarily removes one player upgrade effect — Gaap mechanic | 2 turns |

> Status effects that last more than one turn need a visible duration counter in the UI.
> Burn and Poison durations are tentative — set during balancing.
> Fear's exact mechanical effect (ATK reduction, DEF reduction, or action restriction) is TBD.

---

## Spawn System

- Enemies spawn solo or in groups of 2–3 per encounter
- Exact group sizes TBD during balancing
- Composition escalates by Sphere tier:
  - Sphere 1: Tier 1 enemies only
  - Sphere 2: Tier 2 enemies, occasional Tier 1
  - Sphere 3: Tier 3 enemies, occasional Tier 2
- **Gate demons** appear at the end of their designated area within a floor — they block progression until defeated. See [[Core Loop]] for full floor structure.
- **Naberius** appears as a random roaming encounter across all three floors — see [[Naberius]]
- **Sphere bosses** appear at the end of each floor, blocking the entrance to the next Sphere — see [[Bael]], [[Paimon]], [[Beleth]]

---

## Checkpoints and Game Over

- Player HP reaching 0 → game over screen, run ends
- No mid-run saves within a floor
- **Each Sphere has its own checkpoint** — on entering a new floor, progress is saved and HP and MANA are fully restored
- On game over the player restarts from the last Sphere checkpoint
- Gate demon and Sphere boss defeats are **not individually checkpointed** — if the player dies after defeating Ronove but before defeating Andras, they restart from the Sphere 1 entrance

> This means the player must re-defeat earlier gate demons on a retry within the same Sphere. Consider whether gate demon defeats should be remembered within a Sphere attempt — a decision worth making during playtesting.

---

## Related Notes

- [[Core Loop]] — where combat sits in the overall loop
- [[Divine Light System]] — how enemies feed the resource
- [[Magic System]] — magic attacks, mana costs, and elemental weaknesses
- [[Upgrades Overview]] — how upgrades modify combat
- [[Demon Roster Overview]] — all enemies and their mechanics
- [[Bael]] / [[Paimon]] / [[Beleth]] / [[Asmodai]] — boss combat specifics
