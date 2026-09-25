# Architecture

This is a technical overview of the DeepCrawlerForge engine as shipped in `index.html`.

## 1. One file, no build

The whole program is one self-contained HTML document: markup, styles and many `<script>` blocks. Development proceeds in numbered *candidates*. Each candidate adds or corrects a scoped behaviour, usually as a new script block that wraps the previous owner of a function. The public build is the same code with the development workbench locked away (see §7). There are no dependencies, bundlers, CDNs or network calls.

## 2. Zero embedding: runtime harvesting

Nothing from the original game is stored in the program. When you drop your ZIP:

1. The ZIP is read into an in-memory virtual file system (VFS). PAK archives are expanded into their member files.
2. **Structural discovery** finds the data the engine needs inside your executables and data files. It uses executable structure (MZ relocations, call and reference patterns, table shapes) instead of hard-coded offsets. Examples are UI chrome, fonts, the viewport rectangle, item and monster tables, spell and message text, trigger programs, sound drivers and the intro program.
3. Level files are compiled into runtime mazes, wall and decoration sets, and trigger programs.
4. When a discovery is ambiguous, the engine **fails closed**. It reports "unresolved" instead of guessing, and Authentic mode never shows a guessed value.

The practical rule for contributors and reviewers: no original byte, coordinate, colour, filename-to-content mapping, level/block/item/event mapping or observed timing may be written into the code as a constant.

## 3. Deterministic simulation

- **One authoritative gameplay clock.** The world advances in turns of 250 ms of game time. There are no other gameplay timers.
- **Live mode is not a second engine.** It injects ordinary *Wait* actions every 250 ms. Live and turn-based play of the same inputs give identical results.
- **One RNG root.** A campaign captures a single 16-bit source seed when it starts, and all later randomness is timeline state. Character generation and pre-game presentation use private copies and never consume gameplay randomness.
- **World hash.** A compact hash of the complete world state (level, position, facing, turn, clocks, party, monsters, items, flags, RNG) identifies every moment of a game.
- **Timeline.** Every action is journaled with sparse checkpoints and branches. Restores happen from checkpoints with zero replay, and replays must reproduce recorded hashes exactly.

## 4. Presentation

- The 320×200 screen is composited from harvested chrome and graphics, then scaled with pixel-exact rendering. Fullscreen changes only the presentation layer and never the simulation.
- The **intro and title sequences** run the original presentation logic in a restricted, presentation-only interpreter. This interpreter executes the mounted intro program's drawing and timing code, and its presentation clock is completely separate from the gameplay clock and RNG.
- Sound and music are synthesized in the browser from the game's own driver and music data.

## 4a. Studio intro

When the page loads, a short intro (about 8 s) plays in its own full-screen overlay. First comes "Archawk Games presents", then a DeepCrawlerForge title card marked *unofficial fan project · bring your own game files*. It introduces the engine, not the game you load afterwards.

- It starts only after the engine has finished loading, so it runs smoothly. Until then the overlay is plain black.
- A click, tap or any key skips it. It is not shown at all when the system asks for reduced motion.
- It removes itself completely afterwards.
- It has no connection to the game: it doesn't read or change engine state, and it has no gameplay clock, timer or randomness.
- Its font (Orbitron, OFL) is embedded, so it also makes no network requests.

## 5. Profiles

The engine has three profiles, backed by one capability table:

| Profile | Purpose | In public build |
|---|---|---|
| Authentic | Original screen, rules and input only | ✔ |
| Enhanced | Original screen plus optional, individually switchable features | ✔ |
| Forge | Developer workbench: source inspection, direct level entry, traces, tuners | locked |

Enhanced features that affect gameplay are recorded as timeline state. A replay therefore knows which rules were active.

## 6. Certification (development side)

Correctness is established by comparing against the original DOS program, which runs in development as an **oracle/validator only**. Oracle observations are evidence: they decide pass or fail, but they never become production values or mappings. An automated planner explores the dungeon, and each new kind of interaction must pass a validator comparison before a certificate is recorded in a single certification ledger. Progress stops at the first interaction that is not yet certified. That stopping point is the **certification frontier** ([CERTIFICATION.md](CERTIFICATION.md)).

This tooling, the ledger and the evidence are not part of the public repository.

## 7. The public edition

The public `index.html` is produced mechanically from the development build of the same release ([RELEASES.md](RELEASES.md)):

- The default profile is Authentic. The Forge selector is removed, and a stored Forge preference is ignored.
- A small edition gate refuses to enter any level beyond the frontier. For stairs and other source transitions, the refusal happens *before* any state changes (the same fail-closed path the engine already uses for a missing level file). Other loaders, such as imports and restores, fail closed before loading. The gate adds no timer, RNG or gameplay state.
- External web fonts are removed, so the page makes no network requests.
- A credit line under the game shows the copyright, the licence and an *unofficial fan project, not affiliated* disclaimer.
- Gameplay code is otherwise byte-for-byte the development build. `BUILD-INFO.json` records the SHA-256 of both builds.

## 8. Known limits

- The browser/OS matrix is not fully verified yet; Chromium is the reference.
- Intro presentation parity with DOS is partial (see the status table in the README).
- Standard ZIP only (no ZIP64).
