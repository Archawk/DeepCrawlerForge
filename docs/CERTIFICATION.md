# Certification and the preview frontier

## What "certified" means

A behaviour is **certified** when it has been compared with the original DOS program, under the same conditions, and found to match. The DOS program acts only as a validator: it produces evidence, and the evidence never flows back into the engine as data.

Certification covers more than "it looks right". It includes state transitions such as party stats, inventory ownership, monster state, doors and flags, together with randomness consumption and timing.

## Levels, the frontier and this release

| | Dev95SH-Candidate205 |
|---|---|
| Fully certified levels | 1, 2, 3 |
| Certification frontier | Level 4 |
| Frontier policy for this build | levels 1, 2, 3 (fully certified only) |
| Highest playable level | 3 |

The **certification frontier** is where automated certification currently stands, at the first interaction that has not yet been validated against the original.

The public build lets you play every fully certified level. Depending on the release policy, it also lets you play the frontier level itself, which is marked as *still being certified* when you enter it. The build refuses to go further:

- **Stairs, pits, portals** and any other transition driven by the game's own trigger programs are refused before anything changes. The party stays where it is, and the message *"The way on is sealed in this preview."* appears.
- **Imports and restores** into a level beyond the limit fail cleanly, with no partial state.

This limit is a courtesy boundary that keeps the public preview honest. It is not copy protection.

## Other verification in this release

| Check | Result |
|---|---|
| Engine regression suite | 624 tests: 499 pass, 0 fail, 125 skipped |
| Mounted start-up self-test | 28/28 PASS |
| Intro / DOS presentation parity | intro, menus, setup and character creation match DOS; combat rules, turn undead, the presentation hold, the stairs manual check and the level maintenance schedule match the original; the certified campaign runs from the start to the Level 4 arrival |
| Public-build smoke test (headless browser) | see `BUILD-INFO.json` → `verification.publicSmoke` |
| Clean audit (no game data in the repo) | see `BUILD-INFO.json` → `verification.cleanAudit` |

## Why progress is gated rather than simply released

Uncertified areas can contain behaviour that differs from the original in ways that affect a whole campaign, such as a door that can be forced when it shouldn't be, or an event that fires at the wrong moment. Every later public release widens the frontier. Save games from the certified range carry forward.
