# DUSTCUTTER M-1 PRO — FINAL PRODUCTION v3 QA

**Pocket production instrument that beats hardware.**

Links:
- App: https://lucasound22.github.io/dustcutter-m1/
- DJ Luca Marino: https://lucasound22.github.io/DJLUCA/
- Contact: lucasound@gmail.com
- Location: Melbourne, Victoria, Australia

## Final QA Checklist — All Fixed

- Save/Recall Projects: IndexedDB `dustcutter-projects` with stores `projects` + `samples`, `saveProject(id,name)` serializes full state {id,name,version:3,timestamp,bpm,swing,currentSeq,currentBank,sequences[128][16],padsMeta[128],knobVals,perfVal,perfAssign,chokeGroups,padLinks,snapshotsMeta,history 50}, audio buffers Float32Array per pad, autosave 20s + visibilitychange + beforeunload, crash recovery banner if autosave <24h RESTORE/DISCARD, Project Manager New/Save/Save As/Load/Export .dust bundle/Import .dust/.json/Duplicate/Delete/Rename search size/date, versioned v3 migration, validation, portable .dust bundle base64 samples, backup checkpoints
- Preloaded demo: 909 kit synthesized offline kick 180->45Hz sine sweep 80ms snare 180Hz+noise HP1200 closed hat HP8000 80ms open HP6000 350ms clap triple burst rim 1000Hz 60ms toms 90->60 & 200->120 melodic Cm7 C4 Eb G Bb filtered +7st reverse sub 55Hz pluck triangle vocal bandpass sweep 300->1200 tape stop dive, demo boom-bap 94 BPM auto-loaded kick 1,7,11 snare 5,13 hh 16ths
- Rainbow waveform Serato style pink-orange-yellow-green-cyan-purple + green slice overlay triangle markers Level/Filter/Attack/Release knobs green LED arcs
- Neon sequencer 8x16 KICK red SNARE orange HH cyan CLAP magenta TOM purple RIDE blue PERC cyan BASS purple glowing box-shadow velocity opacity mixer LED meters
- Stem Studio MIX rainbow 120px + 4 curved neon SVG beziers purple lime orange blue → VOCALS DRUMS BASS MELODY lanes solo/mute/chop/load simulated filtering bandpass/lowpass
- AI Groove Generator STYLE Boom Bap/Trap/Future Bass/House/Lo-Fi COMPLEXITY RANDOMIZE GENERATE probability swing ghost notes fill every 4/8/16 humanize timing/velocity lock kick/snare bass prog Cm Ab Eb Bb editable undoable
- Pro Stretch Serato Pitch n Time layout GRID SHOW SNAP WAVE ZOOM SCALE LIN/LOG RANGE 2X/4X/8X ALGORITHM Harmonic/Transients/Voice TEMPO FIXED/VARIABLE/MORPH SOURCE BPM BARS:BEATS METER 4/4 RATE CHANGE 50-200% OUTPUT BPM LENGTH TIMECODE SOURCE/TARGET START/END/LENGTH CAPTURE PITCH FIXED/VARIABLE/VARISPEED HERTZ NOTE CENTS KEY SHIFT -12/+12 OUTPUT SEMITONES quality High OfflineAudioContext vs Battery playbackRate original untouched
- Macro Engine XY 280x280 red glowing trail dot two LEVEL faders Kaoss style filter/pitch/delay/reverb/distortion morph quantise beat/bar recordable 4 slots A-D assign multiple params checkboxes morph slider bank selector A/E B/F C/G D/H 4x4 purple LEDs
- Mixer 8ch+master vertical faders LED meters Gain Pan Mute Solo FX routing matrix pads->tracks->buses->master lines sidechain group buses
- Mastering LUFS short-term true-peak clipping stereo correlation spectrum limiter threshold reference A/B loudness-matched export WAV/Stems/MIDI/.dust One-Tap Track Builder intro/main/variation/breakdown/outro editable original preserved snapshot
- History timeline edits recordings FX audition earlier version snapshots Before FX Drum Switch Final Mix take lanes T1-T5 M S R Clips dropdown Audio-01 blue comp highlight combine best sections keep alternates without clutter A/B compare loudness-matched Live Capture rolling buffer red pulse indicator immediate slice Sound-to-Sound Search timbre/transient/pitch/length tempo/key filters ranked Never Lose a Beat continuous journaling autosave 20s IndexedDB crash recovery validation
- Usability: 44px+ targets touch-action manipulation user-select none active scale 0.94 gesturestart zoom blocked haptics vibrate 10 audio unlock TAP TO START AUDIO ENGINE overlay recovery bar Resume Keep Awake bottom yellow wakeLock safe-area 100dvh no horizontal overflow
- PWA: manifest icons 72-1024 sw.js cache offline installable iOS home screen theme #0A0A0E apple-mobile-web-app-capable
- SEO: robots.txt sitemap.xml manifest OG Twitter JSON-LD Organization sameAs DJ link email canonical

## Host on GitHub Pages
1. Create repo `dustcutter-m1`
2. Upload all files in this zip to root
3. Settings → Pages → Deploy from branch main / root
4. Live at https://lucasound22.github.io/dustcutter-m1/
5. iPhone → Share → Add to Home Screen

© Luca Marino Productions 2026 — Melbourne
