---
tags: [content, research, temporary]
up: "[[Index]]"
---
# TEMPORARY research: how 3D content and documentaries are made with Claude (2026-10-23)

Status: first pass. **No Reddit evidence yet**: Reddit is blocked for WebSearch, WebFetch and the Chrome extension ("not allowed due to safety restrictions"), and agent-reach has no Reddit backend installed (needs a logged-in session: OpenCLI via Chrome login, or rdt-cli with cookies). Everything below comes from blogs, GitHub, Hacker News and vendor pages. Vendor claims are marked.
To be restructured later into the research-team list (user plan, 2026-10-23).

## A. 3D with Claude: the four patterns people actually use
| # | Pattern | How it works | Verdict from sources |
|---|---|---|---|
| 1 | **Blender MCP** (Claude drives Blender) | Add-on in Blender + MCP server; Claude runs Python in the open session, reads viewport screenshots. `ahujasid/blender-mcp` (~21.6K stars, Show HN 151 pts / 61 comments, 2025-07), now an **official Blender Lab MCP add-on** (tested Blender 5.1, `claude mcp add blender ... uv ... run blender-mcp`). | Good for scene layout, primitives, materials, lights, camera, batch rename/cleanup, simple keyframes. Weak at organic forms, topology, Geometry Nodes, rigging/weights, precise placement, proportions. "Scene director, Blender stays the source of truth." |
| 2 | **Generator + Claude as glue** | Blender MCP calls Hyper3D Rodin / Hunyuan3D / Meshy / Poly Haven / Sketchfab for assets, Claude places and fixes them. | Image-to-3D best on single objects; complex scenes hit-or-miss. Meshy comparison pages are vendor marketing; the useful metric is cost per approved asset (retries + cleanup). |
| 3 | **Code-only procedural 3D** (img2threejs skill) | Claude Code skill: reference image to a TypeScript Three.js factory built from primitives and shaders, with pivots/sockets for animation, reference-vs-render sheet each step. Apache-2.0, 10.6K to 15.6K stars (sources conflict). | Close to the photo, not photoreal; 10 to 20+ min per model. Already in the user's own pipeline (see Projects/img2threejs). |
| 4 | **Vibe-coded Three.js games/sites** | Claude writes the scene in code (e.g. HN "I hate cubes" game). | Cheap, shareable, no asset pipeline. |

Known failure modes (MindStudio, Medium): Blender API drift (Claude knows older versions; suggestion: use 3.6 LTS if scripts fail), bad Booleans/modifier order, surfaces that look fine but deform badly under a rig, connection drops when Blender crashes, Python-exec security risk (disable telemetry; don't leave the add-on running). Nothing found yet on rigging quality specifically.

## B. Documentaries with Claude: the pipeline everyone converges on
research -> script (beat sheet + fact check, human approves) -> voice -> visuals -> edit/compose -> render -> review.
| Piece | Options seen |
|---|---|
| Research / script | Claude (+ NotebookLM to study what already performs; vendor-written guides) |
| Voice | ElevenLabs (scene-based skill, timing validation, per-line caching), or offline Piper TTS (free) |
| Visuals | (a) **Real footage**: Archive.org, NASA, Wikimedia, Pexels/Pixabay/Unsplash, ranked with CLIP (OpenMontage "documentary montage"); (b) **code-drawn animation** in Remotion/HyperFrames (no footage at all); (c) generated clips (Higgsfield, fal.ai, Runway, Gemini images) |
| Edit / render | Remotion (free up to 3 people, paid for companies of 4+), HyperFrames, FFmpeg |
| Projects | **OpenMontage** (AGPL-3.0, new, no releases, Windows npm issue #148, $10 default budget cap, must say "documentary montage / real footage only" or it animates stills), LearnWithHasan Remotion shorts repo (MIT, ~38 to 42 s shorts, ElevenLabs needed, tested on Windows 11), ECC `video-editing` skill |
| Cautionary | InstantVideos.org ("documentary in 30 s", Show HN 26 pts / 31 comments, 2026-07) is **now shut down**; no stated method. |

## C. Risks to carry into the workflow
- **YouTube monetisation** (secondary sources, unverified against YouTube's own page): "inauthentic content" enforcement is channel-level; automated, templated, repetitive faceless channels get demonetised; AI voice alone is not the trigger, lack of creator input is. Check YouTube's policy page before building for revenue.
- **Licences**: AGPL (OpenMontage), Remotion company licence, footage licences per source.
- **Revenue claims** in faceless-channel guides ($400K etc.) are unverifiable marketing; ignore for planning.

## D. Gaps / next steps for the research team
1. **Reddit** (r/ClaudeAI, r/blender, r/threejs, r/aivideo, r/NewTubers): needs a logged-in route. Options: (a) user pastes/exports threads, (b) install agent-reach OpenCLI using the user's Chrome login (credential decision is the user's), (c) skip.
2. YouTube transcripts/comments of "Claude + Blender" and "AI documentary" tutorials (yt-dlp is installed; JS-runtime config warning from `agent-reach doctor`).
3. GitHub issues of blender-mcp and OpenMontage for real failure reports.
4. Rigging/character quality: test, don't read (the user's 3D Avatar project is the evidence base).
5. Map to the team workflow: each pattern above = one "capability card" (inputs, tools, cost, failure modes, verdict).

## Sources
- [Blender MCP real-world performance (MindStudio)](https://www.mindstudio.ai/blog/claude-blender-mcp-real-world-performance)
- [Claude Code and Blender MCP (hydroxide.dev)](https://hydroxide.dev/articles/blender-mcp-claude-code/)
- [How to 3D model anything with Claude + Blender (The Rundown)](https://app.therundown.ai/guides/how-to-3d-model-anything-with-claude-blender)
- [ahujasid/blender-mcp docs mirror](https://docsearch.algolia.com/mcp/docs/repo/ahujasid/blender-mcp)
- [Show HN: MCP server for Blender](https://blender-mcp-psi.vercel.app/)
- [img2threejs repo](https://github.com/img2threejs/img2threejs)
- [OpenMontage setup/FAQ (explainx)](https://explainx.ai/blog/openmontage-agentic-video-production-claude-code-2026)
- [Faceless Shorts with Claude Code (LearnWithHasan)](https://learnwithhasan.com/guide/how-to-make-faceless-youtube-shorts-with-claude-code/)
- [Claude + HyperFrames + ElevenLabs (MindStudio)](https://www.mindstudio.ai/blog/ai-video-generation-claude-code-hyperframes-elevenlabs)
- [Higgsfield faceless channel](https://higgsfield.ai/blog/start-faceless-channel-with-ai) (vendor)
- [YouTube monetisation timeline 2026 (AIR)](https://air.io/en/monetization/youtube-monetization-policy-changes-2026-a-complete-dated-timeline) (secondary)
- [InstantVideos.org](https://instantvideos.org/) (ended)
