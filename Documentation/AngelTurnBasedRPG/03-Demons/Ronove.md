# Ronove

#demon #tier-1 #gate-demon #tentative

---

## Overview

Used as the first major fight in the game within [[Sphere 1]]. Ronove tries to harvest the player's soul before realizing the guardian angel is there and is forced to fight.

**Goetic Rank:** Marquis
**Legions Commanded:** 19
**Tier:** 1
**Gate Role:** Angel → Archangel
**Appears In:** Sphere 1

---

## Source Material

From the *Ars Goetia*:

In [demonology](https://en.wikipedia.org/wiki/Demonology "Demonology"), **Ronove** is a Marquis and Great Earl of [Hell](https://en.wikipedia.org/wiki/Hell "Hell"), commanding nineteen[[1]](https://en.wikipedia.org/wiki/Ronove#cite_note-1) legions of [demons](https://en.wikipedia.org/wiki/Demon "Demon"). He teaches art, [rhetoric](https://en.wikipedia.org/wiki/Rhetoric "Rhetoric"), languages, and gives good and loyal servants the favour of friends and foes.

He is depicted as a monster holding a staff, without detailing his appearance. He is also described as taker of old souls; often coming to earth to harvest souls of decrepit humans and animals near death.

> Ronove's job is to harvest souls of decrepit humans, meaning their guardian angel's would be weaker than those of non-decrepit humans with stronger will. So Ronove should act surprised when he actually senses danger from the guardian angel. Ronove will have a life siphon power, where every few turns he take's the player's life and adds a portion of it to his own, due to him harvesting souls in his lore.

---

## Appearance (Sprite Reference)

- Form: A monster holding a staff
- Tone: Slight fear due to his unique appearance, yet Ronove should also look fearful, yet maintain a smug demeanor.
- Key visual details: The staff, as it is his main weapon, and his grin due to being cocky, yet afraid.
- Size: Medium sized (between a normal enemy and the rest of the gate demons).

**Animation states needed:**
- [ ] Idle
- [ ] Attack
- [ ] Hurt
- [ ] Death

---

## Battle Mechanic

Life Siphon

Ronove attacks the player, any life taken from the player will be added to Ronove (health added will be 25% of the damage done to player).

- 25% of the damage done to the player will be added to Ronove's life.
- Only one turn, single move.
- Not as difficult to manage due to Ronove being the first gate demon.

**AI Behaviour:**
- Attack -> Attack -> Life Siphon (when Ronove health is below 50%)
- Only start using Life Siphon if Ronove's health is below 50%

---

## Gate Demon Behaviour

- Enters with name card: *"Ronove — Marquis of Hell, 19 Legions"*
- Outlined in light, gate demon entry sting plays
- Defeating sets the `gate_defeated` flag for the relevant ascension
- Refusal dialogue fires if player attempts to ascend before defeating this demon


## Stat Block

| HP | ATK | DEF | SPD | MAG | MANA | Light Drop |
|----|-----|-----|-----|-----|------|------------|
| [value] | [value] | [value] | [value] | [value] | [value] | [value] |

---

## Elemental Weakness

**Weak to:** [Element — see [[Magic System]]]
[One sentence on why this fits their lore.]

---

## Programming Checklist

- [ ] Create `obj_ronove` in GMS2
- [ ] Assign stat block
- [ ] Implement battle mechanic
- [ ] Set elemental weakness flag
- [ ] Set `is_gate_demon = true`
- [ ] Hook into gate demon spawn system
- [ ] Trigger gate_defeated flag on death
- [ ] Add name card entry event

---

## Related Notes

- [[Demon Roster Overview]]
- [[Combat System]]
- [[Magic System]]
