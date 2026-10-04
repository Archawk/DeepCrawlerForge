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

## Provenance

DeepCrawlerForge is an independently rewritten EOB-compatible engine. It contains no copy of the original game program or its data files, and no code, tables or assets from ScummVM or from any other re-implementation.

The original game program is never distributed with DeepCrawlerForge. During development it is used as the behavioral oracle and validator. At runtime, the player's own supplied game files—including the executable—are read locally as external input so DCF can discover source structures and behavior. No original game executable bytes are embedded in DeepCrawlerForge. The engine finds what it needs inside **your** files when it starts: graphics, text, levels, rules and the program's own tables are read from them, and the places in the program that hold them are located by decoding its instructions.

The current technical provenance audit finds no known material third-party source expression, original game payloads, substantial executable fingerprints, original-program addresses, or authored Authentic source mappings in the distributed public code.

This is a technical provenance assessment, not a formal legal clean-room certification.

Every release runs a provenance audit over the exact public `index.html`: byte-pattern locators, addresses of the original program, identifiers removed earlier, and reviewed authored constants. The result is in `BUILD-INFO.json` under `verification.provenanceAudit`. Since Dev95SE Candidate200 the audit reports no open item (`claimReady: true`): code in your copy of the program is found by decoding its instructions, not by stored byte patterns; no address of the original program is embedded; and the engine's event names and interface record layout are read from your program rather than written into the engine. Every earlier finding is registered as removed, and a release in which one reappears fails the audit and is not published.

## Third-party components

The studio intro embeds the **Orbitron** typeface (© 2018 The Orbitron Project Authors) under the SIL Open Font License 1.1. See [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## Trademarks

*Eye of the Beholder*, *Dungeons & Dragons*, *Forgotten Realms* and related names and logos are trademarks of their respective owners, including Wizards of the Coast LLC. The original game was developed by Westwood Associates and published by Strategic Simulations, Inc. These names are used only to describe which game data this program is compatible with.

DeepCrawlerForge is an unofficial, non-commercial fan project. It is not affiliated with, sponsored by or endorsed by any of these companies.

## Rights holders

If you represent a rights holder and have a concern, please open an issue or contact the maintainer (Markus Kettunen) through the repository profile. It will be handled promptly.
