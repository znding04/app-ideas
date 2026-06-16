# PKM / Knowledge Management — New Concepts Session (2026-06-01)

> Domain session #13 — exploring Personal Knowledge Management opportunities for ljding.app
> Prior research: knowledge-research.md (May 2026), productivity-ideas.md (May 2026)

---

## This Session's Focus

PKM / Knowledge Management was already lightly explored in May research. 
This session drills deeper into the specific white space available given:
- learn.ljding.app already exists (structured AI curriculum)
- hangwith.ljding.app exists (social/friendship tracking)
- Productivity domain already has 6 ranked ideas (Drift, Handoff, Compass, etc.)
- Knowledge domain already has a "bilingual web-first PKM" gap identified

**Research question:** What specific PKM sub-niche should we target, given ecosystem context?

---

## Key Research Findings

### Top Opportunity from Web Research: AI-Powered Personal Knowledge Management

**Market data:**
- Global productivity software: $62.5B (2024) → $142.9B by 2030 (14.8% CAGR)
- AI productivity tools: $13.6B (2025) → $17B (2026), 25% CAGR
- AI-driven productivity app funding grew 110%+ in 2024 alone

**Key gap:** Current tools (Notion, Obsidian, Roam) force users into one paradigm. No tool nails AI-powered semantic retrieval across all content sources automatically.

### Prior Knowledge (from knowledge-research.md)

- Note-taking app market: ~$2.5B, 6-8% CAGR
- Open-source stars: AppFlowy (70k), AFFiNE (68k), Siyuan (44k), Logseq (43k)
- **Bilingual CN/EN gap:** Nearly zero dedicated bilingual PKM tools exist
- **Web-first gap:** Most strong open-source PKMs are desktop-first
- **Read-it-later + linking gap:** Wallabag, Pocket lack bidirectional linking

---

## Three App Concepts Generated

### Concept 1: MindWeave — `weave.ljding.app`

**Core value proposition:** Automatically connects the dots across everything you read, watch, highlight, and note — so you rediscover the right knowledge exactly when you need it.

**Top 3 features:**
1. **Auto-ingest pipeline** — Browser extension + API captures highlights from web articles, PDFs, YouTube transcripts, Kindle, Pocket. Each item chunked, embedded, tagged without manual effort.
2. **Contextual resurfacing** — When writing (in app or via extension), AI surfaces related notes, highlights, connections in a sidebar, ranked by semantic relevance.
3. **Knowledge graph explorer** — Visual, interactive graph of your concepts and sources. Click a node to see all fragments; AI generates a "synthesis card" summarizing what you know.

**Target user:** Prolific readers and lifelong learners (researchers, grad students, senior engineers, content creators) who consume 10+ articles/videos per week.

**Differentiation:**
- Notion: blank canvas, no auto-ingest, no semantic linking
- Obsidian: requires manual backlinks; MindWeave auto-links via embeddings
- Readwise/Reader: captures highlights but no cross-linking graph or contextual surfacing
- Mem.ai: AI search but weak ingestion, no visual graph

**Rough tech:** Next.js + Supabase (pgvector) + Claude API + browser extension + react-force-graph

---

### Concept 2: RecallStack — `recall.ljding.app`

**Core value proposition:** Turns your highlights, notes, and bookmarks into automatically generated flashcards so you actually retain what you consume.

**Top 3 features:**
1. **Auto-card generation** — AI reads highlights/notes, generates Q&A cards, cloze deletions, concept-relationship cards. You review and approve, never write from scratch.
2. **Adaptive review sessions** — SM-2+ algorithm with AI-adjusted difficulty. 5-10 minute sessions, mobile-first for commutes/breaks.
3. **Source-linked cards** — Every card links back to original source (article, video timestamp, PDF page).

**Target user:** Professionals and students who read a lot but retain little; Anki users who bounced off manual card creation friction.

**Differentiation:**
- Anki: biggest bottleneck is manual card creation. RecallStack auto-generates.
- RemNote: tries to be both note-taking and SRS — does neither exceptionally. RecallStack is ingestion-first.
- Readwise: resurfaces highlights randomly; RecallStack uses proven SRS scheduling for retention.

**Rough tech:** Next.js + PWA + Supabase + Claude batch API + custom SM-2 client-side

---

### Concept 3: ThreadMap — `threads.ljding.app`

**Core value proposition:** Captures scattered research across tabs, chats, docs into structured "investigation threads" that AI keeps organized and queryable.

**Top 3 features:**
1. **Thread capture** — Start a research thread (e.g., "Evaluate hosting providers"), clip web pages, paste chat snippets, drop screenshots, dictate voice notes. Everything timestamped and auto-summarized.
2. **AI thread digest** — Ask "What have I learned so far?" and get structured summary: key findings, open questions, contradictions across sources.
3. **Thread handoff** — Export as briefing doc (Markdown/PDF) or as prompt-ready context package for Claude/ChatGPT.

**Target user:** Knowledge workers doing investigative research (vendor evaluation, bug diagnosis, competitive analysis, due diligence) who lose context across 30+ tabs and multiple chat sessions.

**Differentiation:**
- Notion: document-centric, not investigation-centric; no "live research thread" concept
- Arc browser Spaces: organizes tabs but doesn't extract/summarize/synthesize content
- ChatGPT/Claude: chats lose context across sessions; ThreadMap persists research and re-enters any AI with full context

**Rough tech:** Next.js + Tailwind + Chrome extension + Supabase (pgvector) + Claude long-context

---

## Recommendation

**Ship MindWeave (weave.ljding.app) first.**

**Rationale:**
1. Broadest appeal — PKM has mass market, not just niche
2. Strongest synergy with learn.ljding.app — courses feed knowledge into personal knowledge base
3. Clear monetization — free tier (limited ingestion) → paid unlimited + AI features
4. Data moat — more you capture, stickier the tool
5. Clear defensible differentiation — auto-linking via embeddings (not manual) is genuinely novel

**Build order within PKM:**
1. MindWeave (broadest, highest retention)
2. RecallStack (SRS proven, natural learn.ljding.app extension)
3. ThreadMap (most novel, most complex)

**Suggested scores for PRIORITIES.md update:**
| App | Feasibility | Differentiation | Monetization | Domain Fit | Total |
|-----|:-----------:|:---------------:|:------------:|:----------:|:------|
| MindWeave | 4 | 5 | 4 | 5 | 18 |
| RecallStack | 4 | 4 | 4 | 5 | 17 |
| ThreadMap | 3 | 5 | 4 | 4 | 16 |
