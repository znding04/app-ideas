# News/RSS Domain — App Concepts for ljding.app

**Domain:** News & Content Aggregation for Chinese-American Diaspora
**Session:** 30 (2026-06-19)
**Author:** Hermes Agent (cron job)
**Context:** Ecosystem: learn.ljding.app, hangwith.ljding.app | Stack: Vue 3 + Vite + TailwindCSS + Cloudflare Workers/D1

---

## Concept 1: 读报 (DúBào) — Bilingual News Dashboard for Diaspora Readers

**Subdomain:** dubao.ljding.app

**One-line pitch:** A privacy-first bilingual (EN/ZH) news aggregator that unifies Chinese and English sources in a single, no-account reading interface.

**MVP Scope:**
- RSS feed subscription manager with OPML import
- Bilingual source directory: curated EN and ZH sources organized by topic
- Unified timeline in chronological order
- Article card: headline, source, thumbnail, estimated read time, EN/ZH language indicator
- Read progress tracking (articles started vs. completed)
- No account: local IndexedDB storage, optional Cloudflare D1 sync for cross-device
- PWA with offline reading

**Ecosystem Fit:**
- learn.ljding.app: Reading as learning — articles flow into Recall for fact retention
- hangwith.ljding.app: "Share to hangout" sends article to group for async discussion
- Passage: "Send to Passage" for long-form articles worth saving

**Scores:**
| Dimension | Score | Rationale |
|-----------|:-----:|-----------|
| Feasibility | 5/5 | Pure frontend RSS reader with standard fetch APIs. OPML import/export. 3-4 weeks MVP. |
| Differentiation | 5/5 | No bilingual RSS reader exists. All RSS apps are English-only. Genuinely novel. |
| Monetization | 3/5 | Free core. $4/mo cross-device sync. $2/mo analytics. Lower ceiling but RSS power users pay. |
| Domain Fit | 5/5 | Direct learn.ljding.app integration. Privacy-first aligns with ecosystem. |
| **Total** | **18** | |

---

## Concept 2: 观点 (GuānDiǎn) — Cross-Border Opinion Aggregator

**Subdomain:** guandian.ljding.app

**One-line pitch:** See how the same story is covered differently in Chinese and English media — a media literacy tool showing EN vs. ZH coverage side-by-side.

**MVP Scope:**
- Story detection: significant stories appearing in both EN and ZH sources are surfaced
- Side-by-side view: EN article left, ZH article right (stacked on mobile)
- AI perspective summary: one-sentence framing comparison from each source
- Bias indicator: source editorial leanings labeled (not judged)
- Reading tracker: log which perspectives you consume
- Bilingual topic tagging: topics labeled in both EN and ZH

**Ecosystem Fit:**
- learn.ljding.app: Media literacy module — "how to read Chinese and US news critically"
- hangwith.ljding.app: Share perspective comparisons with family groups
- MindWeave: Articles tagged and linked by topic, building a perspective graph

**Scores:**
| Dimension | Score | Rationale |
|-----------|:-----:|-----------|
| Feasibility | 3/5 | AI summarization + news API + ZH feed parsing. 5-6 weeks. |
| Differentiation | 5/5 | No tool surfaces cross-border perspective bias in structured format. Genuinely novel. |
| Monetization | 4/5 | $5/mo for unlimited comparisons + AI summaries. Free tier (5/day). |
| Domain Fit | 5/5 | Deepest media literacy fit. Directly addresses diaspora-specific need. |
| **Total** | **17** | |

---

## Concept 3: 侨闻 (QiáoWén) — Diaspora News Curation for Chinese-Americans

**Subdomain:** qiaowen.ljding.app

**One-line pitch:** A curated news aggregator for Chinese diaspora — featuring SupChina, ChinaFile, Radii, diaspora newsletters, and translated Chinese state media, with context notes explaining the cultural and political context behind the news.

**MVP Scope:**
- Curated source directory: ~50 EN-language diaspora publications by topic and perspective
- Translated CN headlines: when a significant CN story breaks, show EN coverage + translated CN headline
- Context cards: AI-generated background context ("This is about X — here's why it matters to Chinese Americans")
- Diaspora relevance score: shows whether a story is specifically relevant to diaspora community
- Daily briefing email (optional): morning digest of top diaspora-relevant stories
- Bookmark and share to hangout groups

**Ecosystem Fit:**
- learn.ljding.app: Cultural literacy education — context cards are mini-lessons
- hangwith.ljding.app: Share relevant news to family groups; spark cross-generational discussions
- GuānDiǎn: QiáoWén stories feed into the perspective comparison tool

**Scores:**
| Dimension | Score | Rationale |
|-----------|:-----:|-----------|
| Feasibility | 4/5 | Curated directory + LLM context cards + email API. 4-5 weeks. |
| Differentiation | 5/5 | No news app specifically curated for Chinese-American diaspora relevance. |
| Monetization | 3/5 | Free core. $4/mo for daily email briefing + offline. Lower ceiling. |
| Domain Fit | 5/5 | Strongest cultural identity fit. Directly serves Chinese-American information needs. |
| **Total** | **17** | |

---

## Concept 4: 留声 (LiúShēng) — Podcast & Audio News Aggregator with Bilingual Subtitles

**Subdomain:** liusheng.ljding.app

