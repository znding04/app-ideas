# News/RSS Domain — Research Brief for ljding.app

## Domain: News & Content Aggregation for Chinese-American Diaspora

### Market Context

**Global news app market:** ~$8.2B (2025), growing at 6-8% CAGR. Key trends:
- AI-powered personalized news curation
- Cross-border content access tools (VPN-adjacent)
- Bilingual content consumption (growing demand for immigrant communities)
- RSS/reader apps experiencing renaissance among power users and privacy-conscious readers

**Diaspora-specific pain points:**
1. **Language isolation** — Second-gen Chinese Americans often consume English news but parents need Chinese-language content; no unified tool bridges both
2. **Cross-border content access** — WeChat articles, Chinese news sites, and diaspora publications often block or throttle non-China IPs
3. **Bilingual reading tracking** — No tool tracks what you read in both languages and surfaces patterns
4. **Diaspora publications scattered** — SupChina, ChinaFile, The China Project, Radii, various diaspora newsletters exist but are siloed
5. **Filter bubble risk** — Chinese diaspora vulnerable to both Chinese state media AND English-language misinformation about China

### Key Market Gaps

| Gap | Problem | Opportunity |
|-----|---------|-------------|
| Bilingual news aggregation | No tool combines EN + ZH news in one interface | Unified reading dashboard |
| Cross-border content access | Chinese publications behind China IP blocks | Read-it-later for diaspora content |
| Diaspora-specific curation | Mainstream news apps don't understand diaspora relevance | Cultural relevance scoring |
| Privacy-first reading | Google News / Apple News require accounts | Local-first reader with no tracking |
| Reading analytics | People want to track what they consume | Reading habit insights for lifelong learners |

### Ecosystem Fit

- **learn.ljding.app**: Reading is a core learning activity. News/RSS feeds into learn's content consumption tracking.
- **hangwith.ljding.app**: Share interesting articles with friends/family groups. "Read this together" async discussion.
- **Privacy-first values**: No-account, local-first reading app aligns with ecosystem philosophy.

### Differentiation from Existing Ecosystem Apps

The News/RSS domain complements:
- **Passage** (read-it-later + recall pipeline) — Passage is content you save; News/RSS is live feeds you subscribe to
- **Tidbit** (knowledge capture) — Tidbit captures insights; News/RSS feeds the content to be captured from
- **Recall** (spaced repetition) — News/RSS content can flow into Recall for retention of key facts

---

## App Concepts (5)

### 1. 读报 (DúBào) — Bilingual News Dashboard for Diaspora Readers

**Subdomain:** dubao.ljding.app

**One-line pitch:** A privacy-first bilingual (EN/ZH) news aggregator that unified across Chinese and English sources in a single, no-account reading interface.

**Why NOW:**
- Second-gen Chinese Americans want to stay informed about both their host country AND heritage country, but must switch between separate apps
- WeChat article sharing (Chinese content) and Apple News (English content) are completely siloed
- No-account RSS readers (NetNewsWire, Reeder) are popular but English-only; Chinese RSS feeds are largely unknown to diaspora kids raised in the US
- Growing awareness of information diet management among digitally conscious users

**MVP Scope:**
- RSS feed subscription manager with OPML import
- Bilingual source directory: curated EN and ZH sources organized by topic (China news, US politics, tech, culture)
- Unified timeline in chronological order
- Article card shows: headline, source, thumbnail, estimated read time, EN/ZH language indicator
- Read progress tracking (articles started vs. completed)
- No account: local storage for subscriptions, optional Cloudflare D1 sync for cross-device
- PWA with offline reading

**Ecosystem Fit:**
- **learn.ljding.app**: Reading as learning — articles consumed here flow into Recall (spaced repetition) for key fact retention
- **hangwith.ljding.app**: "Share to hangout" button sends article to a group for async discussion
- Passage (read-it-later): "Send to Passage" for long-form articles worth saving

**Feasibility: 5/5** — Pure frontend RSS reader with standard fetch APIs. OPML import/export. Local storage. 3-4 weeks MVP.

**Differentiation: 5/5** — No bilingual RSS reader exists. All RSS apps are English-only. The bilingual reading dashboard with ZH/EN source organization is genuinely novel.

**Monetization: 3/5** — Free core (unlimited feeds, no account). $4/mo for cross-device cloud sync + offline reading. $2/mo for read analytics dashboard. Lower ceiling but RSS power users accept paid tiers.

