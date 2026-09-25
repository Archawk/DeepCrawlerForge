# Privacy and storage

- **No network.** The public `index.html` makes no network requests: no fonts, CDNs, analytics or telemetry. Every release is smoke-tested for this.
- **Your game files stay local.** The ZIP you drop is read into browser memory, is never uploaded, and is not stored by the page.
- **What is stored, and where.** The page uses your browser's own storage for this site only:
  - `localStorage`: the selected profile (`dcf_profile`), Enhanced options, and restored-content toggles.
  - `IndexedDB`: the Enhanced timeline and checkpoints of your current game, if the timeline is enabled. It is saved after a short pause in play, at most every 15 seconds, and when the page is hidden (you switch tabs or leave). Checkpoints store only what changed since the start of the timeline, so long games stay small.
- **Clearing.** Clearing site data in your browser removes everything the page has stored. Your game files are not affected.

When you open the hosted GitHub Pages copy, GitHub serves the file and may keep standard web server logs under its own privacy policy. Opening a downloaded `index.html` locally involves no server at all.