**One-line pitch:** A bilingual podcast/audio aggregator for Chinese diaspora — discover EN and ZH podcasts, read AI-generated bilingual transcripts, and track audio learning consumption across both languages.

**MVP Scope:**
- Podcast directory with EN and ZH categories
- Audio player with speed control and sleep timer
- AI-generated bilingual transcripts (Whisper + translation API)
- Dual-pane transcript display (EN above ZH, or toggle mode)
- Listening history and progress tracking
- Subscription management with OPML export
- Episode notes with key term bilingual glossary
- PWA for mobile listening

**Ecosystem Fit:**
- learn.ljding.app: Audio learning — podcasts as educational content with transcript support
- TīngPǔ (from music domain): Shares audio processing pipeline
- Passage: Long-form audio articles can be sent to Passage for reading later

**Scores:**
| Dimension | Score | Rationale |
|-----------|:-----:|-----------|
| Feasibility | 3/5 | Audio player straightforward. AI transcripts add cost/latency. 5-6 weeks. |
| Differentiation | 5/5 | No bilingual podcast aggregator with dual-pane transcripts exists. |
| Monetization | 4/5 | Free tier (basic player). $6/mo for unlimited transcripts + offline. |
| Domain Fit | 4/5 | Complements learn.ljding.app audio learning. Heritage language angle. |
| **Total** | **16** | |

---

## Concept 5: 过滤 (GuòLǜ) — Privacy-First News Reader with Reading Analytics

**Subdomain:** guolv.ljding.app

**One-line pitch:** A local-first, no-account news reader with built-in reading analytics — see how much you read, what topics dominate your consumption, and get gentle nudges toward a more balanced information diet.

**MVP Scope:**
- RSS/Atom feed subscription with OPML import
- Unified reading list sorted by recency
- Clean article reader view (no ads, no tracking pixels)
- Reading analytics: time per article, topics read, balance score
- "Reading nudges": gentle prompts when feed is heavily skewed (e.g., "8 political articles today — maybe explore culture?")
- Bilingual topic labels (EN + ZH)
- No account: local IndexedDB storage, optional E2E encrypted sync
- PWA for offline reading

**Ecosystem Fit:**
- learn.ljding.app: Reading habit tracking as meta-learning skill
- Radar (burnout detection): Reading patterns could signal information overload
- MindWeave: Articles tagged and linked to build personal knowledge graph

**Scores:**
| Dimension | Score | Rationale |
|-----------|:-----:|-----------|
| Feasibility | 5/5 | Standard RSS patterns. Analytics is rule-based (keyword matching). 3-4 weeks. |
| Differentiation | 4/5 | Privacy-first + reading analytics + information diet nudges is novel combination. |
| Monetization | 3/5 | Free core. $3/mo for cross-device encrypted sync. Lower ceiling. |
| Domain Fit | 4/5 | Strong learn.ljding.app integration. Complements other reading apps. |
| **Total** | **16** | |

---

## Summary Scoring Table

| Rank | App | Subdomain | Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|------|-----|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 1 | **读报 (DúBào)** | dubao.ljding.app | 5 | 5 | 3 | 5 | **18** |
| 2 | **观点 (GuānDiǎn)** | guandian.ljding.app | 3 | 5 | 4 | 5 | **17** |
| 2 | **侨闻 (QiáoWén)** | qiaowen.ljding.app | 4 | 5 | 3 | 5 | **17** |
| 4 | **留声 (LiúShēng)** | liusheng.ljding.app | 3 | 5 | 4 | 4 | **16** |
| 4 | **过滤 (GuòLǜ)** | guolv.ljding.app | 5 | 4 | 3 | 4 | **16** |

---

## Recommended Build Order

1. **读报 (DúBào)** — Highest score (18), highest feasibility (5/5), 3-4 weeks MVP. Establishes reading infrastructure for ecosystem. Bilingual RSS reader is foundational.

2. **侨闻 (QiáoWén)** — Highest diaspora differentiation (5/5). Context cards are killer feature. 4-5 weeks. Best cultural fit for Chinese-American identity.

3. **过滤 (GuòLǜ)** — High feasibility (5/5), 3-4 weeks. Reading analytics + information diet nudges differentiates from DúBào. Best for learn.ljding.app meta-learning angle.

4. **观点 (GuānDiǎn)** — Highest conceptual differentiation but most complex (5-6 weeks). Build after reading infrastructure is established.

5. **留声 (LiúShēng)** — Audio shares infrastructure with TīngPǔ (music domain). Build after audio domain is validated.

---

## Cross-Ecosystem Synergies

- **DúBào → Passage**: Articles worth saving flow to Passage for read-it-later + recall pipeline
- **DúBào → Recall**: Key facts from articles flow into SRS for retention
- **DúBào → GuòLǜ**: Share reading infrastructure; DúBào the reader, GuòLǜ the analytics layer
- **QiáoWén → learn.ljding.app**: Context cards as mini-lessons; cultural literacy education
- **QiáoWén → GuānDiǎn**: QiáoWén stories feed into perspective comparison
- **QiáoWén → hangwith.ljding.app**: Share relevant news to family groups
- **GuòLǜ → Radar**: Reading overload patterns feed into burnout detection
- **LiúShēng → TīngPǔ**: Shared audio processing pipeline (Whisper transcription)
