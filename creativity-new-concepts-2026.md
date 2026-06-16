# Creativity Domain — New App Concepts (Session 2026-05-24)

**Date:** 2026-05-24
**Domain:** Creative Tools
**Ecosystem:** ljding.app (learn.ljding.app, hangwith.ljding.app)

---

## Research Findings

### Reddit User Analysis (2026) — Unmet Creative Needs

1. **No free, browser-based creative suite** — Canva backlash growing (subscription fatigue, templated output). Users want open-source, no-AI-slop alternatives.
2. **Constrained-creativity daily challenge apps barely exist** — Wordle proved bounded challenges drive 40-60% completion rates vs 5-15% for courses. No web app delivers "Wordle for creating."
3. **Writing tools confuse capture with creation** — Bear and similar apps are notes apps wearing writing clothes. Gap: focused long-form environment without $20/mo price tag.
4. **Privacy-first/offline creative tools rising** — Subscription exhaustion drives demand for tools that work without accounts, no cloud sync, no data harvesting.
5. **Cooperative creative experiences underserved** — Splice-jam style collaborative creation barely exists on web.

### Gap Analysis vs. Existing Concepts

| Already Covered (creativity-research.md) | Status |
|-----------------------------------------|--------|
| Verse (verse.ljding.app) — constrained writing | ✅ Ranked |
| Riff (riff.ljding.app) — voice brainstorm | ✅ Ranked |
| Tone (tone.ljding.app) — lo-fi music | ✅ Ranked |
| Montage (montage.ljding.app) — micro-video editor | ✅ Ranked |

---

## New Concepts (Session 2026-05-24)

### 1. Palette — palette.ljding.app

**One-line pitch:** Daily design challenge where you create something beautiful using only 3 randomly assigned colors and basic shapes.

**Why NOW:**
- Wordle/Connections proved daily bounded challenges drive retention (40-60% completion vs 5-15% for courses)
- Canva backlash: users want creation without subscription fatigue and templated output
- No web app combines daily prompts + constraint enforcement + visual community sharing
- Figma/Canva complexity ceiling locks out casual visual creators

**MVP scope:** Each day users get a 3-color palette + simple prompt (e.g., "calm", "chaos", "home"). Drag-drop shapes, gradients, and text on a fixed canvas. Community gallery with upvotes. Streak system + weekly curator's pick. Built with HTML5 Canvas or SVG manipulation — no heavy dependencies.

**Ecosystem fit:**
- **learn.ljding.app** — "Design Fundamentals" micro-courses on color theory, composition, contrast directly applicable to that day's Palette challenge
- **hangwith.ljding.app** — Group design challenges and critique circles

**Feasibility: 4/5** — SVG/Canvas editor with constraints is well-scoped. Daily prompt system is simple cron + D1 table. Main risk is mobile editor polish, but constrained tools (only shapes, no freehand) keep it manageable.

**Estimated MVP: 3 weeks**

---

### 2. Splice — splice.ljding.app

**One-line pitch:** A remix-chain collage tool where you start from someone else's creation and transform it — building collaborative art through iteration.

**Why NOW:**
- Remix culture is the dominant creative mode for Gen Z (TikTok duets, sample culture, meme templates)
- No dedicated tool for visual remix chains exists
- "Exquisite corpse" format is ancient but has never had a good digital, asynchronous implementation
- AI image tools feel solitary — Splice adds the social layer

**MVP scope:** Users upload or create a base image/collage. Others "splice" it — cropping, layering, adding text/stickers, applying filters. Each splice links back to its parent, forming a visual tree. Users browse chains, fork at any point, and follow creators. Editor is intentionally limited (crop, layer, text, 5 filters). Built with Canvas API + Cloudflare R2 for image storage.

**Ecosystem fit:**
- **learn.ljding.app** — Courses on visual storytelling, collage history, remix ethics, composition techniques
- **hangwith.ljding.app** — "Splice jams" where friend groups pass a creation back and forth in real-time sessions

**Feasibility: 3/5** — Image manipulation in-browser is doable but editor UX needs care. R2 storage for images adds infrastructure. Chain/tree data model in D1 is straightforward. Main risk: editor polish (3-week stretch, 6 weeks comfortable).

**Estimated MVP: 4-6 weeks**

---

### 3. Flicker — flicker.ljding.app

**One-line pitch:** Shake your phone, tap the screen, or hum a note — Flicker turns your body's micro-inputs into unique generative art pieces.

**Why NOW:**
- Generative art went mainstream via NFTs but creation side stayed code-heavy
- Phone sensors (accelerometer, gyroscope, microphone) are universally available but almost never used as creative input
- Lo-fi aesthetic trend means "imperfect, organic, human-feeling" outputs are valued over polished renders
- Zero skill floor — creativity without learning curves

