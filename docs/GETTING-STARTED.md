# Getting started

## 1. Get the game files

You need the files from the original **DOS** release of *Eye of the Beholder* (1991). You can use your original floppies or CD, or a digital re-release that contains the DOS files. DeepCrawlerForge does not provide these files. Please don't ask for them in issues.

The game folder normally contains files like these:

```
EOB.EXE        INTRO.EXE      EOBDATA.SAV    LEVELS.TMP
EOBDATA1.PAK … EOBDATA6.PAK   EYE.PAK
CGA.OVL  EGA.OVL  MCGA.OVL  TGA.OVL
FONT6.FNT  FONT8.FNT
```

[TESTED-GAME-FILES.md](TESTED-GAME-FILES.md) lists the exact file set this release was verified against, as names, sizes and SHA-256 hashes (no content). Other versions or languages of the DOS game may work. The engine discovers data structures from your files instead of assuming fixed offsets. However, only the listed set is verified.

## 2. Make a ZIP

Put the game files into a ZIP archive so that they sit **at the top level** of the ZIP:

- **Windows:** select the files in the game folder → right-click → *Send to → Compressed (zipped) folder*.
- **macOS:** select the files → right-click → *Compress*.
- **Linux:** `cd EOB && zip ../eob1.zip *`

The original files are only read. The ZIP is opened in your browser's memory and never modified or uploaded.

## 3. Open DeepCrawlerForge

- **Hosted:** open the project's GitHub Pages address (see README).
- **Local:** download `index.html` and double-click it. Everything runs locally, and the page makes no network requests.

Drop the ZIP onto the **Game data** box, or tap it and choose the file. Mounting takes a few seconds while the engine reads and compiles the game data.

## 4. Start playing

On the start screen, choose **AUTHENTIC** (the original experience) or **ENHANCED** (optional modern features). [PLAYING.md](PLAYING.md) covers modes, controls and the Enhanced options.

## Troubleshooting

| Symptom | What to check |
|---|---|
| Nothing happens after dropping the ZIP | The files must be at the top level of the ZIP, not inside a sub-folder. Use a standard (non-ZIP64) ZIP. |
| "LEVELn.MAZ missing" or similar | The ZIP is incomplete. Include every `EOBDATA*.PAK`. |
| "The way on is sealed in this preview." | You reached the certification frontier of this public build. See [CERTIFICATION.md](CERTIFICATION.md). |
| A save won't load | Saves from beyond the playable level range are refused in the public build. |
| Sound doesn't start | Browsers only allow audio after a click or key press. Click the game screen once. |

If a problem remains, please open an issue (see [CONTRIBUTING.md](../CONTRIBUTING.md)).
