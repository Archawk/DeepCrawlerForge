# Changelog

Public releases of DeepCrawlerForge. Each entry is written for players. The development release notes are more detailed and stay in the development workspace.

<!-- Release sessions: add the new entry at the top. The heading MUST contain the development
     release id (e.g. Dev95RG-Candidate176); the packager refuses a final build otherwise. -->

## 0.194.0 — Dev95RY-Candidate194 (preview)
- The campaign runner's Level-2 key solution is now checked step by step against the original game running under emulation: the throw onto the pressure plate, the walk past the pit, and the key in the lock.
- Saves exported from DeepCrawlerForge now keep the current level's changes when loaded in the original game. Opened doors and closed pits no longer revert.
- Runner fix: right after opening a lock, it no longer lifts and puts back a lock pick endlessly.
- Game rules unchanged.

## 0.193.0 — Dev95RX-Candidate193 (preview)
- The campaign runner gets past the Level-2 lock: it keeps the pit shut with an item thrown onto the pressure plate, fetches the Silver Key from its niche and opens the locked door.
- The runner plans in a background worker, so the view stays smooth while it plays.
- Runner fixes: no casting during a rest, no endless stair walking when both levels are explored, climbing out of a pit's landing area by the ladder.
- Game rules unchanged.

## 0.192.0 — Dev95RW-Candidate192 (preview)

- Wands work: right-click a wand in a hand. Each use takes a charge; the Wand of Slivias pushes monsters back. As in the original, a wand's missile spells hit with the holder's level; the new Enhanced bug fix "Wand spells at the wand's level" (on by default) uses the wand's.
- Potions work, and identified items show their full original names ("Potion of Healing", "Wand of Lightning", "Staff +2"). As in the original the Potion of Speed does nothing; the new Enhanced bug fix "Potion of Speed works" (on by default) hastes the drinker.
- Cone of Cold hits the original's squares (one ahead, three at two, three at three).
- Distant sounds are heard within the same moment, as in the original; door and monster attack sounds use the original's volume at the party.
- Messages: "casts" uses the original spell names; a poisoned character shows "is poisoned!".

## 0.191.0 — Dev95RV-Candidate191 (preview)

- Fireball, Ice Storm and Flame Strike hit every monster in the square they land in, and no longer the squares around it, as in the original.
- Hold Person and Hold Monster try to hold every monster in the square they land in, as in the original.
- Monster steps and distant sounds are heard one sound late, as in the original. In Enhanced mode the new bug fix "Positional sounds on time" (on by default) plays each at once.

## 0.190.0 — Dev95RU-Candidate190 (preview)

- The intro plays its original music and its scene sound effects. The original intro uses its own sound bank, which DCF had not been playing.
- AdLib sound comes from the original sound driver found in your game files, played through a new OPL2 (AdLib chip) synthesizer. Checked against the original write by write.
- The main menu is silent, as in the original; the intro music no longer continues into it.

## 0.189.0 — Dev95RT-Candidate189 (preview)

- The Read Magic scroll now lies in the hidden Level 5 room, which holds four restored scrolls: Burning Hands, Stinking Cloud, Cloudkill and Read Magic.
- The hidden room's wall opens when any of those four is switched on (Enhanced mode, Restored content). With all four off it stays solid, as in the original.
- Knock stays on Level 2. Protection from Lightning has no scroll; clerics pray for it.

## 0.188.0 — Dev95RS-Candidate188 (preview)

- Spells are now matched to the original's spell records by what the records contain, not by their names. Every spell behaves exactly as before.
- Wands point to the right spells through the original's wand table (Frost casts Cone of Cold, Curing casts Cure Serious Wounds). Using wands is still to come.
- Restored spells in Enhanced mode (Restored content, one switch per spell): Knock, Protection from Lightning, Stinking Cloud, Cloudkill and Read Magic. The original never finished them; Authentic mode keeps them unfinished.
- Their scrolls: Read Magic on Level 1, Knock on Level 2, Stinking Cloud and Cloudkill in the hidden Level 5 room.
- The Burning Hands scroll can be found again (it was disappearing when the level was entered).

## 0.187.0 — Dev95RR-Candidate187 (preview)

