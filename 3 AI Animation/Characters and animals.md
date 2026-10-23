---
tags: [content, ai-animation, characters]
---
# Characters and animals (a tiger, a bird)
The owner wants real animated animals in the documentaries, not only shapes and charts (2026-10-08). This note compares the ways to get them. **My assessment, nothing here is tested yet.**

| Option | Look | Cost | Fits the pipeline | Main risk |
|---|---|---|---|---|
| A. 2D vector rig in code (SVG parts moved by animation: walk cycle, wing flap) | Flat illustrated, matches the infographic style | Free | Directly (same engine as the scenes) | Drawing a good tiger or bird; each pose costs design time |
| B. Ready-made animated packs (Lottie and similar) | Depends on the pack | Free or paid | Directly (Lottie is supported) | Few animals, no control, licence per asset |
| C. 3D animated models (skeleton animation, Three.js) | Realistic or stylised 3D, camera can move | Free models exist (check each licence) | Yes (Three.js is supported by the renderer) | Heavier to render; models must come with animations |
| D. AI image-to-video | Photoreal or painterly | Cloud credits (the PC's 6 GB GPU is too small for good local models) | Clips are imported as video | Cost, consistency between shots, no frame-exact control |

**Recommendation:** start with A for the flat documentary style (one tiger walking across a scene and a bird landing on a node as the first proof, 5 seconds). Use C when a scene needs a rotating, realistic animal. Keep D for establishing shots only, via [[1 AI Generation/AI Generation]]. The owner has already learned Three.js, which makes C reachable.

## First proof (when the owner says go)
Render 5 seconds: tiger crosses the frame, a bird lands on a node of a diagram. Success = it looks good at full screen and re-renders in under a minute.

## Open
Which option the owner prefers, and the art style (flat, paper-cut, painted).
