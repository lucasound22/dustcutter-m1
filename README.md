# DUSTCUTTER M-1 PRO — FINAL DEBUG — No External Samples Needed

Why no samples folder? All 8 Roland kits are SYNTHESIZED inside index.html via Web Audio API OfflineAudioContext — no external WAVs, no CORS, no 100MB download, instant PWA load, works offline, zero-latency.

Banks:
A 909 Classic 16 pads, B 808 Legend, C 707 Vintage, D 606 Acid, E 505/LINN/DMX, F CR78/COMPURHYTHM, G MELODIC+BASS Cm7 chops sub 55Hz pluck vocal sweep tape-stop, H FX+PERC vinyl crackle riser downlifter verb stutter reverse cymbal shaker tambourine
All buffers generated in initKits() — kick sine sweeps 180->45Hz 60->35Hz etc, snare sine+noise HP1200, hats noise HP8000/9000 etc, cowbell 540+800Hz.

10 loops auto-loaded sequences 0-9: Boom Bap 94, Trap 140, Lo-Fi 85, House 124, Future Bass 150, Drill 142, Dancehall 100, Broken Beat 110, Trap Soul 90, Acid Jungle 160.

If you want real sampled Roland WAVs, you can still import them via library IMPORT button — app accepts .wav .mp3 .aiff .flac .ogg .mp4 — drag to pad, save/recall keeps them in IndexedDB .dust bundle.

Host: upload all files in this zip to GitHub Pages root. Live at https://lucasound22.github.io/dustcutter-m1/

DJ: https://lucasound22.github.io/DJLUCA/
Contact: lucasound@gmail.com

© Luca Marino Productions 2026 — Melbourne
