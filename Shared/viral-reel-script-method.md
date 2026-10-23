---
up: "[[README]]"
tags: [project, content-creation, marketing, instagram, prompt]
moved-from: "main vault: Projects/Content Creation/viral-reel-script-method.md"
---
# Viral reel script method (clone a viral reel's structure for your niche)

Source: YouTube Short by bravetech, "How to Clone Any Creator's Viral Reels with Claude AI" (`youtube.com/shorts/Y2gLUMjhiBs`, 97 s, about 90K views, uploaded 2026-06-07). Analysed 2026-10-05 with our pipeline (timeline in `C:\dev\reels\3-analysed\yt_Y2gLUMjhiBs\`). Feeds [Instagram Campaign Scraping](obsidian://open?vault=Codebase%20and%20learning&file=Projects%2FInstagram%20Campaign%20Scraping%2FSTATE) (the hook rubric) and Blue by Fable content.

## The tool: Sort Feed
- Name read from the video's frames 10 to 14 (he searches Google for "sort feed"): **Sort Feed**, site `sortfeed.com`, a Chrome extension ("Sort Feed - works on Instagram & TikTok" in the Chrome Web Store).
- Its own tagline: "Find winning content ideas in your niche: sort, export, download, and transcribe top posts."
- The site has Pricing, Affiliates, Community (it started as a Discord) and a login page. **Price and free tier not checked.** Not installed. It runs inside your logged-in browser (Instagram account risk applies). Vet before installing.

## The method, step by step
1. Install the extension and pin it.
2. Open a competitor's (or admired creator's) Instagram profile, Reels tab. Prefer a competitor that already has viral videos.
3. Open the extension: default is the latest 25 posts; switch to **Views** to get the 25 most viewed. It gathers them for download.
4. Transcribe icon on a video: fetches the transcript and downloads it as a file.
5. Paste the prompt below into Claude, paste the transcript where it says "paste here", add niche, style and signature.
6. Result: a script with the viral video's structure, in your topic and voice.

## The prompt (verbatim from the video description)

```
You are a scriptwriter who specializes in adapting viral content for creators.

I'll give you:

1. The TRANSCRIPT of a video that went viral
2. MY NICHE (the subject I talk about)
3. MY STYLE (how I talk)

---

STEP 1 — ANALYZE THE TRANSCRIPT

Silently identify:

- Hook structure (first 2-3 sentences)
- Type of twist used
- How the lesson was delivered
- Elements that drove retention (numbers, contrast, visual scene)

---

STEP 2 — BUILD THE HOOK (TOP PRIORITY)

The hook is the first 2 sentences. They need to stop the scroll in the first 5 seconds. This is not opinion, it's how the algorithm works: if the person doesn't stop within the first 3-5 seconds, the video dies.

For that, the hook MUST activate one of these mechanisms:

PATTERN INTERRUPT
→ Say something that contradicts what the person expected to hear
→ Ex: "Volkswagen bought Audi with one goal: to kill it."

COGNITIVE TENSION (open loop)
→ Create a question in the person's head they NEED to resolve
→ Ex: "She used her wedding money to build a product. Today it makes $100 million in revenue."
→ (the brain asks: how? why? what happened?)

IMPOSSIBLE CONTRAST
→ Place two facts that shouldn't exist together
→ Ex: "This ball boy became the most powerful man in world soccer."

NUMBER THAT SHOCKS
→ A specific, unexpected number anchors attention
→ Never vague: not "made a lot of money"
→ It's: "went from $700K in debt to building a $400 million business"

ORDINARY IDENTITY + ABSURD RESULT
→ Show someone ordinary doing something impossible
→ Ex: "He was a landscaper. The sauce he gave as a Christmas gift sold for $400 million."

HOOK RULES:

✗ Maximum 2 sentences
✗ Never start with "Let me tell you..."
✗ Never start with a direct question ("Did you know that...?"). A question weakens, a statement shocks.
✓ End the second sentence on a tension point, never on an answer
✓ If the hook already resolves the curiosity, it failed

---

STEP 3 — ADAPT TO MY NICHE

Keep EXACTLY:
✓ The narrative structure
✓ The sentence rhythm
✓ The type of hook
✓ The position of the twist

Replace ONLY:
→ The topic (adapt to my niche)
→ The examples (use references from my world)
→ The numbers (use real data from my niche)

---

STEP 4 — DELIVER THE SCRIPT

Format it exactly like this, mandatory:

SCRIPT — [VIDEO TITLE]
Estimated duration: [X seconds]
Hook mechanism used: [mechanism name]
Why this hook stops the scroll: [1 sentence]

---

HOOK (0-5 seconds)
- [Sentence 1]
- [Sentence 2]

DEVELOPMENT
- [Sentence 1]
- [Sentence 2]
- [Sentence 3]

TWIST
- [Twist sentence]

ESCALATION
- [Milestone 1]
- [Milestone 2]
- [Milestone 3]
- [Milestone 4]

LESSON
- [Lesson sentence]

SIGNATURE
- [Your fixed signature]

---

(each bullet = 1 short sentence, the way you'd say it out loud)(no paragraphs, one idea per line)(maximum 15 words per bullet)

---

GENERAL RULES:

✗ Never vague numbers ("a lot", "several", "a bunch")
✗ Never abstract emotion ("got sad"). Describe the SCENE.
✗ Never a CTA in the middle of the video. Only at the end.
✓ At least 1 physical/visual detail in the development
✓ Lesson in 2 sentences max
✓ Short sentences. Speech rhythm, not text rhythm.

---

NOW SEND ME:

TRANSCRIPT:
[paste here]

MY NICHE:
[ex: digital marketing, fitness, personal finance, fashion...]

MY STYLE:
[ex: direct and casual / empathetic and motivational / analytical and cynical...]

MY FINAL SIGNATURE:
[ex: "I'm Sarah and I teach women to invest from zero. Follow me so you don't miss the next one."]
```
(Emoji icons removed from the copy above; wording unchanged.)

## How we use it
- **Hook labels for the analysis loop:** pattern interrupt, cognitive tension, impossible contrast, number that shocks, ordinary identity + absurd result. Plus its hook rules as a checklist (max 2 sentences, no opening question, ends on tension).
- **Structure labels for the timeline:** hook (0-5 s), development, twist, escalation, lesson, signature.
- **Limit:** written for story-style business videos. For shoe and fashion reels we also need product-reveal, styling and call-to-action labels (second rubric, not written yet).
- **Our pipeline's own read of this short:** hook = price claim + "watch till the end" (first 3 s); no cut for the first 11.4 s, then a cut every 3-4 s; 3.8 words per second; talking head with screen recording in the middle.