**Domain Fit: 5/5** — Direct learn.ljding.app integration (reading as learning). Privacy-first aligns with ecosystem. Complements Passage + Recall pipeline.

**Total Score: 18/20**

---

### 2. 观点 (GuānDiǎn) — Cross-Border Opinion Aggregator

**Subdomain:** guandian.ljding.app

**One-line pitch:** See how the same story is covered differently in Chinese and English media — a media literacy tool that surfaces perspective bias by showing EN vs. ZH coverage side-by-side.

**Why NOW:**
- Chinese diaspora are caught between two information ecosystems — US media often covers China through a geopolitical lens; Chinese state media covers the US differently
- No tool helps readers see "both sides" of a story in a structured way
- Growing media literacy awareness; second-gen Chinese Americans increasingly skeptical of both US and CN media narratives
- Misinformation about China (and about the US, from CN media) is a genuine problem for diaspora communities

**MVP Scope:**
- Story detection: when a significant story appears in both EN and ZH sources, surface it
- Side-by-side view: EN article on left, ZH article on right (or stacked on mobile)
- Perspective summary: AI-generated one-sentence summary of how each source frames the story
- Bias indicator: show source's known editorial leanings (labeled, not judged)
- Reading tracker: log which perspectives you consume
- Bilingual topic tagging: topics labeled in both EN and ZH

**Ecosystem Fit:**
- **learn.ljding.app**: Media literacy education module — "how to read Chinese and US news critically"
- **hangwith.ljding.app**: Share perspective comparisons with family groups; spark cross-generational discussions
- MindWeave (knowledge graph): articles tagged and linked by topic, building a perspective graph

