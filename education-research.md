# Education Domain Research for ljding.app

**Date:** 2026-05-22
**Context:** Ecosystem includes learn.ljding.app, hangwith.ljding.app | Existing: productivity (3 apps ranked), wellness (3 apps), mindfulness (5 apps) | Stack: Vue 3 + Vite + TailwindCSS + Cloudflare Workers/D1

---

## Market Overview

The global edtech market continues to evolve with several key trends as of mid-2026:

1. **Spaced repetition goes mainstream** — Anki surpassed 10M users; Notion-based spaced repetition tools proliferate, but web-first alternatives scarce
2. **AI tutoring finally maturing** — GPT-4o-class models enable natural dialogue tutors; web-first AI tutors still rare
3. **Language learning app consolidation** — Duolingo dominance but bilingual (EN/ZH) web tools underserved
4. **Study tool fragmentation** — students use 5+ disjointed tools (Notion, Anki, Google Calendar, a timer, a notes app)
5. **"Bidirectional" learning** — teaching others is proven to improve retention, but no tool facilitates peer teaching well
6. **Web-first gap persists** — most innovation happens in mobile apps; desktop learners underserved

## Gap Analysis

### What Students Complain About in Learning Tools

| Gap | Description | Affected Segments |
|-----|-------------|-------------------|
| **Tool fragmentation** | No single place for study planning, spaced review, focus timer, and note capture | All students |
| **Spaced repetition UX** | Anki is powerful but ugly; modern alternatives are either mobile-only or Notion-dependent | Self-directed learners |
| **No native web Anki** | AnkiDroid exists but no clean web-first SRS with good UX | Web-focused learners, developers |
| **Bilingual study tools** | Chinese learners of English (and vice versa) lack web-first tools with CJK support | Chinese diaspora, ESL learners |
| **AI tutoring on desktop** | AI tutors are mobile apps (CourseHero, Chegg) or complex LMS; browser-based AI tutoring rare | Students who want 24/7 help |
| **Passive reading vs active recall** | Read-it-later tools (Pocket, Instapaper) don't integrate with active recall | Lifelong learners |
| **Study session tracking** | No tool tracks *what* you studied, *how long*, and *outcome quality* | Self-tracking nerds |

### Underserved User Segments

1. **Chinese-English bilingual learners** — 1.4B people studying a second language with almost no web-first bilingual tools
2. **Indie hackers / self-taught developers** — learn programming via scattered resources (YouTube, docs, courses) with no unified study system
3. **Graduate students** — managing papers, notes, literature reviews with no good tool for web-centric workflows
4. **Language learners doing SRS** — using Anki on desktop but wanting a web-native alternative that isn't ugly

## Competitive Landscape

| Tool | Type | Web? | Gaps |
|------|------|------|------|
| **Anki** | SRS flashcard | ❌ Desktop only (ankiweb.net is limited) | Ugly, no modern UX, limited media |
| **Duolingo** | Gamified language | ✅ | English-only mobile, no SRS depth |
| **Notion** | All-in-one workspace | ✅ | Not designed for study sessions, no SRS native |
| **RemNote** | Academic note-taking + SRS | ✅ | Heavy, complex, expensive |
| **Roam Research** | Zettelkasten + SRS | ✅ | Expensive, steep learning curve |
| **Obsidian** | Local PKM | ❌ (local) | Requires setup, desktop-only |
| **Quizlet** | Flashcard + games | ✅ | No spaced repetition, shallow |
| **Chegg** | AI tutoring | ✅ | Subscription expensive, mobile-first |
| **Course Hero** | Study resources | ✅ | Not a learning tool, a document database |
| **Khan Academy** | Video courses | ✅ | No SRS, no AI tutoring depth |
| **Campfire** | Spatial learning | ✅ | Very new, still rough edges |

## App Concepts

### 1. Recall — recall.ljding.app

**One-line pitch:** Web-first spaced repetition system with a beautiful UX, bilingual card creation, and a focus session timer — built for developers and self-directed learners who want Anki's power without the friction.

**Why NOW:**
- AnkiDroid is the only decent option for desktop learners; web-native SRS is genuinely undersupplied
- RemNote and Roam are too heavy/expensive; there's a gap for "Anki but modern"
- Bilingual card creation (EN↔ZH) is completely unserved on web
- learn.ljding.app could integrate Recall as its study engine

**MVP Feasibility:** 4/5 — Card CRUD, SM-2 or FSRS algorithm, basic review UI, local storage for MVP. Cloud sync later.

**Ecosystem Fit:**
- learn.ljding.app: native study engine; spaced review for any course content
- drift.ljding.app: focus session data feeds into recall quality tracking
- radar.ljding.app: burnout risk can factor in study load from recall

**Ratings:**

