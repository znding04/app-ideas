# Navigation/Wayfinding Domain — App Concepts (Session 27, 2026-06-16)

## Domain: Navigation / Wayfinding

**Research covered:** 5 market gaps, 6 app concepts
**Session:** 27th domain explored (Navigation/Wayfinding)

---

## Market Gaps

| Gap | Problem | Evidence |
|-----|---------|----------|
| **English-first China navigation** | No English-friendly web navigation for China | Google Maps limited in China, Gaode/Baidu require Chinese |
| **Bilingual local discovery** | No verified bilingual directory of Chinese-speaking businesses | WeChat groups + word of mouth only |
| **Cultural venue database** | Chinese heritage sites not on Google Maps | Found through informal networks only |
| **Shuttle family logistics** | Zero tools for dual-country lifestyle navigation | WeChat/phone is current state |
| **Web-first China trip planning** | All navigation is mobile-first | Trip planning happens on desktop, not phone |

---

## App Concepts

### 1. ChinaWay — chinaway.ljding.app

||| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 4/5 | OSM data + Gaode English API + web interface. 4-5 weeks MVP. No Chinese input required. |
| Differentiation | 5/5 | Zero English-friendly web navigation tools for China. Complete white space. |
| Monetization | 3/5 | $5/mo for offline maps + itinerary sync. Free core covers basic navigation. Lower ceiling. |
| Domain Fit | 5/5 | Strongest travel fit — English speakers visiting China is the core diaspora navigation use case. |
| **Total** | **17** | |

**One-line pitch:** An English-first web navigation tool for getting around China — maps, transit, and business info without needing Chinese.

**Why NOW:** More Chinese Americans visiting China as tourism resumes. Shuttle families need reliable English navigation for China home visits. No English-accessible China map exists that works on desktop.

**MVP scope:** OSM base map + Gaode API English search + turn-by-turn driving/transit + business listing display. No Chinese input needed. PWA that works offline in China with cached tiles. 4-5 weeks.

---

### 2. HuMini — huxiao.ljding.app

||| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 5/5 | Yelp API + bilingual enhancement + crowdsourced bilingual data layer. 3-4 weeks MVP. |
| Differentiation | 4/5 | Bilingual + diaspora-specific service categories (bilingual doctors, Chinese-speaking banks). No direct competitor. |
| Monetization | 3/5 | $4/mo for listing claims + premium categories. Free core covers discovery. Lower monetization ceiling. |
| Domain Fit | 4/5 | Complements roam.ljding.app (China trips) and wander.ljding.app (travel journal). Diaspora neighborhood discovery. |
| **Total** | **16** | |

**One-line pitch:** Find Chinese-speaking doctors, lawyers, banks, and grocery stores in any US city — verified bilingual and listed in English.

**Why NOW:** Growing Chinese-American population in second-tier cities. Second-generation Chinese Americans navigating parent healthcare needs. WeChat referrals are unverified and non-transparent.

**MVP scope:** Yelp API integration + bilingual business enhancement + category filters for Chinese-speaking providers + map interface + community reviews. 3-4 weeks.

---

### 3. WalkIn — walkin.ljding.app

||| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 4/5 | Place database + crowdsourced contribution + map visualization. Content is the challenge. 4-5 weeks. |
| Differentiation | 5/5 | No crowdsourced Chinese cultural venue database exists. Genuinely novel. |
| Monetization | 3/5 | $3/mo for listing claims + analytics. Ads model possible for venues. Lower ceiling. |
| Domain Fit | 4/5 | learn.ljding.app cultural education integration. Wander (travel journal) includes cultural site visits. |
| **Total** | **16** | |

**One-line pitch:** A curated, crowdsourced database of Chinese cultural venues — temples, heritage sites, museums, community centers — discoverable in both English and Chinese.

**Why NOW:** First-generation parents wanting to share Chinese heritage with second-generation kids have no searchable venue database. Cultural heritage sites are poorly indexed globally.

**MVP scope:** Venue database with EN/ZH names + descriptions + hours + photos + map. Crowdsourced contributions with moderation. Bilingual search. 4-5 weeks.

---

### 4. AroundCN — aroundcn.ljding.app

||| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 4/5 | Trip itinerary builder + cloud sync + mobile PWA. 4-5 weeks MVP. |
| Differentiation | 4/5 | Web-first bilingual China pre-trip planning. No bilingual competitor. |
| Monetization | 3/5 | $4/mo for sync + premium templates (business trip, family visit, solo traveler). Lower ceiling. |
| Domain Fit | 5/5 | Strongest China travel fit. Integrates with ChinaWay (navigation) and Wander (travel journal). |
| **Total** | **16** | |

**One-line pitch:** Plan your China trip itinerary on desktop — bilingual EN/ZH trip planner that syncs to your phone for offline access while in China.

