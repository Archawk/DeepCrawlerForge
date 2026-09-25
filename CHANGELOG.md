# Changelog

Public releases of DeepCrawlerForge. Each entry is written for players. The development release notes are more detailed and stay in the development workspace.

<!-- Release sessions: add the new entry at the top. The heading MUST contain the development
     release id (e.g. Dev95RG-Candidate176); the packager refuses a final build otherwise. -->

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
