---
tags: [content, ai-animation, todo]
---
# Sketchbook Reels: to-do (created 2026-10-10)
Goal (owner): 30 to 40 s vertical reels, dark sketchbook / charcoal look, drawn at 8-12 fps, stories with characters that do things, realistic voices, one integrated command. Free and local. Architecture: [[3 AI Animation/Sketchbook Reels - architecture]].

## Setup
- [ ] ComfyUI portable v0.39.0 (nvidia cu126, 1.9 GB) downloading to `C:\dev\comfy-dl`, extract to `C:\dev\comfy`
- [ ] SDXL base 1.0 safetensors (6.9 GB) downloading, move to `C:\dev\comfy\...\models\checkpoints`
- [ ] First run: check GPU is used, low-VRAM mode, time per picture
- [ ] Charcoal / ink LoRA (find, check licence, safetensors only)
- [ ] Chatterbox (Resemble AI, MIT): check install size and whether it fits 6 GB; test one sentence
- [ ] Decide on a stronger image model (FLUX GGUF?): see Q&A below

## Proofs (one at a time, show the owner each)
- [ ] 3 test frames: charcoal portrait, dark street, sketch chart
- [ ] Lock the style recipe: one style prompt + seed/LoRA, saved as `style.json`
- [ ] One puppet character split into layers (head, torso, arms, 3 mouth shapes), speaking one line
- [ ] Sketchbook look in HyperFrames: 8-12 fps stepping, line boil (SVG turbulence), paper grain, scribble reveal
- [ ] Voice test: Kokoro vs Chatterbox on the same sentence

## Integration
- [ ] One command: script -> storyboard -> pictures -> animate -> voice + captions + music -> MP4
- [ ] Scene validator (no render before the plan passes)
- [ ] Per-scene cache and resume after a crash
- [ ] Phone delivery (Ares 🎬 button already serves story.mp4; generalise to the latest render)

## Waiting on the owner
- [ ] ONE reference clip or image of the exact look wanted
- [ ] The Bangla caption lines for the story video (type them or send a voice note)
- [ ] Which characters / story for reel 1

## Rules for this project
- Voice cloning only of the owner's own voice or voices with rights.
- Models: .safetensors only, official sources, no custom ComfyUI nodes before vetting.
- FLUX.1 dev is non-commercial: check licences before monetised posts.