**MVP scope:** Users pick a "seed style" (geometric, organic, particle, wave) then generate art by interacting physically — tilting the phone affects color, tapping adds elements, ambient sound influences movement. Each piece takes 10-30 seconds. Shareable as images or looping animations. Daily gallery showcases community creations. Built with p5.js/Canvas + Web Audio API + DeviceMotion API.

**Ecosystem fit:**
- **learn.ljding.app** — Generative art basics, understanding algorithms, creative coding intro (funnels users into learning p5.js)
- **hangwith.ljding.app** — "Flicker together" mode where friends' sensor inputs combine into a single collaborative piece

**Feasibility: 4/5** — p5.js handles rendering. DeviceMotion API is well-supported on mobile browsers. Art generation can start simple (Perlin noise + particle systems) and expand. Storage is lightweight (save as PNG to R2). Main risk: outputs must feel genuinely beautiful, not random.

**Estimated MVP: 3-4 weeks**

---

## Summary Table — All Creativity Apps

| Rank | App | Subdomain | Feasibility | Differentiation | Monetization | Ecosystem Fit | **Total** |
|------|-----|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 1 | **Montage** | montage.ljding.app | 2 | 8 | 8 | 8 | **26** |
| 2 | **Riff** | riff.ljding.app | 4 | 9 | 7 | 9 | **29** |
| 3 | **Tone** | tone.ljding.app | 3 | 8 | 6 | 7 | **24** |
| 4 | **Verse** | verse.ljding.app | 5 | 8 | 7 | 8 | **28** |
| 5 | **Palette** | palette.ljding.app | 4 | 8 | 7 | 8 | **27** |
| 6 | **Splice** | splice.ljding.app | 3 | 9 | 7 | 8 | **27** |
| 7 | **Flicker** | flicker.ljding.app | 4 | 9 | 6 | 6 | **25** |

*Scoring: 1-5 per category, max 20. Montage scores highest on raw points but feasibility is 2/5.*

---

## Recommended Build Order (Creativity Domain)

| Order | App | Rationale |
|-------|-----|-----------|
| **1** | **Palette** | Safest bet — lowest technical risk, proven daily-challenge retention model, clearest learn synergy, 3-week MVP |
| **2** | **Verse** | Easiest MVP (5/5), strong differentiation, direct learn.ljding.app synergy, weekend-scope |
| **3** | **Flicker** | Most novel and differentiated, zero skill floor, 3-4 week MVP, mobile sensor creativity is genuinely white space |
| **4** | **Riff** | Speech tech is mature, high differentiation, strong ideation use case for both learn and hangwith |
| **5** | **Tone** | Natural audio extension but sample curation adds complexity; build after tone.ljding.app ecosystem exists |
| **6** | **Splice** | Highest ceiling but image editor complexity; build after Palette has established community patterns |
| **7** | **Montage** | Highest demand but technically complex (video compositing); wait for WebCodecs maturity or leverage FFmpeg.wasm |

---

## Grand Rankings — All Domains

| Grand Rank | App | Domain | Subdomain | **Total** |
|-----------|-----|--------|-----------|:---------:|
| 1 | **Drift** | Productivity | drift.ljding.app | **18** |
| 1 | **静心 (JingXin)** | Mindfulness | jingxin.ljding.app | **18** |
| 1 | **Recall** | Education | recall.ljding.app | **18** |
| 1 | **Passage** | Education | passage.ljding.app | **18** |
| 1 | **SkillAdjacent** | Career | skills.ljding.app | **18** |
| 1 | **InterviewPal** | Career | interview.ljding.app | **18** |
| 7 | **Compass** | Productivity | compass.ljding.app | **17** |
| 7 | **Handoff** | Productivity | handoff.ljding.app | **17** |
| 7 | **Radar** | Wellness | radar.ljding.app | **17** |
| 7 | **心情簿 (XinQingBu)** | Mindfulness | xinqing.ljding.app | **17** |
| 7 | **吐纳 (TuNa)** | Mindfulness | tuna.ljding.app | **17** |
| 7 | **同修 (TongXiu)** | Mindfulness | tongxiu.ljding.app | **17** |
| 7 | **Cohort** | Education | cohort.ljding.app | **17** |
| 7 | **ResumeVault** | Career | resume.ljding.app | **17** |
| 7 | **SalaryStreet** | Career | salary.ljding.app | **17** |
| 16 | **Palette** | Creativity | palette.ljding.app | **27** |
| 16 | **Splice** | Creativity | splice.ljding.app | **27** |
| 16 | **Verse** | Creativity | verse.ljding.app | **28** |
| 16 | **Tidbit** | Productivity | tidbit.ljding.app | **16** |
| 16 | **Review** | Productivity | review.ljding.app | **16** |
| 16 | **Stack** | Wellness | stack.ljding.app | **16** |
| 16 | **Explain** | Education | explain.ljding.app | **16** |
| 16 | **Translate** | Education | translate.ljding.app | **16** |
| 16 | **ConnectKit** | Career | connect.ljding.app | **16** |
| 24 | **Riff** | Creativity | riff.ljding.app | **29** |
| 25 | **Flicker** | Creativity | flicker.ljding.app | **25** |
| 26 | **Montage** | Creativity | montage.ljding.app | **26** |
| 26 | **Tempo** | Productivity | tempo.ljding.app | **15** |
| 26 | **StressMap** | Wellness | stressmap.ljding.app | **15** |
| 26 | **禅修 (ChanXiu)** | Mindfulness | chanxiu.ljding.app | **15** |

