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

> Ronove's job is to harvest souls of decrepit humans, meaning their guardian angel's would be weaker than those of non-decrepit humans with stronger will. So Ronove should act surprised when he actually senses danger from the guardian angel. Ronove will have a life siphon power, where every few turns he take's the player's life and adds a portion

---

## Appearance (Sprite Reference)

- Form: [Canonical Goetic appearance]
- Tone: [Feeling the sprite should convey]
- Key visual details: [Most important elements to capture]
- Size: [Standard enemy / gate demon larger variant]

**Animation states needed:**
- [ ] Idle
- [ ] Attack
- [ ] Hurt
- [ ] Death

---

## Battle Mechanic

**[Mechanic Name]**

[Describe the mechanic — what it does, when it triggers, how long it lasts.]

- [Mechanical details]
- [Duration and stacking rules]
- [Difficulty note]

**AI Behaviour:**
- [What does this enemy do on its turns?]
- [Any conditional logic?]

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
