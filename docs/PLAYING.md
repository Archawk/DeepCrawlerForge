# Playing

## Authentic

Authentic presents the original 320×200 game screen with the original rules, timing and input model. Mouse and keyboard work as they did in the DOS game. There are no overlays, no automap and no helpers. Time runs live, as in the original: the world advances in 250 ms steps whether or not you act.

## Enhanced

Enhanced keeps the complete original screen and rules, and adds optional features on top. Each feature can be switched on or off in the Enhanced options:

| Option | What it does |
|---|---|
| Automap | Full automap and a small HUD map, built only from squares the party has actually visited. |
| Timeline scrubber | Step backwards and forwards through your game and branch from any earlier point. Every action is recorded deterministically. |
| Enemy hit points | Shows monster hit points. |
| Turn-based mode | The world waits for your action instead of running live. Toggle between live and turn-based at any time. |
| Burning Hands scroll | Restores content that exists in the game data but can't be reached in the original. |
| Restored ending | Continues after the original ending through a restored escape route. |
| Attack All | One command attacks with every ready party member. |
| Modern keyboard | W/S move forward and back, A/D strafe, Q/E turn, plus keyboard focus for inventory and spells. |
| Smart pickup | Friendlier item pickup and hand-off. |
| Mobile input | Shows the touch input toggle on small screens. |

Live mode in Enhanced is the same turn system as turn-based mode, with turns advanced automatically every 250 ms. Switching between the two never changes the outcome of the same inputs.

## Fullscreen

Use the ⛶ button in the game bar. The game scales to fit the screen, keeps the 8:5 aspect ratio, and draws pixels sharply.

## Saving

Progress is kept in your browser's local storage (see [PRIVACY-AND-STORAGE.md](PRIVACY-AND-STORAGE.md)). Where the in-game menus offer it, games can be exported and imported. In the public build, imports are limited to the playable level range.

## The preview limit

Each public build is playable up to its certification frontier. If you reach a staircase or other passage that leads beyond it, the message *"The way on is sealed in this preview."* appears and the party stays where it is. Nothing is lost, and later releases open more of the dungeon. See [CERTIFICATION.md](CERTIFICATION.md).