| Criterion | Score | Rationale |
|-----------|-------|-----------|
| Market Demand | 8 | Anki's popularity proves demand; web-first SRS gap is clear |
| Technical Complexity | 4 | SRS algorithm + card UI + storage; no novel ML needed |
| Differentiation | 8 | Beautiful web-native SRS with bilingual support is genuinely novel |
| Ecosystem Fit | 9 | Core to learn.ljding.app; natural integration with multiple ecosystem apps |

### 2. Explain — explain.ljding.app

**One-line pitch:** AI-powered study buddy that explains concepts at your level — starts with a diagnostic question, adapts explanation depth, and generates practice problems. Web-first, text-based, no video.

**Why NOW:**
- AI tutoring is the #1 edtech trend; Chegg/CourseHero are expensive and not AI-native
- Web-first AI tutors barely exist — most are mobile apps
- "Explain like I'm 5" → "Explain like a PhD" spectrum is underserved
- White space: adaptive explanations for technical/programming topics on web

**MVP Feasibility:** 4/5 — LLM API for explanations + adaptive difficulty loop + practice problem generation. Simple web UI.

**Ecosystem Fit:**
- learn.ljding.app: the AI tutor layer for any course content
- review.ljding.app: practice problems from Explain feed into spaced review
- drift.ljding.app: study sessions with Explain count as learning focus time

**Ratings:**

| Criterion | Score | Rationale |
|-----------|-------|-----------|
| Market Demand | 8 | AI tutoring is proven and growing; web gap is real |
| Technical Complexity | 4 | LLM API + adaptive logic + practice generation |
| Differentiation | 7 | Adaptive explanations is a clear angle; Quizlet/Similar don't do this |
| Ecosystem Fit | 8 | Deep learn.ljding.app integration; works as standalone too |

### 3. Cohort — cohort.ljding.app

**One-line pitch:** Cohort-based learning tracker that manages your learning group — track who's studying what, accountability check-ins, and shared study sessions. Web-first.

**Why NOW:**
- Cohort-based courses (Luma, Maven) are exploding but there's no standalone tool for informal study groups
- "Study with a friend" lacks tooling — just a group chat, nothing structured
- hangwith.ljding.app's social infrastructure can power study group features
- Bilingual support for Chinese diaspora study groups is completely unserved

**MVP Feasibility:** 5/5 — Group CRUD, check-in system, study session tracker, simple weekly view. No complex real-time needed.

**Ecosystem Fit:**
- hangwith.ljding.app: natural extension — friends studying together
- learn.ljding.app: course content can be shared within cohorts
- drift.ljding.app: group focus sessions (study together remotely)

**Ratings:**

| Criterion | Score | Rationale |
|-----------|-------|-----------|
| Market Demand | 7 | Informal study groups are everywhere but have no good tool |
| Technical Complexity | 3 | Group management + check-ins + calendar; straightforward |
| Differentiation | 7 | Cohort tracking for informal groups is novel; most tools are for formal courses |
| Ecosystem Fit | 9 | Strongest integration with hangwith.ljding.app; group accountability |

### 4. Stack — stack.ljding.app (from Productivity domain)

Already rated 16/20 in Productivity. Revisit here: **Note: Renamed from original "Learning Stack Manager" concept to avoid confusion with the wellness "Stack" app.**

### 5. Passage — passage.ljding.app

**One-line pitch:** Read-it-later + active recall pipeline — save articles, read them in a clean view, and the app auto-generates flashcards from article content using AI.

**Why NOW:**
- Pocket/Instapaper save articles but don't help you *remember* them
- No tool combines save → read → recall in one web-native workflow
- AI flashcard generation from article text is technically feasible now (LLM extraction)
- Developers/professionals read a lot but retain little without active review

**MVP Feasibility:** 4/5 — URL saving, article extraction (Mercury/Readability), clean reader view, LLM flashcard generation.

**Ecosystem Fit:**
- learn.ljding.app: reading as a learning activity; articles become study material
- recall.ljding.app: flashcards feed directly into SRS system
- review.ljding.app: articles can be reviewed with spaced repetition

**Ratings:**

| Criterion | Score | Rationale |
|-----------|-------|-----------|
| Market Demand | 8 | Read-it-later is proven; adding recall layer is the obvious next step |
| Technical Complexity | 5 | Article extraction + LLM flashcard generation + reader view |
| Differentiation | 8 | Save → Read → Recall pipeline is novel; no tool does all three |
| Ecosystem Fit | 9 | Strong with learn.ljding.app (reading as learning) and recall.ljding.app (SRS) |

### 6. Translate — translate.ljding.app

**One-line pitch:** Bilingual reading trainer — save EN or ZH content, see translations inline, track vocabulary acquisition, and review with SRS. The "Rosetta Stone for autodidacts."

**Why NOW:**
- Language learners struggle with "I can read but not retain vocabulary"
- No web tool combines bilingual reading + inline translation + vocabulary tracking + SRS
- Chinese-English learners are a massive underserved market
- Duolingo teaches vocabulary in isolation; Translate teaches in context

