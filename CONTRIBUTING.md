# Contributing

Thank you for helping. This repository publishes finished public builds. Development happens in a separate workspace, so **bug reports are the most valuable contribution**.

## Reporting a bug

Use the *Bug report* issue template and include:

- the `release` and `buildId` values from `BUILD-INFO.json`
- browser and operating system
- mode (Authentic or Enhanced) and any Enhanced options you changed
- what you did, what happened, and what the original game does in the same situation (if you know)
- if possible, an exported **timeline** from Enhanced. It lets the exact moment be replayed deterministically.

## Please do not

- attach or link game files, PAK archives, executables, or saves that contain game data
- ask for, or offer, copies of the game
- open pull requests that add game data or values copied out of the original files. The engine must discover everything from the player's own files at runtime (see [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md)).

## Code changes

`index.html` is generated from the development build, so pull requests against it can't be merged directly. If you have a fix, open an issue describing it. A patch or diff in the issue is welcome, and the change will be carried into the next development candidate with credit. By posting a patch, you agree that it may be used in DeepCrawlerForge under the project's licence (GPL-3.0-or-later with the terms in LICENSE-ADDITIONAL-TERMS.md).

## Forks

Forks are welcome under the GPL. Please give your fork its own name, keep the credit line *"DeepCrawlerForge — original work by Markus Kettunen"* visible in the page, and say that it is modified. See [LICENSE-ADDITIONAL-TERMS.md](LICENSE-ADDITIONAL-TERMS.md).

## Conduct

Be kind and assume good faith. Issues are for DeepCrawlerForge, not for general *Eye of the Beholder* support.
