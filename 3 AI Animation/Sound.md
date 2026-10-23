---
tags: [content, ai-animation, sound]
---
# Sound
**Status 2026-10-08: the test film has no audio at all.** Fixing this is the first job.

## What is available today
- **Narration:** Kokoro (voice `bm_fable`, runs on the RTX 3060) and Piper, both on the PC. Faster Kokoro voices to audition at no download cost. Heavier cloning models are an option later (ask before downloading).
- **Sound effects:** a bundled library of 19 effects in Hyperframes; ffmpeg can also synthesise whooshes and hits.
- **Mixing:** ffmpeg filters tested present: `sidechaincompress` (music ducks under the voice), `loudnorm` (consistent loudness), `amix`, `apad`.
- **Captions:** faster-whisper gives word timings.
- **Music:** stock music needs the owner to sign in to HeyGen (free catalog). Without it: no music, or generated music (MusicGen, heavy and not installed).

Full voice comparison (Kokoro, Piper, cloning models, ElevenLabs limits): [[3 AI Animation/voice-options|Voice options]] (moved here from the main vault 2026-10-08).

## Plan
1. Audition 6 to 8 Kokoro voices on one paragraph; the owner picks one voice for the whole film.
2. Add narration per scene (cached by text and voice so edits are cheap), captions from word timings.
3. Add a music bed that ducks under the voice, and a few effects on cuts and transitions.
4. Normalise loudness; listen on speakers and on a phone.
5. Check: play the 30-second test film again with sound.

## Open
Voice style (warm narrator, neutral, accent), and whether to sign in to HeyGen for music.
