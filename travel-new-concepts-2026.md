# Travel & Trip Planning — New App Concepts (2026)

**Date:** 2026-05-29
**Domain:** Travel & Trip Planning
**Ecosystem:** ljding.app (learn.ljding.app, hangwith.ljding.app)

---

## App Concepts

### 1. Roam — Content-to-itinerary converter
**Subdomain:** roam.ljding.app

Turn travel inspiration into actionable plans. Paste a URL from Xiaohongshu, TikTok, or YouTube and AI extracts places, timings, and tips into a structured itinerary. Browse and fork community-shared templates by destination, adapt them for your dates/budget/pace/group size, and export bilingual EN/ZH itineraries to Calendar, PDF, or shareable link.

### 2. Trip — Collaborative group trip planner
**Subdomain:** trip.ljding.app

Group trip planning that actually works. Real-time multiplayer itinerary editing with group decision tools (vote on destinations, preference matching), schedule alignment across time zones, smart shared packing lists, budget tracker with currency conversion, and offline PWA mode. Strongest ecosystem integration with hangwith.ljding.app for friend group imports and trip invitations.

### 3. Wander — Private travel journal and memory keeper
**Subdomain:** wander.ljding.app

A privacy-first travel journal. Automatic trip timelines from photo EXIF data, check-ins, and notes. All content encrypted and private by default. Personal travel map visualization, trip stats (countries, distance, cuisines), and selective sharing via hangwith.ljding.app. Memory prompts surface "on this day last year" nostalgia.

---

## Scoring

Scoring: 1-5 per category (5 = best), max total = 20

| Rank | App | Subdomain | Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|------|-----|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 1 | **Roam** — Content-to-itinerary converter | roam.ljding.app | 4 | 5 | 3 | 5 | **17** |
| 2 | **Trip** — Collaborative group trip planner | trip.ljding.app | 3 | 4 | 4 | 5 | **16** |
| 2 | **Wander** — Private travel journal | wander.ljding.app | 5 | 4 | 3 | 4 | **16** |

---

## Scoring Rationale

### Roam (17/20) — Recommended #1 Travel App
- **Feasibility 4/5**: MVP complexity is low (2/5) — core is LLM-powered content parsing + template display, no real-time collaboration needed. Main challenge is reliable extraction from diverse sources (Xiaohongshu, YouTube). Similar to Passage's URL extraction complexity. ~3-4 weeks MVP.
- **Differentiation 5/5**: No tool converts social media travel content into structured itineraries. Bridges the inspiration-to-plan gap that no current tool addresses. Bilingual CN/EN focus for diaspora travelers is genuine white space. Community templates create network effects.
- **Monetization 3/5**: Free core (URL-to-itinerary conversion). Premium templates + advanced adaptation + calendar export for $5/mo. Moderate ceiling — conversion tool expected to be free at core.
- **Domain Fit 5/5**: Feeds into trip.ljding.app for collaborative refinement. learn.ljding.app provides destination language prep. Content templates shared through hangwith.ljding.app social graph. Validates travel category interest before investing in harder trip.ljding.app.

### Trip (16/20)
- **Feasibility 3/5**: Real-time multiplayer editing via Cloudflare Durable Objects, offline sync with conflict resolution, map integration (Mapbox GL JS). Most complex piece is offline sync. 6-8 weeks for full MVP.
- **Differentiation 4/5**: Group-first approach (not single-user with sharing bolted on) is differentiated. Wanderlog exists but is mobile-app-first. Web-native + bilingual + privacy-first adds value, but collaborative planning is not a completely novel category.
- **Monetization 4/5**: $6/mo for unlimited trips + offline mode + budget analytics. Group features drive organic upgrades (one member pays, group benefits). Travel users are willing to pay for coordination tools.
- **Domain Fit 5/5**: Strongest hangwith.ljding.app integration — pull friend groups directly, suggest trips based on shared interests. learn.ljding.app hosts travel language/culture modules. Shared identity system across ljding.app ecosystem.

### Wander (16/20)
- **Feasibility 5/5**: Core is a CRUD app with photo upload (Cloudflare R2), EXIF parsing, and map visualization. No real-time collaboration needed. MVP complexity 2/5. ~3-4 weeks MVP.
- **Differentiation 4/5**: Privacy-first encrypted journal is genuinely differentiated from social photo sharing (Google Photos, Instagram). Web-native with no app lock-in. But travel journaling is a more crowded category than content conversion or group planning.
- **Monetization 3/5**: Free core (trip creation + photos + map). $5/mo for cloud backup + advanced stats + cross-device sync. Journal apps have a lower monetization ceiling — users expect basic journaling to be free.
- **Domain Fit 4/5**: Complements trip.ljding.app (plan before, journal during/after — completes the travel lifecycle). Selective sharing via hangwith.ljding.app. Travel patterns could inform learn.ljding.app recommendations. Less direct integration than Roam or Trip.
