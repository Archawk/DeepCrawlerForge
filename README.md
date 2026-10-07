# DeepCrawlerForge

**An independently written browser engine for the original 1991 *Eye of the Beholder* (DOS) game data. Bring your own game files.**

DeepCrawlerForge is a single HTML file. Open it in a modern browser, give it a ZIP of your own *Eye of the Beholder* game folder, and play the original dungeon as a faithful **Authentic** recreation or with optional **Enhanced** quality-of-life features.

It includes **no game data**. Graphics, text, levels, fonts, sound and even the screen layout are read from your files, in your browser, every time the game starts. Nothing is uploaded.

> **Public preview 0.208.0** (`Dev95SK-Candidate208`, released 2026-10-07). You can play levels 1, 2, 3, 4, 5, 6 (fully certified only). The game stops you before any level that has not been checked yet. See [Certification status](#certification-status).

---

## Play

1. **Online:** open **https://archawk.github.io/DeepCrawlerForge/**
   **Offline:** download `index.html` from this repository (or the release ZIP) and open it in your browser.
2. Make a ZIP of your *Eye of the Beholder* folder, with the files at the top level of the ZIP (for example `EOB.EXE` and the `EOBDATA*.PAK` files).
3. Drop the ZIP onto the page, or tap **Drop eob1.zip here**.
4. Choose **AUTHENTIC** or **ENHANCED** on the start screen.

[docs/GETTING-STARTED.md](docs/GETTING-STARTED.md) covers the full steps, the files the game needs, the tested file set and troubleshooting.

**Requirements:** a current desktop browser (Chromium-based browsers are the tested reference; Firefox, Safari and mobile browsers are expected to work but are not yet part of the verified matrix), and a legally owned copy of the original DOS game. No server, install or internet connection is needed once the page has loaded.

## Modes

| | Authentic | Enhanced |
|---|---|---|
| Original 320×200 screen, rules and input | ✔ | ✔ |
| Automap / HUD map | – | ✔ |
| Turn-based mode (optional) | – | ✔ |
| Timeline scrubber (rewind/branch) | – | ✔ |
| Enemy hit points, Attack All, smart pickup, modern keyboard | – | ✔ (each optional) |
| Special quest tracker, exploration status | – | ✔ (each optional) |
| Fixes for bugs of the original game (Authentic keeps the original) | – | ✔ (each optional) |
| Restored content (unfinished spells, the Burning Hands scroll, restored ending) | – | ✔ (each optional) |
| Extended content (options that build on the original design) | – | ✔ (each optional) |
| Campaign runner: hand the game to it, take over at any moment | – | ✔ (optional) |

Each Enhanced feature can be switched on or off separately. Authentic mode never shows modern overlays. See [docs/PLAYING.md](docs/PLAYING.md).

## Certification status

DeepCrawlerForge is developed against the original game. During development, the original DOS program runs as a *validator*, and the engine's behaviour is compared with it. Features count as **certified** only when they have been measured to match.

| | This release |
|---|---|
| Fully certified levels | 1, 2, 3, 4, 5, 6 |
| Certification frontier | Level 7 (in progress) |
| Playable in this public build | up to level 6 |
| Engine regression suite | 731 tests: 537 pass, 0 fail, 194 skipped |
| Mounted start-up self-test | 28/28 PASS |
| Intro / DOS presentation parity | intro, menus, setup and character creation match DOS; combat rules, turn undead, the presentation hold, the stairs manual check, the level maintenance schedule, the encounters, magic projectiles and monster spells match the original; the certified campaign runs to the Level 7 arrival |

The playable range grows with each public release. [docs/CERTIFICATION.md](docs/CERTIFICATION.md) explains what "certified" means and how the frontier works.

## How it works (short version)

- **Zero embedding.** No original bytes, bitmaps, fonts, text tables, coordinates or level mappings ship in this repository. Everything is harvested at runtime from the files you supply.
- **Deterministic.** One authoritative simulation clock (250 ms turns) and one seeded RNG root. Live play is ordinary turns advanced automatically, so a game is always reproducible.
- **Single file.** No build step, no framework and no dependencies. `index.html` is the whole program.

Details are in [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md).

## Repository layout

```
index.html            the game (public edition, single file)
BUILD-INFO.json       exact build identity, frontier and verification summary
SHA256SUMS            checksums of every file in this release
docs/                 player and technical documentation
CHANGELOG.md          public release history
LICENSE               GNU GPL v3 (licence for the DeepCrawlerForge code)
LICENSE-ADDITIONAL-TERMS.md   copyright notice + GPL §7 attribution terms
NOTICE.md             trademarks, game data and provenance statement
```

This repository contains **published releases only**. Development, certification tooling and evidence are kept in a separate workspace. See [docs/RELEASES.md](docs/RELEASES.md) for how a public build is produced from it.

## Reporting problems

Please open an issue using the bug template. The most useful report includes the **build line from `BUILD-INFO.json`**, your browser, the mode (Authentic/Enhanced), and, if you have it, an exported timeline. **Never attach game files or saves that contain game data.** See [CONTRIBUTING.md](CONTRIBUTING.md).

## Legal

DeepCrawlerForge is free software, © 2026 Markus Kettunen, released under the **GNU GPL v3 or later** ([LICENSE](LICENSE)) with section 7 attribution terms ([LICENSE-ADDITIONAL-TERMS.md](LICENSE-ADDITIONAL-TERMS.md)). You may use, study, share and modify it freely. Anything you distribute that is based on it must stay free under the same licence, keep the credit *"DeepCrawlerForge — original work by Markus Kettunen"*, be marked as modified, and use its own name. The licence covers **only the code in this repository**. *Eye of the Beholder*, its game data and all related trademarks belong to their respective owners, and none of them are included or licensed here. This is an unofficial, non-commercial fan project. It is not affiliated with or endorsed by any rights holder. Read [NOTICE.md](NOTICE.md).
