---
tags: [content, ai-animation, pipeline]
---
# Pipeline (status 2026-10-08; source: the Documentary notes in the main vault, see [[Cross-references]])
Idea: a video is a program. Each scene is HTML + CSS + seekable animation; a renderer steps through time, captures every frame and ffmpeg joins the frames into an MP4.

## Installed (all in `C:\dev\documentary\`, see [[Shared/Where files live]])
- Hyperframes 0.8.138 (HTML to video, Apache-2.0), used through `npx`; telemetry disabled.
- Our own Puppeteer + ffmpeg harness (`render.mjs`).
- Remotion renderer from the NextWork editor repo, ffmpeg + ffprobe full build, faster-whisper (captions).
- Voices on the PC: Kokoro and Piper (see [[3 AI Animation/Sound]]).

## What exists
- Test film 1: 30 s, 1920x1080, 30 fps, silent, rendered in 37.8 s. Checks: 0 errors, contrast 42 of 42. Visually basic. See [[3 AI Animation/Productions]].

## What is missing (not built)
1. Scene plan (manifest) and a validator that checks it before rendering.
2. Voice, captions and sound stages ([[3 AI Animation/Sound]]).
3. A library of scene types: charts, timelines, comparisons, maps, callouts (Hyperframes has a registry of about 400 blocks, untested here).
4. One file per scene, cached output per scene, parallel rendering, resume after a crash (what makes an hour-long film possible).
5. Animated characters ([[3 AI Animation/Characters and animals]]).
6. Real content: the script and details for the first documentary.

## Scale estimate (UNTESTED for complex scenes)
One hour is 108,000 frames. At the measured speed for simple scenes that is about 75 minutes of capture. Heavier scenes will be slower: measure on a 3-minute piece before promising anything.