- Starting a new party right after quitting to the main menu no longer stops with "unstubbed INT 21h/AH=41". A mouse move at the wrong moment could make the original pick its Load game row; your input now waits until the original has left its main menu.
- AUTOROLL appears once the portrait is chosen, together with the RE-ROLL / MODIFY buttons.
- The Horizon eye stays visible while an inventory is open.
- Horizon (the automatic explorer):
  - keeps the Spellbook and Holy Symbol in the casters' hands, so the Mage and the Cleric/Paladin can cast;
  - uses the least useful item (for example a Rock) to hold a floor plate, never a casting implement;
  - no longer opens and closes the same doors or presses do-nothing buttons over and over;
  - fights a monster it keeps circling next to;
  - heals badly wounded members, casts protection before a close fight and casts attack spells at monsters in line.
- Timed spells that run out now replay exactly as they were played.

## 0.186.0 — Dev95RQ-Candidate186 (preview)

- Clicking a plain wall no longer "forces" a door that is not there (a doorway could appear in the wall). Checked against the DOS original, which does nothing there.
- Horizon (the automatic explorer):
  - no longer freezes after casting at an enemy while its own spell is still in the air;
  - waits for a spell to finish before casting the next one;
  - fights a monster that blocks its way instead of stepping back and forth;
  - handles running out of food: no resting while starving, it ends the rest at the starving prompt.
- Horizon plans about twice as fast.
- Autosave writes only what changed since the last save.

## 0.185.0 — Dev95RP-Candidate185 (preview)

- Floor plates work as in the original: the door a plate opens closes again when you step off it, unless you leave an item on the plate.
- Clicking into an open doorway no longer counts as an attempt to break the door open.
- Horizon (the automatic explorer):
  - no longer gets stuck walking back into a pit or shuttling between two squares;
  - remembers the squares you already explored when you start it mid-game;
  - eats rations before the party starves;
  - puts arrows in the quiver and readies throwing weapons;
  - dismisses the "rested" summary before moving on;
  - leaves an item on a floor plate so the door it opens stays open.
- Arrows you pick up with the Enhanced quick pick-up go straight into the quiver.
- Autosave does less work on long games.

## 0.184.0 — Dev95RO-Candidate184 (preview)

- Character creation: Smart and Random parties are created in a few seconds and shown straight in the original party screen, where you can rename characters (or delete, replace and modify them as usual).
- Autoroll now sits beside the stats: pick the stat to maximise (or the total) and press AUTOROLL.
- The mouse is much smoother during character creation.
- Load Game uses the original menu look.
- Quitting to the main menu from Camp no longer leaves the timeline bar on screen.
- Horizon (the automatic explorer) casts spells, stops walking into its own thrown daggers and keeps its controls visible.
- Replays of long games now match what happened when you played.

## 0.183.0 — Dev95RN-Candidate183

- Doors: while a door opens, you see the monsters and items behind it through the opening, and through the gaps of a closed barred door, as the original draws them (checked pixel for pixel against the DOS original). Nothing can be hit or picked up through a door that is not open.
- Monsters keep the original game's timing, and the monster types that do so in the original now attack right after stepping next to you.
- Some creatures no longer take up a whole square, as in the original.
- Long games stay fast: the saved timeline is many times smaller and autosave no longer pauses the game.

## 0.182.0 — Dev95RM-Candidate182 — first public preview

- First public build. Play Authentic or Enhanced with your own *Eye of the Beholder* DOS files; nothing from the game is included.
- Playable to level 2. Level 1 is certified against the original game running in a DOS emulator; level 2 is still being certified (see `docs/CERTIFICATION.md`).
- The original intro, main menu, setup program and character creation run from your own game files and match the DOS version.
- Enhanced: Smart and Random parties get generated names you can edit; autoroll can be turned off in the Enhanced features menu.
- Armor Class follows the original game's calculation, checked against the DOS original.
- Monsters use the original game's own record fields: their Armor Class, to-hit number and hit points match the DOS original.
- Loading a saved position restores exactly what was saved.
- Game archives are read more flexibly (any folder depth, whole-folder zips), and missing files are listed.
- Touch controls for setup and character creation.
- An Archawk Games intro plays when the page opens. Click, tap or press a key to skip it; it is off when your system asks for reduced motion.