**Feasibility: 3/5** — AI perspective summarization requires LLM API. Story matching across EN/ZH sources requires a news API (NewsAPI or similar). Feed parsing for ZH sources (many don't have RSS) is the hard part. 5-6 weeks MVP.

**Differentiation: 5/5** — No tool surfaces cross-border perspective bias in structured side-by-side format. This is genuinely novel and directly addresses a diaspora-specific need no competitor serves.

**Monetization: 4/5** — $5/mo for unlimited comparisons + AI summaries. Free tier (5 comparisons/day). Higher ceiling than typical reader apps due to AI feature value.

**Domain Fit: 5/5** — Deepest media literacy fit in the ecosystem. learn.ljding.app for critical media consumption education. Unique diaspora-specific angle no other app addresses.

**Total Score: 17/20**

---

### 3. 留声 (LiúShēng) — Podcast & Audio News Aggregator with Bilingual Subtitles

**Subdomain:** liusheng.ljding.app

**One-line pitch:** A bilingual podcast/audio aggregator for Chinese diaspora — discover EN and ZH podcasts, read AI-generated bilingual transcripts, and track your audio learning consumption across both languages.

**Why NOW:**
- Chinese diaspora (especially 1.5-gen) increasingly consume podcasts (EN) but parents listen to Chinese-language audio
- No web-first audio aggregator with bilingual transcript support exists
- Audio content is growing rapidly (podcasts, audiobooks, news radio) but accessibility for non-native speakers is limited
- Second-gen want to listen to heritage language podcasts but lack comprehension support

**MVP Scope:**
- Podcast directory with EN and ZH categories
- Audio player with speed control and sleep timer
- AI-generated bilingual transcripts (Whisper + translation API)
- Transcript displayed in dual-pane (EN above ZH, or toggle mode)
- Listening history and progress tracking
- Subscription management with OPML export
- Episode notes with key term translations (bilingual glossary)
- PWA for mobile listening

**Ecosystem Fit:**
- **learn.ljding.app**: Audio learning — podcasts as educational content with transcript support
- **TīngPǔ (from music domain)**: Shares audio processing pipeline with music domain
- **Passage**: Long-form audio articles can be sent to Passage for reading later

**Feasibility: 3/5** — Audio player is straightforward. AI transcript generation adds cost and latency. Bilingual translation quality control is the challenge. 5-6 weeks MVP.

**Differentiation: 5/5** — No bilingual podcast aggregator with dual-pane transcripts exists. This bridges the heritage language audio gap for second-gen diaspora listeners.

**Monetization: 4/5** — Free tier (basic player, limited transcripts). $6/mo for unlimited transcripts + offline + bilingual glossary. Podcast listeners are engaged and premium-tolerant.

**Domain Fit: 4/5** — Complements learn.ljding.app audio learning. Heritage language learning angle. Less direct social integration than other concepts.

**Total Score: 16/20**

---

### 4. 过滤 (GuòLǜ) — Privacy-First News Reader with Reading Analytics

**Subdomain:** guolv.ljding.app

**One-line pitch:** A local-first, no-account news reader with built-in reading analytics — see how much you read, what topics dominate your consumption, and get gentle nudges toward more balanced information diet.

**Why NOW:**
- Growing awareness of information diet (Dr. Andrew Menditti's work on media consumption psychology)
- Google News and Apple News are free but track everything; privacy-conscious readers want alternatives
- RSS is experiencing a renaissance as people flee algorithm-driven feeds
- No tool helps readers see their OWN reading patterns and biases

**MVP Scope:**
- RSS/Atom feed subscription with OPML import
- Unified reading list sorted by recency
- Article reader view (clean typography, no ads, no tracking pixels)
- Reading analytics: time spent per article, topics read, balance score (topics covered vs. omitted)
- "Reading nudges": gentle prompts when your feed is heavily skewed (e.g., "You read 8 political articles today — maybe explore culture?")
- Bilingual topic labels (EN + ZH)
- No account: local IndexedDB storage, optional E2E encrypted sync
- PWA for offline reading

**Ecosystem Fit:**
- **learn.ljding.app**: Reading habit tracking as meta-learning skill
- **Radar (burnout detection)**: Reading patterns could signal information overload contributing to burnout
- **MindWeave**: Articles can be tagged and linked to build personal knowledge graph

**Feasibility: 5/5** — Standard RSS reader patterns. Analytics engine is simple rule-based (topic classification via keyword matching, not ML). 3-4 weeks MVP — second simplest in domain.

**Differentiation: 4/5** — Privacy-first + reading analytics + information diet nudges is a novel combination. Most RSS readers are feature-identical; the analytics + nudge layer is unique.

**Monetization: 3/5** — Free core (all features). $3/mo for cross-device encrypted sync. Lower ceiling but recurring revenue from privacy-conscious power users.

**Domain Fit: 4/5** — Strong learn.ljding.app integration (reading habits as learning meta-skill). Complements other reading apps. Privacy-first aligns with ecosystem.

**Total Score: 16/20**

---

### 5. 侨闻 (QiáoWén) — Diaspora News Curation for Chinese-Americans

**Subdomain:** qiaowen.ljding.app

**One-line pitch:** A curated news aggregator specifically for Chinese diaspora — featuring SupChina, ChinaFile, Radii, diaspora newsletters, and translated Chinese state media, with context notes that explain the cultural and political context behind the news.

**Why NOW:**
- Chinese diaspora consumers are underserved by mainstream news aggregators which don't understand diaspora relevance
- Publications like SupChina, Radii, The China Project serve this audience but aren't discoverable in mainstream apps
- Second-gen Chinese Americans want to understand China coverage but lack context that first-gen takes for granted
- "Explain the background" is the most requested feature when sharing Chinese news with diaspora audiences

**MVP Scope:**
- Curated source directory: ~50 EN-language diaspora publications organized by topic and perspective
- Translated CN headlines: when a significant CN story breaks, surface EN coverage + translated CN headline
- Context cards: AI-generated background context on stories ("This is about X — here's why it matters to Chinese Americans")
- diaspora relevance score: show whether a story is specifically relevant to diaspora community
- Daily briefing email (optional): morning digest of top diaspora-relevant stories
- Bookmark and share to hangout groups

**Ecosystem Fit:**
- **learn.ljding.app**: Cultural literacy education — context cards are mini-lessons
- **hangwith.ljding.app**: Share relevant news to family groups; spark cross-generational discussions
- **GuānDiǎn (观点)**: QiáoWén stories feed into the perspective comparison tool

**Feasibility: 4/5** — Curated directory (no RSS scraping complexity). Context card generation uses LLM. Daily briefing is standard email API (Mailgun/SendGrid). 4-5 weeks MVP.

**Differentiation: 5/5** — No news app is specifically curated for Chinese-American diaspora relevance. The context card feature ("explain why this matters") is completely novel and directly addresses a real pain point.

**Monetization: 3/5** — Free core (curated feeds + context cards). $4/mo for daily email briefing + offline reading. Lower ceiling but strong loyal audience among diaspora news consumers.

**Domain Fit: 5/5** — Strongest cultural identity fit. Directly serves Chinese-American diaspora information needs. learn.ljding.app for cultural literacy. No other app in ecosystem serves this specific audience.

**Total Score: 17/20**

---

## Feature Comparison

| Feature | Google News | Apple News | NetNewsWire | 读报 DúBào | 侨闻 QiáoWén | 过滤 GuòLǜ |
|---------|:-----------:|:----------:|:-----------:|:-----------:|:------------:|:-----------:|
| No account required | No | No | Yes | **Yes** | **Yes** | **Yes** |
| Bilingual EN/ZH | No | No | No | **Yes** | **Yes** | **Yes** |
| RSS support | No | No | Yes | **Yes** | Partial | **Yes** |
| Reading analytics | No | Limited | No | No | No | **Yes** |
| Diaspora-specific curation | No | No | No | No | **Yes** | No |
| Information diet nudges | No | No | No | No | No | **Yes** |
| Media literacy tools | No | No | No | No | **Yes** | **Yes** |
| Cross-border content access | No | No | No | No | No | No |
| PWA/offline | Limited | Limited | Yes | **Yes** | **Yes** | **Yes** |

---

## Scoring Summary

| Rank | App | Subdomain | Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|------|-----|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 1 | **读报 (DúBào)** | dubao.ljding.app | 5 | 5 | 3 | 5 | **18** |
| 2 | **观点 (GuānDiǎn)** | guandian.ljding.app | 3 | 5 | 4 | 5 | **17** |
| 2 | **侨闻 (QiáoWén)** | qiaowen.ljding.app | 4 | 5 | 3 | 5 | **17** |
| 4 | **留声 (LiúShēng)** | liusheng.ljding.app | 3 | 5 | 4 | 4 | **16** |
| 4 | **过滤 (GuòLǜ)** | guolv.ljding.app | 5 | 4 | 3 | 4 | **16** |

---

## Recommended Build Order

1. **读报 (DúBào)** — Highest score (18), highest feasibility (5/5), fastest MVP (3-4 weeks). Establishes the reading infrastructure for the ecosystem. Bilingual RSS reader is the foundational tool.

2. **侨闻 (QiáoWén)** — Highest differentiation for the diaspora audience (5/5). Context cards are the killer feature. 4-5 weeks. Best cultural fit for Chinese-American identity angle.

3. **过滤 (GuòLǜ)** — Second highest feasibility (5/5), 3-4 weeks. Reading analytics + information diet nudges is a compelling differentiator. Best for the learn.ljding.app meta-learning angle.

4. **观点 (GuānDiǎn)** — Highest conceptual differentiation but most complex to build (5-6 weeks). Best after reading infrastructure is established. Media literacy is a natural extension of the ecosystem's educational mission.

5. **留声 (LiúShēng)** — Audio learning is adjacent to reading but shares infrastructure with TīngPǔ (music domain). Build after audio domain is validated.

---

## Cross-Ecosystem Synergies

- **DúBào → Passage**: Articles worth saving flow to Passage for read-it-later + recall pipeline
- **DúBào → Recall**: Key facts from articles can flow into SRS for retention
- **DúBào → GuòLǜ**: Sharing reading infrastructure; DúBào the reader, GuòLǜ the analytics layer
- **QiáoWén → learn.ljding.app**: Context cards as mini-lessons; cultural literacy education
- **QiáoWén → GuānDiǎn**: QiáoWén stories feed into perspective comparison
- **QiáoWén → hangwith.ljding.app**: Share relevant news to family groups
- **GuòLǜ → Radar**: Reading overload patterns could feed into burnout detection
- **LiúShēng → TīngPǔ**: Shared audio processing pipeline (Whisper transcription)

---

## Why News/RSS for ljding.app?

The ljding.app ecosystem has a strong educational identity (learn.ljding.app). News/RSS is a natural extension — it's reading-as-learning with:

1. **Bilingual reading** — No existing tool serves bilingual EN/ZH consumption in a web-native, privacy-first format
2. **Media literacy** — Chinese diaspora are uniquely exposed to information from two ecosystems; tools that help navigate this are genuinely valuable
3. **Content-to-learning pipeline** — News consumed → facts extracted → Recall SRS → knowledge retained is the complete learning loop
4. **Diaspora-specific relevance** — Chinese-American news consumption patterns (following both countries) are underserved

This domain also positions ljding.app as the "anti-algorithm" reading platform — respecting user attention, privacy, and the desire to consume diverse perspectives intentionally rather than having feeds curated by engagement-maximizing algorithms.
