# Changelog

Public releases of DeepCrawlerForge. Each entry is written for players. The development release notes are more detailed and stay in the development workspace.

0.205.0 is the first public release. The entries below it describe earlier development previews that were not published.

<!-- Release sessions: add the new entry at the top. The heading MUST contain the development
     release id (e.g. Dev95RG-Candidate176); the packager refuses a final build otherwise. -->

## 0.205.0 — Dev95SH-Candidate205 (preview)
- Fights follow the original's rules more closely:
  - arrows, thrown items and spells hit or miss as the original rolls them;
  - multi-class characters no longer always hit;
  - clerics and paladins holding a holy symbol turn undead automatically, as in the original;
  - when a monster hits the party, the game pauses for a moment, as the original does (Enhanced has a bug fix that removes the pause; it is on by default).
- The first time you take certain stairs down, the game asks for a word from the manual, as the original does. Enhanced can enter it for you (off by default).
- Wandering monsters come back on the levels where the original brings them back, at the same moments.
- When the whole party has fallen, the game is over, as in the original, with a button to rewind. Enhanced also ends the game when no one is left conscious (a bug fix, on by default).
- The bug-fix choices are part of your game: a saved game or timeline plays back the same whatever your current settings.
- Below the screen (Enhanced): which levels' special quests you have finished, and how much of each level you have explored.
- The campaign runner:
  - can be told to play to the start of a level (walking back to it if you are past it) or to the end of the game;
  - stops at once when you take over;
  - avoids fights it cannot win, puts on armour and shields it finds, and does not rest next to monsters.
- The history menu lists the start of each level.
- The Enhanced menu at the start shows every option's full description: long lists are split into pages, and a long text continues with Tab or a click. The DeepCrawlerForge title after the studio intro stays on screen a little longer.
- The Enhanced menu has a new category, Extended content, for options that build on the original design. Its options (the cleric rests at story events; the drow patrol keeps the eggs it takes as a bribe, so they can be won back) and three new encounter bug fixes apply to the encounters of later levels (beyond this preview), which now follow the original more closely.
- Because the fight rules changed, the certified timeline is rebuilt from the start of the game. This preview's certified timeline runs from Level 1, turn 0, to the Level 4 arrival (turn 6348) and replays exactly from its start. This preview plays through the end of Level 3.
- The single simulation clock is unchanged.

## 0.202.0 — Dev95SG-Candidate202 (preview)
- Two things the original game does in the background every moment now happen here too:
  - about every second and a half, every monster on the level gets a small random change to how it is drawn;
  - on the first levels, distant dungeon sounds play near the party at random intervals.
  Both use the game's dice, so every later roll now follows the original exactly. Every value is read from your copy of the game.
- The campaign runner:
  - casts protection and attack spells only when a fight is dangerous;
  - shows the spellbook while it casts in live play;
  - no longer falls back and forth through the Level-2 pits;
  - tries levers when it is stuck;
  - waits instead of stepping into its own arrow;
  - stops pulling a lever back and forth while holding an item.
  - no longer walks back and forth between a lever and a far corridor on Level 2, and finds its way out of the pit pocket there;
  - waits for a monster to clear the way, or walks up and fights it, instead of giving up;
  - finishes Level 2 instead of wandering it for thousands of turns: teleport squares no longer count as unexplored, it understands the elevator (press the button twice), and it no longer shuts itself in with door switches;
  - puts arrows into the quiver, and no longer prints a burst of bogus "taken" messages;
  - highlights the spell it is casting, and keeps its eye icon visible while the spellbook is open.
- The restored-scroll options no longer tell where the scroll is hidden.
  - It also plans about three times faster, so live play no longer slows down near the end of Level 1.
- Because the dice now follow the original more closely, the certified timeline is rebuilt again from Level 2. This preview's certified timeline runs from Level 2, turn 1121, to turn 2121 and replays exactly from its start.
- The single simulation clock is unchanged.

