# EP6 Sample Flip Night — finalist loop labels
## Chopped Mon Oct 26, 2026 for Tue Oct 27 · source: `~/workspace/sample-chops/songs/` (Bobby Soul chops)

Each loop is exactly **4 bars**, cut beat-to-beat on the detected beat grid (start = grid beat
nearest the shortlist point, length = exactly 16 beats), phase micro-shifted ≤27 ms and given a
5.8–11.6 ms wrap crossfade so the loop point is click-free (verified: the largest sample-to-sample
step anywhere across the wrap is *smaller* than the 99.9th-percentile step inside the loop body on
all four). BPM below is measured from the loop's own 16-beat span — the number that governs the chop.

| Track | BPM (measured) | Key | Lead instrument | Bars | Loop starts at | File |
|-------|---------------|-----|-----------------|------|----------------|------|
| track-40 | 97.1 (label 97) | G♯ minor — full-track and loop estimates agree (KS corr 0.947 / 0.955) | **vocal (est., low confidence)** — see note | 4 | 3:08.7 | `ep6-track-40_97bpm_Gsharpmin_vocal_4bar.wav` |
| track-43 | 89.9 (label 90) | D minor — full and loop agree (0.976 / 0.977, clearest margin of the four) | **bass-led (est.)** | 4 | 3:51.9 | `ep6-track-43_90bpm_Dmin_bass_4bar.wav` |
| track-30 | 117.5 (label 117) | C minor **(est.)** — full track says C♯ minor (0.967), loop says C minor (0.930 vs C♯ minor 0.928 — a coin flip); loop value used | **drums / break (est., high confidence)** | 4 | 4:10.9 | `ep6-track-30_117bpm_Cmin_drums_4bar.wav` |
| track-32 | 116.5 (label 116) | C minor — full and loop agree (0.968 / 0.972) | **keys (est.)** — horns/strings not ruled out | 4 | 0:35.9 | `ep6-track-32_116bpm_Cmin_keys_4bar.wav` |

Durations: 9.89 s · 10.68 s · 8.17 s · 8.24 s. Bar check at the label BPM: 4.00 / 4.01 / 3.98 / 3.98 bars
(all within ±0.02 bar of exact). All files 44.1 kHz / 16-bit stereo, decode-verified.

## What each loop is (only what the analysis supports)
- **track-40** — steady 4-bar groove, energy even across all four bars. A transcription pass caught a
  short repeated phrase ("just me… I'll be there") and pitched mid-band content is active ~58% of the
  loop → reads as a repeating vocal hook. Not certain: the transcriber's own no-speech score was high,
  so treat "vocal" as a lead, not a fact — a 10-second listen settles it.
- **track-43** — dark, bass-heavy groove (88% of energy under 250 Hz), even across bars, no vocals
  detected and almost no stable mid-band melodic line → the bass and drums carry it. Slowest and
  longest of the four; the most raw material around it in the source track.
- **track-30** — a drum break: ~97% percussive energy in *every* bar, no vocals, minimal pitched
  content (which is why its key estimate is the shakiest). Even level across all four bars.
- **track-32** — sustained harmonic bed (highest sustain measure of the four) over a balanced
  rhythm section, even across bars. Keys is the best single-word estimate; a horn or string pad
  would measure similarly — flagged honestly.

## Method notes / honest limits
- Key = Krumhansl–Schmuckler profiles over mean chroma (same family as CrateMatch), run on the full
  track and on the loop separately; labels follow the loop where they disagreed.
- BPM cross-check: beat-grid tempo vs onset-autocorrelation agreed within ~1 BPM on tracks 43/30/32.
  Track-40's *global* tracker read 95.7 while its loop-window beats measure 97.1 (the shortlist said
  ~96) — tempo drifts slightly across this rip; the loop is internally exact either way.
- Loop starts moved slightly from the shortlist's approximate points (which were "starts at about"):
  −0.27 s (40), −0.05 s (43), −0.08 s (30), −0.11 s (32) — all snaps onto the detected beat grid,
  plus a ≤27 ms phase nudge for the clean wrap. Lengths were NOT stretched to a nominal BPM;
  each is exactly 16 detected beats.
- Instrument labels are machine estimates from spectral/harmonic features + a transcription pass —
  marked (est.) everywhere they appear. Keith's ear is the final call, same as the shortlist.
