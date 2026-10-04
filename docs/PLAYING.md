# Playing

## Authentic

Authentic presents the original 320×200 game screen with the original rules, timing and input model. Mouse and keyboard work as they did in the DOS game. There are no overlays, no automap and no helpers. Time runs live, as in the original: the world advances in 250 ms steps whether or not you act.

## Enhanced

Enhanced keeps the complete original screen and rules, and adds optional features on top. The Enhanced menu on the start screen groups them into five categories, and each option can be switched on or off separately. Every option has a full description in the menu (Tab, or a click on the text, shows the next page of a long one).

### Quality of life

| Option | What it does |
|---|---|
| Automap + autorun | Full automap and a small HUD map, built only from squares the party has visited. Click a known square to walk there; autorun stops at combat, input or anything new. |
| Timeline | Step backwards and forwards through your game and branch from any earlier point. Every action is recorded deterministically. |
| Enemy HP | Shows each visible monster's hit points. |
| Turn-based mode | The world waits for your action instead of running live. Space switches between live and turn-based at any time. |
| Attack All | One command (or Tab) attacks with every ready party member. |
| Modern keyboard | W/S forward and back, A/F strafe, Q/E turn, F1–F6 select characters, plus keys for inventory, spells and the automap. |
| Smart pickup | Shift+G puts the floor item into the first free pack slot of the selected character. |
| Status below the screen | Which levels' special quests are complete, and how much of each visited level the party has explored. |
| Character creation | Autoroll a chosen stat, and rename party members. |
| Smaller helpers | Effect timers on portraits, door auto-wait, thrown-item auto-pickup, buff refresh, a direct HP bars/numbers switch, the touch input switch, the manual word entered for you, and encounter notices. |

### Bug fixes

Corrections for bugs of the original game, for example hit points above 127, the ring that should stop hunger, the Potion of Speed, the moment the whole game freezes while a monster attack plays, and a party that lies unconscious for ever. Authentic mode always keeps the original behaviour. The choices are part of your game: a saved game or timeline plays back the same whatever your current settings.

### Restored content

Content that exists in the game but can't be reached or doesn't work in the original: the Burning Hands scroll, the unfinished Read Magic and Knock spells, the empty Stinking Cloud, Cloudkill and lightning-protection spells, and a restored ending with an escape route.

### Extended content

Options that build on the original design, such as encounters that remember what happened in them.

### Tools & automation

| Option | What it does |
|---|---|
| Campaign runner | Hand the game to the runner: it plays on (for example to the start of a level) and stops at once when you take over. Its moves are ordinary timeline actions, so they can be rewound like your own. |
| Campaign seed | Choose or reuse the seed of a deterministic campaign. |

Live mode in Enhanced is the same turn system as turn-based mode, with turns advanced automatically every 250 ms. Switching between the two never changes the outcome of the same inputs.

## Fullscreen

Use the ⛶ button in the game bar. The game scales to fit the screen, keeps the 8:5 aspect ratio, and draws pixels sharply.

## Saving

Progress is kept in your browser's local storage (see [PRIVACY-AND-STORAGE.md](PRIVACY-AND-STORAGE.md)). Where the in-game menus offer it, games can be exported and imported. In the public build, imports are limited to the playable level range.

## The preview limit

Each public build is playable up to its certification frontier. If you reach a staircase or other passage that leads beyond it, the message *"The way on is sealed in this preview."* appears and the party stays where it is. Nothing is lost, and later releases open more of the dungeon. See [CERTIFICATION.md](CERTIFICATION.md).
