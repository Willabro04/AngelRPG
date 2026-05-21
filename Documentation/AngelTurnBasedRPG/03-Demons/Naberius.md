# Naberius

#demon #tier-1 #roaming #tentative

---

## Overview

[One or two sentences on this demon's role in the game.]

**Goetic Rank:** Marquis
**Legions Commanded:** 19
**Tier:** 1
**Gate Role:** Roaming — no gate role
**Appears In:** Sphere all

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

## Roaming Encounter

Naberius has no gate role. Appears randomly across all three floors in any area.
Does not block ascension. Can appear multiple times in a single run.


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

- [ ] Create `obj_naberius` in GMS2
- [ ] Assign stat block
- [ ] Implement battle mechanic
- [ ] Set elemental weakness flag
- [ ] Set `is_roaming = true`
- [ ] Hook into random roaming encounter system



---

## Related Notes

- [[Demon Roster Overview]]
- [[Combat System]]
- [[Magic System]]