## 0.201.0 — Dev95SF-Candidate201 (preview)
- Monster timing now matches the original game to the tick, also while arrows and thrown items are in the air:
  - a monster acts only once its moment has passed, not on it;
  - a flying item checks for a hit again whenever a monster or the party moves;
  - monsters and flying items take their turns in time order within each quarter second.
- A monster turning on the spot now makes its footstep sound, as in the original. The rattle you hear at the start of a new game is the kobolds nearby: the sound is loud when they are close and fades as they walk away.
- The campaign runner arms the back row with the party's bows and slings and shoots, opens doors deeper into a level, eats a ration when it still adds food, and leaves spare items next to stairs so they are easy to find again.
- Because monster timing changed, the certified timeline is being rebuilt from Level 2. This preview's certified timeline runs from Level 2, turn 1121, to turn 1179 and replays exactly from its start.
- The provenance notice now describes how the original program is used during development and at runtime.
- The single simulation clock is unchanged.

## 0.200.0 — Dev95SE-Candidate200 (preview)
- The campaign runner goes down the Level-3 stairs and reaches Level 4.
- Two details now match the original game:
  - moving the party wakes monsters the way the original does, also after stairs and teleporters;
  - a trap that places a monster finishes the rest of its work (on Level 4, walls change) in the same step.
- The runner keeps its distance from monsters whose touch poisons or paralyses when it has something to shoot, will not rest while someone is poisoned and nothing can cure it, and leaves an item on the Level-1 pressure plate so the door stays open.
- The engine no longer contains any byte pattern of the original program: everything it reads is found by decoding your copy of the game. The provenance notice is updated accordingly.
- The certified timeline continues to Level 4, turn 6151, and replays exactly from its start.
- The single simulation clock is unchanged.

## 0.199.0 — Dev95SD-Candidate199 (preview)
- The campaign runner goes down to Level 3 and completes its special quest. It places the four blue gems in the eye slots until the eyes turn purple, then takes all four back, and the level rewards the party.
- Three details now match the original game:
  - a level the party has never visited loads fresh from the game files, even when the save file holds an old copy of it;
  - the monster clean-up on a level counts the party's steps, not time;
  - a wall clicked with nothing on the mouse cursor sees an empty hand, not a character's weapon.
- The certified timeline continues to Level 3, turn 5936, and replays exactly from its start.
- The single simulation clock is unchanged.

## 0.198.0 — Dev95SC-Candidate198 (preview)
- Taking an item from a wall niche that has a script now runs that script, as in the original game.
- On Level 2 the campaign runner uses all four dagger carvings and completes the level's special quest. It also clears a doorway held by two skeletons, and it puts away an item it does not need before pulling a lever.
- The certified timeline continues to turn 3582. The stairs down to Level 3 are not reached yet.
- The engine now reads the original program by decoded instructions instead of byte patterns. Every value it reads is unchanged.
- The single simulation clock is unchanged.

## 0.196.0 — Dev95SA-Candidate196 (preview)
- The campaign runner now opens doors that take a moment to open, such as stuck doors that must be forced, and waits for them instead of giving up.
- On Level 2 the runner forces four stuck doors, takes the Silver Key from its niche and opens the second lock, and places daggers in three of the four dagger carvings. The certified timeline continues to turn 2065.
- Three details now match the original game:
  - some stuck doors could not be clicked;
  - spinners turned the party to a fixed direction instead of turning it relative to its facing;
  - an arrow put into a non-empty quiver did not become the first one.
- The single simulation clock is unchanged.

## 0.195.0 — Dev95RZ-Candidate195 (preview)
- Horizon stops at a certified Level-2 regional dead end instead of cycling through pits and resting without progress.
- The certified timeline continues to turn 1553. The dagger-sensitive wall route remains under investigation.
- Game rules and the single simulation clock are unchanged.

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