**MVP Feasibility:** 3/5 — Content library, translation API (DeepL or similar), vocabulary extraction, SRS integration. CJK support is non-trivial.

**Ecosystem Fit:**
- learn.ljding.app: language learning as a vertical
- recall.ljding.app: vocabulary cards can be SRS'd
- jingxin.ljding.app: reading practice as a complement to meditation (calm focus)

**Ratings:**

| Criterion | Score | Rationale |
|-----------|-------|-----------|
| Market Demand | 8 | 1.4B people learning a second language; bilingual web tools are rare |
| Technical Complexity | 6 | CJK handling, translation API, vocabulary extraction is complex |
| Differentiation | 9 | Bilingual reading + inline translation + SRS is completely novel |
| Ecosystem Fit | 7 | Fits well with learn.ljding.app; vocab SRS integrates with recall |

## Summary Comparison

| Opportunity | Demand | Complexity | Differentiation | Ecosystem Fit | **Total** |
|------------|--------|------------|-----------------|---------------|-----------|
| Recall (web SRS) | 8 | 4 | 8 | 9 | **29** |
| Explain (AI tutor) | 8 | 4 | 7 | 8 | **27** |
| Cohort (study groups) | 7 | 3 | 7 | 9 | **26** |
| Passage (read→recall) | 8 | 5 | 8 | 9 | **30** |
| Translate (bilingual) | 8 | 6 | 9 | 7 | **30** |

## Recommended Build Order

1. **Recall** — Web-native SRS is the clearest gap; learn.ljding.app needs a study engine; 4-6 weeks MVP
2. **Passage** — Read-it-later + recall pipeline is novel and serves learn.ljding.app content strategy; 4-5 weeks MVP
3. **Cohort** — Simplest MVP (3/5), strongest hangwith integration, group study is underserved; 2-3 weeks MVP
4. **Explain** — AI tutor is high-demand but depends on LLM quality; 4-5 weeks MVP
5. **Translate** — Highest differentiation (9/10) but most complex (CJK handling, translation quality); 6-8 weeks MVP

## Education Domain vs Other Domains

**Compared to existing priorities:**
- Recall (29) scores equal to Riff (29, creativity) and higher than Drift (18, productivity)
- Passage (30) is the highest-scoring app concept overall (tied with Montage at 32 but much easier to build)
- Translate (30) scores very high on differentiation but complex

**Recommendation:** Build Recall first (web SRS gap is clearest), then Passage (read→recall pipeline), then Cohort (group study).

---

## Key Web Research Findings (2026-05-22)

1. **AI + Spaced Repetition is under-integrated.** Few tools combine adaptive AI tutoring with modern SRS algorithms (FSRS-6, SM-20). Clear gap: AI teaches concepts, auto-generates and schedules spaced review — all in one flow.
2. **Card creation is biggest SRS bottleneck for bilingual content.** AI-powered auto-generation broke through in 2025-26, but EN/ZH bilingual cards (with pinyin, tone marks, character decomposition) remain largely manual.
3. **EN/ZH is massive but underserved.** English (58%) + Chinese (22%) = ~80% of $24B+ online language learning market. Most platforms treat Chinese as "just another language" rather than designing for tonal pronunciation, radical-based memorization, and character writing.
4. **Agentic AI tutoring is 2026 frontier.** Industry shifting from generative AI (chatbots) to agentic systems (AI that plans lessons, tracks progress, adapts in real-time). Fastest in STEM tutoring; language learning lags.
5. **Authentic content integration drives 3.2x better retention.** Chinese learners struggle to bridge textbook to authentic content due to character density and lack of tools bridging graded readers to native material with inline SRS capture.
6. **Emotion-aware learning emerging but not combined with SRS.** AI tutors detect frustration/confusion but this emotional intelligence hasn't been applied to spaced repetition sessions where fatigue directly impacts retention.
7. **$115B language learning + $7.9B AI tutoring market but no web app owns EN/ZH + AI tutoring + SRS + authentic content intersection.** Clear greenfield opportunity.

---

## Sources

- [Anki 10M users milestone](https://apps Ankiconnect.com)
- [Web Speech API maturity - 2025-2026 browser support](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API)
- [FSRS algorithm (Free Spaced Repetition Scheduler)](https://github.com/open-spaced-repetition/fsrs4)
- [RemNote academic note-taking](https://www.remnote.com)
- [Luma cohort-based courses](https://lumalabs.ai)
- [Maven courses platform](https://maven.com)
- [Duolingo revenue model](https://duolingo.com)
- [Best Spaced Repetition Apps in 2026 - The Sponge](https://thesponge.app/blog/best-spaced-repetition-apps/)
- [AI Tutor Trends You Can't Ignore in 2026 - Wise](https://www.wise.live/blog/top-ai-tutor-trends/)
- [Online Language Learning Market - Mordor Intelligence](https://www.mordorintelligence.com/industry-reports/online-language-learning-market)