**Why NOW:** Business travelers and families planning China visits need bilingual pre-trip planning that works offline. Google Docs/Sheets is the current workaround. No dedicated tool.

**MVP scope:** Itinerary builder (places + transit + notes) + bilingual place search + export to PDF + PWA sync. 4-5 weeks.

---

### 5. ShuttleNav — shuttlenav.ljding.app

||| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 4/5 | Dual-country service directory + map interface + contractor verification. 4-5 weeks. |
| Differentiation | 4/5 | No dual-country navigation tool. Completely novel category. |
| Monetization | 4/5 | $5/mo premium dual-country features. International families have high willingness to pay. |
| Domain Fit | 3/5 | Specific to shuttle families. Narrower audience but very high cultural resonance for the right users. |
| **Total** | **15** | |

**One-line pitch:** Navigate the "two-country lifestyle" — find trusted contractors, services, and resources near both your US home and China home, in both languages.

**Why NOW:** Shuttle families (maintaining homes in both countries) have zero tooling. Everything is managed via WeChat, phone calls, and personal networks. High frustration = high need.

**MVP scope:** Service directory for both US and China locations + bilingual search + trusted contractor badges + contact info + reviews. 4-5 weeks.

---

### 6. HuWei — huwei.ljding.app

||| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 5/5 | Simple map + place list + filtering + community contributions. 2-3 week MVP. Simplest scope. |
| Differentiation | 4/5 | Maps diaspora community spaces — language exchanges, cultural centers, Chinese community organizations. |
| Monetization | 3/5 | Ads + event promotion + premium city guides. Lower ceiling but community-building potential. |
| Domain Fit | 3/5 | hangwith.ljding.app integration (community events). learn.ljding.app for cultural education. |
| **Total** | **15** | |

**One-line pitch:** Map the diaspora — find nearby Chinese community spaces, cultural events, language exchanges, and heritage meetups wherever you are.

**Why NOW:** Second-generation diaspora kids want to connect with heritage but don't know where. Community spaces exist but aren't discoverable. Language exchange meetups are scattered.

**MVP scope:** Map + place list + community contribution + event listing + bilingual. 2-3 weeks — fastest MVP in domain.

---

## Feature Comparison

| Feature | Google Maps | Baidu/Gaode | Yelp | ChinaWay | HuMini | WalkIn | AroundCN |
|---------|:-----------:|:-----------:|:----:|:--------:|:------:|:------:|:--------:|
| English navigation in China | Limited | No (CN) | No | **Yes** | No | No | No |
| Bilingual EN/ZH | No | No | No | **Yes** | **Yes** | **Yes** | **Yes** |
| Web-first PWA | Yes | No | Yes | **Yes** | **Yes** | **Yes** | **Yes** |
| Cultural venue database | Partial | Yes | No | No | No | **Yes** | No |
| China trip pre-planning | No | Yes | No | No | No | No | **Yes** |
| Dual-country lifestyle | No | No | No | No | No | No | No | **Yes** |
| Chinese-speaking business directory | No | Yes | Partial | No | **Yes** | No | No |

---

## Recommended Build Order

1. **ChinaWay** — Highest differentiation (complete white space), strongest travel fit, 4-5 weeks. Builds the China navigation authority brand.
2. **AroundCN** — Complements ChinaWay (pre-trip planning + navigation), bilingual EN/ZH, 4-5 weeks. Natural companion to ChinaWay.
3. **WalkIn** — Cultural venue database, strong learn.ljding.app integration, 4-5 weeks. Content-driven, no complex APIs.
4. **HuMini** — Fastest MVP (3-4 weeks), broadest appeal, diaspora neighborhood discovery.
5. **ShuttleNav** — Most culturally specific, serves the shuttle family niche well, 4-5 weeks.
6. **HuWei** — Fastest MVP (2-3 weeks), community-building angle, best as a hangwith.ljding.app feature extension.

---

## Cross-Ecosystem Synergies

- ChinaWay → AroundCN: Navigate → Plan (China trip lifecycle)
- AroundCN → Wander (ljding.app): Plan → Remember (travel journal)
- HuMini → Roam: Local discovery → Trip planning
- WalkIn → learn.ljding.app: Cultural venue discovery → Heritage education courses
- ShuttleNav → ZhǎoGōng (home services): Service discovery in both countries
- HuWei → hangwith.ljding.app: Community spaces → Social event coordination

---

## Next Domain to Explore

Suggested domains for future sessions:
- **News/RSS** — content aggregation, reading tracking, bilingual news
- **Photo/Image** — photo organization, sharing, Chinese family photo albums
- **Card Games / Board Games** — multiplayer gaming with Chinese heritage
- **Gift Giving** — gift tracking, wishlists, occasion management for diaspora families
- **Navigation/Wayfinding** — see above (this session)