---

## Updated Full Build Order

1. **Drift** — Smallest scope, highest score, builds daily habit
2. **Recall** — Core to learn.ljding.app, bilingual web-first SRS gap, 4-6 weeks
3. **Passage** — Novel read→recall pipeline, highest ecosystem fit, 4-5 weeks
4. **Radar** — Second smallest scope, first wellness entry, fills clear burnout gap
5. **Compass** — Complements Drift (weekly planning + daily focus)
6. **Cohort** — Simplest MVP, strongest social integration with hangwith.ljding.app, 2-3 weeks
7. **Handoff** — Most differentiated productivity app, solves unaddressed problem
8. **静心 (JingXin)** — Top mindfulness score, bilingual web-first gap, ~5-7 weeks
9. **心情簿 (XinQingBu)** — Simplest MVP (2-3 weeks), privacy-first, serves as data source for others
10. **吐纳 (TuNa)** — Breathwork category (3-4 weeks), complements meditation
11. **Stack** — Behavior science moat, moderate scope
12. **Explain** — AI tutor is high-demand but depends on LLM quality, 4-5 weeks
13. **Tidbit / Review** — Both score 16, pick based on personal utility
14. **Translate** — Highest differentiation but most complex (CJK handling), defer to mid-phase
15. **Tempo** — Requires more data before useful, lower urgency
16. **SkillAdjacent** — Visual skill adjacency mapper, strong learn.ljding.app integration, 4-5 weeks
17. **ResumeVault** — Career document vault, simplest career MVP, 3-4 weeks
18. **InterviewPal** — AI mock interview, high complexity but high demand; best after ResumeVault
19. **SalaryStreet** — Community building required; best after ecosystem has traffic
20. **ConnectKit** — Fastest MVP (2-3 weeks), natural hangwith extension, low monetization
21. **同修 (TongXiu)** — Complex real-time; best after hangwith.ljding.app has user base
22. **StressMap** — Highest differentiation but complex integrations, defer to later
23. **禅修 (ChanXiu)** — Niche audience; content sourcing challenge; build with Buddhist partner
24. **Palette** — Creativity: safest first build, daily-challenge retention model, 3-week MVP
25. **Verse** — Creativity: easiest MVP (5/5), constrained writing with community, weekend-scope
26. **Flicker** — Creativity: most novel, zero skill floor, phone sensor → generative art
27. **Riff** — Creativity: voice brainstorm → idea map, strong learn/hangwith integration
28. **Tone** — Creativity: lo-fi music sequencer, natural audio extension
29. **Splice** — Creativity: visual remix chains, highest ceiling but editor complexity
30. **Montage** — Creativity: highest demand but technically complex; defer to later

---

## Sources

- [Reddit Analysis: What Users Really Want From New Apps 2026](https://nomusica.com/reddit-analysis-reveals-what-users-really-want-from-new-apps-and-saas-tools-in-2026/)
- [10 Trends Creatives Are So Over in 2026](https://www.creativeboom.com/insight/10-trends-creatives-are-so-over-in-2026/)
- [Biggest Complaints About AI Tools 2025-2026](https://strongmocha.com/composing/ai-generator/you-won-t-believe-the-biggest-complaints-about-ai-tools-in-2025-2026/)
- [Web Speech API Browser Support](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API)
- [Tone.js Audio Library](https://tonejs.github.io/)
- [WebCodecs API Status](https://developer.mozilla.org/en-US/docs/Web/API/WebCodecs_API)
- [Wordle Success Proof of Concept](https://www.nytimes.com/wordle/)
- [Loom Market Position](https://loom.com/)

---

*Session completed 2026-05-24. Creativity domain — 3 new concepts generated: Palette, Splice, Flicker.*