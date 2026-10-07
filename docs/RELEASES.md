# How public releases are produced

Development happens in a private workspace that holds the full engine (including the Forge workbench), the certification tooling, the ledger and the evidence. Every development release produces five packages:

1. the current development HTML
2. the runner timeline
3. the full standalone master handover
4. the certification checkpoint
5. **this public repository**, as a ZIP

Package 5 is generated mechanically from package 3 by a packager that lives in the master handover. It is never edited by hand. Each build:

1. **Verifies identity.** The development HTML must match the hash recorded for the release.
2. **Leaves the DOS tools out.** The development HTML carries the tools that run the original DOS program beside the engine and compare them (validators, traces, probes, audits). A plan made for the exact release build lists each piece of that code, and the packager checks it against the build before cutting it. The plan was proved against every script of the build: nothing that stays refers to, reads, or depends on what is cut. After the cut, no removed name may still be referenced, or the build stops. The intro, setup, character creation and music still run the original's own routines from your files, so the small processor model they use stays.
3. **Derives the public HTML.** It locks the profiles to Authentic/Enhanced, removes the Forge selector, installs the frontier gate, removes external fonts and tidies the page head. Every edit is anchored, and a missing or duplicated anchor stops the build.
4. **Renders the documents** from templates, using the release's own status values. An unresolved placeholder stops the build.
5. **Runs the clean audit** against the tested game archive: no game-data file types, no byte-identical files, no unreviewed verbatim game text.
6. **Runs the smoke test.** The exact `index.html` runs in a headless browser. The test mounts the game files, confirms Forge can't be reached, boots a game, checks that the frontier gate refuses the next level without changing the world, and checks that the page makes no network requests.
7. **Writes `BUILD-INFO.json` and `SHA256SUMS`.** `BUILD-INFO.json` also records what the strip removed. The ZIP is built deterministically, so rebuilding the same inputs produces an identical ZIP.

## Studio intro

When enabled in the release config, the packager places the Archawk Games intro directly after `<body>`, with its font embedded. It then adds `THIRD-PARTY-NOTICES.md`. The smoke test checks that the intro finishes by itself, can be skipped with a key, and leaves the page usable.

## Licence notices in the build

The packager writes the copyright, GPL and attribution notice into the head of `index.html`, and adds a small credit line under the game ("Appropriate Legal Notices" in GPL terms) that links to the licence. Neither touches the game screen or its behaviour.

## Versioning

Public versions are `0.<candidate>.0`. For example, `0.176.0` is the public build of development candidate 176. Tags use the same number with a `v` prefix.

## Verifying a download

```sh
sha256sum -c SHA256SUMS
```

`BUILD-INFO.json` lists the development build hash (`identity.masterHtmlSha256`) the public file was derived from.
