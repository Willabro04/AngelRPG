# NG+ System

#core #system #decided

---

## Overview

After completing a run, the player can begin New Game Plus. The core loop — exploration, battles, Divine Light, gate demons, ascension — remains identical. What changes is the upgrade screen: previously chosen upgrades are locked, and only the unchosen options are available. This continues across three runs until all 27 upgrades have been collected, at which point [[Asmodai]] is unlocked as the secret true final boss.

---

## The Three Runs

| Run | Upgrades Available | Asmodai |
|-----|--------------------|---------|
| Run 1 | All 3 options shown, choose any 1 | Not available |
| Run 2 (NG+) | 2 remaining options shown, choose 1 | Not available |
| Run 3 (NG++) | 1 remaining option shown, take it | Unlocks after Beleth if all 27 collected |

> The gate demon system, Divine Light costs, and floor structure are identical across all three runs. The ritual of ascension never becomes automatic.

---

## What Carries Between Runs

| Element | Carries? | Notes |
|---------|----------|-------|
| Upgrade choices (which were picked) | ✓ Yes | Saved to file — locked in subsequent runs |
| Stats | ✗ No | Start fresh each run at Angel base stats |
| Divine Light | ✗ No | Bar starts empty |
| Gate demon defeat flags | ✗ No | Must defeat each gate demon again each run |
| Progression / rank | ✗ No | Start at Angel each run |
| MANA | ✗ No | Resets with stats |

---

## Save Structure

The save file records one thing: **which upgrade was chosen at each of the 9 ranks**, across runs.

```
save {
  run_number: 1 / 2 / 3
  rank_2_choice:  A / B / C
  rank_3_choice:  A / B / C
  rank_4_choice:  A / B / C
  rank_5_choice:  A / B / C
  rank_6_choice:  A / B / C
  rank_7_choice:  A / B / C
  rank_8_choice:  A / B / C
  rank_9_choice:  A / B / C
}
```

> Implement using GMS2's ini file system. Each rank choice is written to file immediately on selection so a crash or close does not lose progress.

---

## Upgrade Screen Behaviour Per Run

**Run 1:** All three upgrade cards displayed. Player chooses one. Chosen upgrade saved to file immediately.

**Run 2 (NG+):** The upgrade chosen in Run 1 is greyed out or hidden. The two remaining options are displayed. Player chooses one. Both choices now saved.

**Run 3 (NG++):** Only the single unchosen upgrade is displayed. Player confirms it. All three are now saved for that rank.

---

## How NG+ Feels

**Run 1:** Learning the loop, choosing upgrades that appeal most. Magic or physical, offensive or defensive — first impressions drive these choices.

**Run 2 (NG+):** Starts with Run 1's upgrades already active. Stronger from the beginning but the game rubber-bands in difficulty toward the mid-to-late Spheres. Upgrade choices are more deliberate — filling in gaps from Run 1.

**Run 3 (NG++):** All previous upgrades active from the start. Should feel fast and powerful in Sphere 1, increasingly tested through Sphere 2, and genuinely challenged by Sphere 3 with all 27 upgrades stacked. Asmodai waits at the end as the true measure of a complete run.

---

## Asmodai Unlock Condition

At the end of Run 3, after [[Beleth]] is defeated:

1. Check if all 27 upgrades have been collected across the three runs
2. If yes → trigger [[Asmodai]] encounter before credits roll
3. If no → credits roll normally

> This check should be redundant on a legitimate Run 3 — if the player reached the end of NG++ they will have all 27. Handle the edge case anyway.

---

## Visual Flags

- A subtle UI marker on the title screen or HUD indicates the current run number
- The title screen music on NG+ is a layered or subtly altered version of the main theme — signals that something has changed without being explicit
- Specific visual treatment TBD — crown, sigil, or glow on the angel or UI border

---

## Related Notes

- [[Core Loop]] — NG+ in the full loop context
- [[Upgrades Overview]] — the full 27 upgrade list
- [[Asmodai]] — the true final boss
- [[Combat System]] — what carries and what resets
- [[Magic System]] — magic upgrades carry between runs
