---
up: "[[README]]"
tags: [project, documentary, voice]
moved-from: "main vault: Projects/Documentary/voice-options.md"
---
# Voices for the documentary (written 2026-10-07; model facts are from memory and NOT yet tested here)

Need: about one hour of narration = roughly 9,000 words, about 50,000 characters, one WAV per scene.

## What is on this PC today (tested by the Ares project, not yet for long narration)
- **Kokoro** (kokoro-onnx 0.6.1, `kokoro-fp32.onnx` + `voices.bin` in `C:\dev\Virtual Assistant\voices\kokoro`), voice `bm_fable`, runs on the RTX 3060 via onnxruntime-gpu (noted in Ares as about 3x faster than real time). Neural, clearly better than robotic voices. Free, offline.
- **Piper** (en_US-ryan-medium, joe-medium, en_GB-alan-medium): faster, more robotic. Fallback.

## Candidates to audition (not installed; sizes and VRAM needs are my recollection, check before downloading)
| Option | Cost | Notes |
|---|---|---|
| Other Kokoro voices (af_, am_, bf_, bm_ families) | free | Zero download. Quickest win: audition 6 to 8 voices on one paragraph. |
| Chatterbox / F5-TTS / XTTS-style voice-cloning models | free, local | More expressive; some can clone a voice from a short clip; heavier (likely 6 GB VRAM is tight) and slower. Licences differ: check each. |
| ElevenLabs | free tier is small (about 10,000 characters a month, far under 50,000), paid plans cost money | Best quality of the lot; the free tier cannot cover an hour. Key must never be pasted in chat. |
| Record your own voice | free | Most natural, no licence worry. Time-heavy for an hour. |

## Plan
1. Audition: render one 30-second paragraph from the real script in every voice above that is already installed (Kokoro voices, Piper) and let the user listen. No new downloads needed for this step.
2. If none is "very good" to the user, test one heavier model for a single paragraph before downloading anything big (ask first, state size).
3. Pick ONE voice for the whole film; keep pronunciation fixes in a small dictionary (names, acronyms like nextwork) applied before speaking.
4. Cache each scene's WAV by hash of text + voice + dictionary, so edits cost seconds.

## Open
- The user's definition of "very good" (warm documentary narrator? neutral? accent?). Not yet stated.
