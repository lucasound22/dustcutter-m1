# DUSTCUTTER M-1 PRO

Pocket drum machine & sampler by **Luca Marino Productions** — 128 pads, 8 classic-inspired kits, 10 demo loops, step sequencer, performance FX, sample chopping, WAV/MIDI export. Installable, works offline on iPhone, iPad and desktop.

Live: https://lucasound22.github.io/dustcutter-m1/ · DJ sets: https://lucasound22.github.io/DJLUCA/ · lucasound@gmail.com

## Deploy (GitHub Pages) — use the DEPLOY zip
1. Unzip `dustcutter-m1-pro-DEPLOY.zip`. You get a **flat** set of files (no sub-folders): `index.html`, `sw.js`, `manifest.json`, icons, etc.
2. In your `dustcutter-m1` repo, delete the old files, then upload **all** of them so `index.html` sits at the repo root (not inside another folder). On github.com: *Add file → Upload files*, drag every file in, commit.
3. Settings → Pages → Deploy from branch → `main` / `(root)`.
4. Open https://lucasound22.github.io/dustcutter-m1/ and hard-refresh (Ctrl/Cmd+Shift+R, or reopen the home-screen app twice) to pick up the new version.

`index.html` contains the entire app (CSS and JS inlined), so even if the icons are missed the app still runs.

**Troubleshooting:** a blank page almost always means `index.html` is in a sub-folder or the repo is not published yet. If an old version keeps appearing, clear the site's data in the browser (Settings → Safari/Chrome → Website data) once.

## Source
The `source` zip holds the readable multi-file project. Run `python3 build.py` to regenerate the flat `dist/` folder you upload.

## Releasing an update
Bump `VERSION` in `sw.js` (then rebuild) (e.g. `v11`). Returning users see a “new version ready” prompt.

## Structure
| File | Purpose |
|---|---|
| `index.html`, `css/app.css` | Shell and styles |
| `js/dsp.js` | Synthesis voices (kicks, snares, hats, claps, perc, keys, FX) |
| `js/kits.js` | 8 kits × 16 pads, 10 factory patterns, GM drum map |
| `js/engine.js` | Web Audio chain, voice player, lookahead sequencer, offline bounce, WAV/MIDI |
| `js/store.js` | IndexedDB autosave and projects, `.dust` import/export + validation |
| `js/app.js` | Interface |
| `sw.js`, `manifest.json` | Offline + install |

## Notes
- All sounds are synthesised in the browser; they are not samples of any Roland product. Kit names describe the character each kit is inspired by.
- `robots.txt` / `sitemap.xml` only take effect when served from a domain root; on a GitHub project page they are harmless.
- iOS: tap **Share → Add to Home Screen**. Exports use the iOS share sheet.
