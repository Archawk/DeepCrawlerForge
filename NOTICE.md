# Notice

## Copyright and licence

DeepCrawlerForge is © 2026 Markus Kettunen. It is free software under the GNU General Public License, version 3 or (at your option) any later version ([LICENSE](LICENSE)), with the additional attribution terms of GPL section 7 in [LICENSE-ADDITIONAL-TERMS.md](LICENSE-ADDITIONAL-TERMS.md). In short: use, study, share and modify it freely. Anything you distribute that is based on it must remain under the same licence, credit *"DeepCrawlerForge — original work by Markus Kettunen"*, be marked as modified, and not use the DeepCrawlerForge name.

The licence applies to the DeepCrawlerForge program code and documentation in this repository, and to nothing else.

## Game data is not included

This repository does **not** contain, and has never distributed, any part of the original *Eye of the Beholder* game: no executables, overlays, PAK archives, graphics, palettes, fonts, text, music, sound, level data or saves. The program reads those files from a copy the player supplies, in the player's own browser, at runtime. Nothing is uploaded or sent anywhere.

Every published build is checked automatically before release (see [docs/RELEASES.md](docs/RELEASES.md)):

- no file in the release has a game-data file type
- no file in the release is byte-identical to any file of the tested game archive
- verbatim text shared with the game files is limited to reviewed items, such as generic rules terms and short search patterns the engine uses to *find* data inside your files. These are tracked by hash, and a new occurrence fails the build.

The summary for each build is in `BUILD-INFO.json` under `verification.cleanAudit`.

## Clean-room statement

DeepCrawlerForge is an independent implementation. It does not contain code, tables or assets from ScummVM, from the original developers, or from any other re-implementation. The original DOS program is used **only during development**, as a black-box validator, and its observations are never copied into the program as values or mappings.

## Third-party components

The studio intro embeds the **Orbitron** typeface (© 2018 The Orbitron Project Authors) under the SIL Open Font License 1.1. See [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## Trademarks

*Eye of the Beholder*, *Dungeons & Dragons*, *Forgotten Realms* and related names and logos are trademarks of their respective owners, including Wizards of the Coast LLC. The original game was developed by Westwood Associates and published by Strategic Simulations, Inc. These names are used only to describe which game data this program is compatible with.

DeepCrawlerForge is an unofficial, non-commercial fan project. It is not affiliated with, sponsored by or endorsed by any of these companies.

## Rights holders

If you represent a rights holder and have a concern, please open an issue or contact the maintainer (Markus Kettunen) through the repository profile. It will be handled promptly.
