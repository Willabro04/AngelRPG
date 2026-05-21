# Divine Light System

#core #system #decided

---

## What It Is

Divine Light is the single progression resource of the game. It accumulates through combat, drives passive stat growth, and is spent to trigger ascension. There is no XP, no gold, no secondary currency. Divine Light does everything.

---

## Accumulation

- Fills passively as the player defeats enemies in battles
- Each enemy type drops a set amount of Light on death
- The bar **never resets between battles on the same floor** — it carries across the entire Sphere
- The bar **resets to zero on death** — even if gate demon defeats are remembered, the Light bar starts empty on a retry
- The bar **resets to zero on ascension** — growth begins fresh for the new rank

**Light drop values by tier:**

| Enemy Tier | Light Dropped |
|------------|--------------|
| Tier 1 | [amount] |
| Tier 2 | [amount] |
| Tier 3 | [amount] |
| Boss | [amount — or zero, TBD] |

> Target pacing: the player should arrive at the gate demon encounter with roughly 60–80% of the required Light. Two or three more clean battles should fill the bar. This keeps the gate demon defeat and the full bar converging near the same moment.

---

## Death and Light Loss

When the player dies and retries from the Sphere checkpoint:

- **Divine Light bar resets to zero** — all accumulated Light is lost
- **Gate demon defeats are remembered** — a defeated gate demon does not need to be fought again on the retry
- **Ascension rank is unchanged** — the player retains their current rank and all upgrades

This means a player who dies with a nearly full bar must refill it from scratch, but does not lose gate demon progress. The risk of pushing a difficult fight is losing your accumulated Light, not losing your gate progress.

---

## Passive Stat Growth

As the bar fills, the angel's base stats increase slightly. This is not the primary power source — upgrades are — but it makes filling the bar feel rewarding throughout rather than just at the end.

**Growth per milestone, per rank:**

| Milestone | ATK | HP | MAG | MANA |
|-----------|-----|----|-----|------|
| 25% | +1 ATK | +2 max HP | +1 MAG | +2 MANA |
| 50% | +1 ATK | +2 max HP | +1 MAG | +2 MANA |
| 75% | +1 ATK | +2 max HP | +1 MAG | +2 MANA |
| 100% | +1 ATK | +2 max HP | +1 MAG | +2 MANA |
| **Total** | **+4 ATK** | **+8 max HP** | **+4 MAG** | **+8 MANA** |

- Growth is **capped at 100%** — no overflow into the next rank's bar
- Stats reset to the **new rank's base values** on ascension — growth begins again from zero
- The cumulative effect across all 9 ranks is meaningful but never dominant over upgrade choices

---

## Ascension Cost

Each rank requires a specific amount of Divine Light to ascend, in addition to the gate demon being defeated:

| Ascend To | Light Cost |
|-----------|-----------|
| Archangel | 50 |
| Principality | 100 |
| Power | 175 |
| Virtue | 275 |
| Dominion | 400 |
| Throne | 575 |
| Cherubim | 800 |
| Seraphim | 1100 |

> Costs scale to keep fill time roughly consistent across ranks despite higher tiers dropping more Light. Tune during balancing.

---

## The Ascension Trigger

Both conditions must be true before the player can ascend:

1. **Gate demon for the current rank has been defeated**
2. **Divine Light bar is full**

When both are met, the ascension option becomes available on the player's next turn. A UI indicator signals this state.

If the player attempts to ascend before the gate demon is defeated, a **refusal dialogue** fires — a unique line per rank hinting at the specific demon without naming them. See each angel rank file for the line.

If the bar is not yet full but the gate demon is defeated, no dialogue fires — the bar communicates that condition visually on its own.

---

## Visual Design Notes

- The bar should feel **sacred rather than gamey** — consider a candle, halo ring, or radiance meter aesthetic rather than a standard HP bar
- Four milestone notches at 25%, 50%, 75%, and 100% marked subtly on the bar
- A **pulse or glow on the angel sprite** fires at each milestone — tied to the stat growth chime in FL Studio
- The bar's glow intensifies as it approaches full

---

## Related Notes

- [[Core Loop]] — where Divine Light sits in the overall loop
- [[Combat System]] — how enemies drop Light during battle and death/checkpoint rules
- [[Magic System]] — MANA growth in context
- [[Angel Ranks Overview]] — Light costs per rank in context
- [[NG+ System]] — Light does not carry between runs, resets on ascension as normal
