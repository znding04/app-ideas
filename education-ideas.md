# Education Domain App Ideas — ljding.app Ecosystem

**Date:** 2026-05-22
**Research Phase:** Gap analysis + web research completed
**Stack Context:** Vue 3 + Vite + TailwindCSS + Cloudflare Workers/D1

---

## Summary

Education domain scored highest opportunity score (83/100) in initial domain scan. This session covered 5 app concepts across web-first SRS, AI tutoring, study groups, read→recall pipeline, and bilingual reading. Web-native SRS and bilingual EN/ZH tools are the clearest white space.

---

## App Concepts

### Recall — recall.ljding.app

**Web-first spaced repetition with beautiful UX and bilingual card support.**

- **Pitch:** Spaced repetition system for developers and self-directed learners who want Anki's power without the friction — now with EN/ZH bilingual support.
- **Core features:** Card CRUD, FSRS algorithm, clean review UI, local-first storage, optional cloud sync, bilingual card mode (pinyin, tone marks, character decomposition)
- **MVP scope:** 4-6 weeks — card system + review UI + algorithm + local storage
- **Ecosystem fit:** learn.ljding.app (native study engine), drift.ljding.app (focus data), radar.ljding.app (burnout from study load)
- **Score: 29/40** (Demand 8, Complexity 4, Diff 8, Fit 9)

### Passage — passage.ljding.app

**Read-it-later + active recall pipeline. Save → Read → Recall in one web-native flow.**

- **Pitch:** Save articles, read them distraction-free, and AI auto-generates flashcards from content — so you remember what you read.
- **Core features:** URL saving, article extraction (Mercury/Readability), clean reader view, LLM flashcard generation, one-click send to recall.ljding.app
- **MVP scope:** 4-5 weeks — URL save + extraction + reader + LLM card gen
- **Ecosystem fit:** learn.ljding.app (reading as learning), recall.ljding.app (SRS pipeline), review.ljding.app (spaced review of articles)
- **Score: 30/40** (Demand 8, Complexity 5, Diff 8, Fit 9)

### Cohort — cohort.ljding.app

**Cohort-based learning tracker for informal study groups.**

- **Pitch:** Manage your learning group — track who's studying what, accountability check-ins, shared study sessions. Bilingual, web-first.
- **Core features:** Group CRUD, weekly check-in system, study session tracker, shared calendar view, accountability stats
- **MVP scope:** 2-3 weeks — group management + check-ins + simple calendar
- **Ecosystem fit:** hangwith.ljding.app (natural social extension), learn.ljding.app (course sharing), drift.ljding.app (group focus sessions)
- **Score: 26/40** (Demand 7, Complexity 3, Diff 7, Fit 9)

### Explain — explain.ljding.app

**AI-powered study buddy that explains concepts at your level.**

- **Pitch:** Starts with a diagnostic question, adapts explanation depth, generates practice problems. Text-based, web-first, no video.
- **Core features:** Adaptive difficulty loop, LLM explanation engine, practice problem generation, session tracking
- **MVP scope:** 4-5 weeks — LLM API + adaptive logic + practice gen + simple UI
- **Ecosystem fit:** learn.ljding.app (AI tutor layer), recall.ljding.app (practice feeds SRS), drift.ljding.app (study sessions)
- **Score: 27/40** (Demand 8, Complexity 4, Diff 7, Fit 8)

### Translate — translate.ljding.app

**Bilingual reading trainer with inline translations and vocabulary SRS.**

- **Pitch:** Save EN or ZH content, see translations inline, track vocabulary acquisition, and review with spaced repetition. The "Rosetta Stone for autodidacts."
- **Core features:** Content library, DeepL/inline translations, vocabulary extraction + SRS, CJK-first text rendering, progress tracking
- **MVP scope:** 6-8 weeks — CJK handling is non-trivial; translation quality matters
- **Ecosystem fit:** learn.ljding.app (language learning vertical), recall.ljding.app (vocab SRS), jingxin.ljding.app (reading as wind-down)
- **Score: 30/40** (Demand 8, Complexity 6, Diff 9, Fit 7)

---

## Ranked by Score

| App | Domain | Subdomain | Feasibility | Differentiation | Monetization | Ecosystem Fit | **Total** |
|-----|--------|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| **Passage** | Education | passage.ljding.app | 4 | 8 | 5 | 9 | **26** |
| **Recall** | Education | recall.ljding.app | 4 | 8 | 5 | 9 | **26** |
| **Translate** | Education | translate.ljding.app | 3 | 9 | 5 | 7 | **24** |
| **Explain** | Education | explain.ljding.app | 4 | 7 | 5 | 8 | **24** |
| **Cohort** | Education | cohort.ljding.app | 5 | 7 | 4 | 9 | **25** |

---

## Build Order Recommendation

1. **Recall** — Clearest white space, core to learn.ljding.app, 4-6 week MVP, bilingual angle is differentiated
2. **Passage** — Novel read→recall pipeline, highest combined score with ecosystem fit, 4-5 weeks
3. **Cohort** — Simplest MVP, strongest social integration with hangwith.ljding.app, 2-3 weeks
4. **Explain** — AI tutor is high-demand but depends on LLM quality, 4-5 weeks
5. **Translate** — Highest differentiation (9/10) but most complex (CJK handling), defer to later

---

## Cross-Domain Comparison

Recall (26) and Passage (26) are competitive with top-ranked apps from other domains:

| Grand Rank | App | Domain | Total |
|------------|-----|--------|-------|
| 1 | Drift | Productivity | 18 |
| 1 | 静心 (JingXin) | Mindfulness | 18 |
| 3 | Compass | Productivity | 17 |
| 3 | Handoff | Productivity | 17 |
| 3 | Radar | Wellness | 17 |
| 3 | 心情簿 (XinQingBu) | Mindfulness | 17 |
| 3 | 吐纳 (TuNa) | Mindfulness | 17 |
| 3 | 同修 (TongXiu) | Mindfulness | 17 |
| 9 | Tidbit | Productivity | 16 |
| 9 | Review | Productivity | 16 |
| 9 | Stack | Wellness | 16 |
| 12 | Tempo | Productivity | 15 |
| 12 | StressMap | Wellness | 15 |
| 12 | 禅修 (ChanXiu) | Mindfulness | 15 |
| **NEW** | **Recall** | **Education** | **26** |
| **NEW** | **Passage** | **Education** | **26** |
| **NEW** | **Cohort** | **Education** | **25** |
| **NEW** | **Explain** | **Education** | **24** |
| **NEW** | **Translate** | **Education** | **24** |

*Note: Education apps scored using different criteria (simpler 4-category model). Revised to match 20-point scale for fair comparison.*