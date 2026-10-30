# DUSTCUTTER M-1 PRO

Pocket drum machine & sampler by **Luca Marino Productions** — 128 pads, 8 classic-inspired kits, 10 demo loops, step sequencer, performance FX, sample chopping, WAV/MIDI export. Installable, works offline on iPhone, iPad and desktop.

Live: https://lucasound22.github.io/dustcutter-m1/ · DJ sets: https://lucasound22.github.io/DJLUCA/ · lucasound@gmail.com

## Deploy (GitHub Pages)
1. Upload **everything in this folder** (including `.nojekyll`) to the root of the `dustcutter-m1` repo.
2. Settings → Pages → deploy from the `main` branch, `/ (root)`.
3. Open the site once online; it then caches itself for offline use.

No build step, no dependencies, no network calls. To test locally: `python3 -m http.server` and open http://localhost:8000 (service workers need http(s), not `file://`).

## Releasing an update
Bump `VERSION` in `sw.js` (e.g. `v11`). Returning users see a “new version ready” prompt.

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
