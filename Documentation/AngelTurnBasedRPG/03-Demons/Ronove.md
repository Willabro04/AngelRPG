# Ronove

#demon #tier-1 #gate-demon #tentative

---

## Overview

[One or two sentences on this demon's role in the game.]

**Goetic Rank:** Marquis
**Legions Commanded:** 19
**Tier:** 1
**Gate Role:** Angel → Archangel
**Appears In:** Sphere 1

---

## Source Material

From the *Ars Goetia*:

[Paste or paraphrase the original Goetia description here.]

> [Your design note — why does their lore connect to their gate role or battle mechanic?]

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
