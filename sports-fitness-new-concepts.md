# Sports & Fitness Domain Research — 2026-06-07

## Market Landscape

### Web-First Fitness: A Massive Gap

The fitness tracking ecosystem in 2026 remains overwhelmingly **mobile-first and wearable-dependent**. Strava, Garmin Connect, Nike Run Club, Fitbod, Hevy, and Strong all require native app installs. No major fitness platform offers a true web-first, browser-native experience. Key observations:

- **Workout logging tools** (Hevy, Strong, Fitbod, JEFIT) are all iOS/Android-only. No web-first strength logger exists with bilingual support.
- **Running trackers** (Strava, Nike Run Club, MapMyRun) depend on phone GPS via native apps or wearable sync. No browser-based alternative.
- **Privacy**: Most fitness apps require accounts, sync to cloud by default, and monetize user health data. A privacy-first, local-storage-first approach is genuinely differentiated.
- **Hybrid fitness** is a $1.2T market in 2026 (McKinsey), with 60%+ of exercisers mixing in-person and digital sessions — yet no tool bridges both in a web-native bilingual format.

### Chinese Diaspora Sports Culture

Chinese diaspora communities in North America maintain strong sporting traditions:

- **Badminton** is the most popular informal sport — recreational clubs exist in every major metro area (SF, LA, NYC, Toronto, Vancouver). Games are organized via WeChat groups with no formal tooling.
- **Basketball** has massive cultural significance — China's CBA league, village basketball (村BA), and diaspora pickup leagues at community centers and parks. Organizing happens via group chats.
- **Table tennis** clubs operate out of community centers, churches, and Chinese cultural associations. Informal but highly engaged.
- **Martial arts** (太极拳, 气功, 武术) — tai chi in parks, wushu schools, qigong practice groups. Cross-generational appeal. No digital practice logging tool exists in any language.
- **Running groups** — diaspora running clubs (often organized via WeChat) for marathons, half-marathons, and casual 5K groups. Strava is used but doesn't serve bilingual needs.

### The Accountability Gap

Research shows 70%+ of successful fitness transformations are linked to social connectivity. Yet:

- **Gym buddy apps** (Fitness Pact, BossAsAService) are English-only, mobile-only, and require native installs.
- **Financial-stakes apps** (StepBet, WayBetter, HealthyWage) use money as motivation but are US-English-only with no bilingual support.
- **WeChat 打卡 groups** are the de facto accountability tool for Chinese diaspora fitness — but WeChat is unstructured, has no progress tracking, and raises privacy concerns.
- **No web-first bilingual fitness accountability tool exists** — this is clear white space.

### Workout Logging Without Wearables

A significant segment of fitness users (bodyweight training, home workouts, martial arts, yoga, outdoor calisthenics) don't use wearables:

- Bodyweight fitness communities (r/bodyweightfitness, calisthenics groups) track progressions manually in spreadsheets or notes apps.
- Voice-first logging (talking your workout log instead of typing) is an emerging UX pattern with no web-native implementation.
- Traditional Chinese movement practices (tai chi forms, qigong sequences) have no digital tracking tool at all.

---

## App Concepts (7 Total)

### 1. 动伴 (DòngBàn) — Workout Accountability Circles

**Subdomain:** dongban.ljding.app

Fitness-specific accountability circles where 3-8 friends check in daily with their workout completions. No wearable required — users manually log workouts (bodyweight, gym, run, martial arts, any movement). Group streaks, progress photos, and weekly summaries create social pressure and celebration. Bilingual EN/ZH interface with culturally-aware encouragement messages. Privacy-first: no GPS tracking, no data sharing, local-first storage with optional group sync.

| Criteria | Score | Rationale |
|----------|:-----:|-----------|
| Feasibility | 5 | Group check-in CRUD + streak tracking + workout logging + invite links. 3-4 week MVP. Proven patterns from 打卡圈. |
| Differentiation | 4 | Fitness-specific version of accountability circles. Bilingual web-first is unique, but category exists (Fitness Pact, StepBet are mobile-only English-only). |
| Monetization | 4 | Free core (3 circles). $5/mo for unlimited circles + progress analytics + photo timeline. Fitness users are proven payers. |
| Domain Fit | 5 | Strongest hangwith.ljding.app integration — workout buddies IS social. Complements 打卡圈 (general habits) and Stack (behavior science). learn.ljding.app for fitness education content. |
| **Total** | **18** | |

### 2. 功夫日记 (GōngFū Rìjì) — Traditional Chinese Movement Practice Tracker

**Subdomain:** gongfu.ljding.app

The only digital practice log for tai chi, qigong, and wushu practitioners. Log sessions with bilingual form names (e.g., "云手 / Cloud Hands"), track time spent per form, record progression through traditional sequences (24-form tai chi → 42-form → 108-form), and journal practice insights. Visual progression map showing mastery of forms. No wearable needed — practice is inherently analog. Integrates bilingual form library with movement descriptions and cultural context.

| Criteria | Score | Rationale |
|----------|:-----:|-----------|
| Feasibility | 4 | Form library + session logging + progression tracking + journal. 4-5 weeks MVP. Content sourcing (bilingual form names, descriptions) is the main effort. |
| Differentiation | 5 | Complete white space. No app — in any language — tracks tai chi/qigong/wushu practice with form-level detail. Bilingual form names bridge generations (grandparent teaching grandchild). |
| Monetization | 4 | Free core (unlimited session logging). $6/mo for form video library + progression analytics + practice streaks + PDF export for instructors. Martial arts practitioners are dedicated and willing to pay for quality tools. |
| Domain Fit | 5 | Strongest cultural fit in the fitness domain. learn.ljding.app integration for martial arts courses. Bilingual form names serve heritage language preservation. Cross-generational appeal (grandparents → grandchildren). |
| **Total** | **18** | |

### 3. 球局 (QiúJú) — Pickup Game Organizer for Diaspora Sports

**Subdomain:** qiuju.ljding.app

Replaces WeChat group chaos for organizing pickup games. Post a game (badminton at Sunnyvale Community Center, Saturday 2pm, need 4 players), RSVP with skill level, get reminders, and log post-game results. Covers badminton, basketball, table tennis, and soccer — the most popular diaspora sports. Court/venue directory with bilingual names. Skill-level matching prevents lopsided games. Post-game stats and friendly leaderboards.

| Criteria | Score | Rationale |
|----------|:-----:|-----------|
| Feasibility | 4 | Game CRUD + RSVP + venue directory + notifications. 4-5 weeks MVP. Venue data is user-contributed (not a data sourcing challenge). |
| Differentiation | 5 | No bilingual pickup game organizer exists. WeChat groups are the current tool — unstructured, no history, no skill matching. Courtbuddy/Playo don't serve Chinese diaspora. |
| Monetization | 3 | Free core (unlimited games + RSVPs). $4/mo for venue premium features + league mode + advanced stats. Lower ceiling but community-driven growth. |
| Domain Fit | 5 | Strongest hangwith.ljding.app integration — in-person sports meetup IS social connection. Natural viral loop (invite friends to play). learn.ljding.app for sport skill courses. |
| **Total** | **17** | |

### 4. 练记 (LiànJì) — Voice-First Workout Logger

**Subdomain:** lianji.ljding.app

Log your workout by talking instead of typing. "Three sets of bench press, 135 pounds, 8 reps" → structured workout log with zero manual entry. Uses Web Speech API for hands-free mid-workout logging. Supports bilingual voice input (EN and ZH). After your workout, review and edit the structured log. Progress charts, PR tracking, and volume analytics — all from voice data. No wearable, no native app — just open the browser and talk.

| Criteria | Score | Rationale |
|----------|:-----:|-----------|
| Feasibility | 4 | Web Speech API + exercise name parsing + set/rep/weight extraction + structured log display. 4-5 weeks MVP. Voice parsing accuracy is the technical challenge. |
| Differentiation | 5 | No voice-first web workout logger exists in any language. Hands-free mid-workout logging is a genuine unmet need. Bilingual voice (EN/ZH exercise names) is completely novel. |
| Monetization | 3 | Free core (unlimited voice logs). $5/mo for AI exercise recognition + custom exercise library + advanced progress reports. Moderate ceiling. |
| Domain Fit | 4 | Complements fitness ecosystem. Less direct hangwith/learn integration than others, but strong standalone utility. Desktop-friendly for post-workout review. |
| **Total** | **16** | |

### 5. 力道 (LìDào) — Bodyweight Fitness Progress Tracker with Skill Trees

**Subdomain:** lidao.ljding.app

A visual skill-tree progression system for bodyweight and calisthenics training. Track your journey from wall push-ups → knee push-ups → full push-ups → diamond → archer → one-arm push-ups. Each movement has a bilingual progression ladder with clear prerequisites. Log reps, sets, and hold times. Visual "skill tree" map shows your overall bodyweight fitness level. No gym, no wearable, no equipment needed — just your body and a browser.

| Criteria | Score | Rationale |
|----------|:-----:|-----------|
| Feasibility | 5 | Exercise CRUD + progression tree visualization + session logging + charts. 3-4 weeks MVP. SVG skill trees are straightforward. |
| Differentiation | 4 | Skill-tree progression for calisthenics is novel UX. No web-first competitor with bilingual support. But bodyweight tracking apps exist (mobile-only). |
| Monetization | 3 | Free core (basic progression tracking). $4/mo for custom skill trees + video form guides + advanced analytics. Lower ceiling for bodyweight-only audience. |
| Domain Fit | 4 | Complements learn.ljding.app (bodyweight courses). Less direct social integration than others. Desktop-friendly for progression planning. |
| **Total** | **16** | |

### 6. 跑友 (PǎoYǒu) — Web-First Running Log for Phone-Only Runners

**Subdomain:** paoyou.ljding.app

A running tracker that works entirely in the browser — no native app, no smartwatch. Uses Geolocation API for GPS tracking during outdoor runs, with manual entry for treadmill sessions. Bilingual pace display (min/km and min/mi), distance in km/miles, and elevation. Group running challenges with friends. Training plan templates for 5K, 10K, half-marathon. Post-run sharing via hangwith.ljding.app. Designed for runners who refuse to buy a Garmin or Apple Watch.

| Criteria | Score | Rationale |
|----------|:-----:|-----------|
| Feasibility | 3 | Geolocation API for browser GPS tracking works but battery drain and accuracy are inferior to native apps. 5-6 weeks MVP. Background tracking is the hard part. |
| Differentiation | 4 | Web-first running without wearables is differentiated. But Strava dominates running. Bilingual pace/distance is unique but narrow. |
| Monetization | 4 | Free core (basic run logging). $5/mo for training plans + group challenges + analytics. Runners are proven payers (Strava, Runkeeper premium). |
| Domain Fit | 4 | Social running groups via hangwith. learn.ljding.app for running form courses. Less unique ecosystem fit than martial arts or pickup games. |
| **Total** | **15** | |

### 7. 赛季 (SàiJì) — Recreational League Season Manager

**Subdomain:** saiji.ljding.app

Season management tool for diaspora recreational sports leagues. Create a league (Sunday Badminton League — Bay Area Chinese Community), add teams, generate round-robin or bracket schedules, track match results and standings, and display player stats. Bilingual EN/ZH for league communications. Currently, diaspora rec leagues use spreadsheets, WeChat screenshots, and word-of-mouth — SàiJì replaces all of it with a clean web dashboard.

| Criteria | Score | Rationale |
|----------|:-----:|-----------|
| Feasibility | 4 | Season CRUD + schedule generation + standings calculation + stats dashboard. 4-5 weeks MVP. Well-understood web patterns. |
| Differentiation | 5 | No bilingual recreational league management tool exists. Chinese community leagues use WeChat + spreadsheets. LeagueApps/TeamSnap don't serve this audience. |
| Monetization | 3 | Free for small leagues (≤4 teams). $5/mo per league for unlimited teams + advanced stats + season archives. League organizers would pay but TAM is small. |
| Domain Fit | 3 | hangwith.ljding.app integration for league social features. Less direct learn.ljding.app synergy. Niche audience limits cross-ecosystem value. |
| **Total** | **15** | |

---

## Summary Rankings

| Rank | App | Subdomain | Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|------|-----|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 1 | **动伴 (DòngBàn)** — Workout accountability circles | dongban.ljding.app | 5 | 4 | 4 | 5 | **18** |
| 1 | **功夫日记 (GōngFū Rìjì)** — Traditional movement practice tracker | gongfu.ljding.app | 4 | 5 | 4 | 5 | **18** |
| 3 | **球局 (QiúJú)** — Pickup game organizer | qiuju.ljding.app | 4 | 5 | 3 | 5 | **17** |
| 4 | **练记 (LiànJì)** — Voice-first workout logger | lianji.ljding.app | 4 | 5 | 3 | 4 | **16** |
| 4 | **力道 (LìDào)** — Bodyweight fitness skill trees | lidao.ljding.app | 5 | 4 | 3 | 4 | **16** |
| 6 | **跑友 (PǎoYǒu)** — Web-first running log | paoyou.ljding.app | 3 | 4 | 4 | 4 | **15** |
| 6 | **赛季 (SàiJì)** — Rec league season manager | saiji.ljding.app | 4 | 5 | 3 | 3 | **15** |

## Recommended #1 Build Candidate: 功夫日记 (GōngFū Rìjì)

While 动伴 (DòngBàn) ties at 18/20, **功夫日记 (GōngFū Rìjì)** is the recommended first build because:

1. **Complete white space** — no app in any language tracks tai chi/qigong/wushu practice at the form level. 动伴 has mobile-only competitors (Fitness Pact, StepBet).
2. **Strongest cultural moat** — bilingual form names (云手 / Cloud Hands) serve heritage language preservation, a core ecosystem value.
3. **Cross-generational appeal** — grandparents practicing tai chi in the park can share progression with grandchildren learning wushu, bridging the generation gap.
4. **No wearable dependency** — traditional movement practice is inherently analog; this app serves users who will never buy a Garmin.
5. **learn.ljding.app synergy** — martial arts courses, movement tutorials, and cultural history content create a natural educational bridge.

### Recommended Build Order (Sports & Fitness Domain)

1. **功夫日记 (GōngFū Rìjì)** — Complete white space, strongest cultural moat, 4-5 week MVP
2. **动伴 (DòngBàn)** — Highest feasibility (3-4 weeks), proven accountability model, fitness-specific 打卡圈
3. **球局 (QiúJú)** — In-person meetup organizer, strongest hangwith integration, 4-5 weeks
4. **力道 (LìDào)** — Simplest MVP (3-4 weeks), bodyweight-only audience, visual skill trees
5. **练记 (LiànJì)** — Voice-first is novel but Web Speech accuracy is a risk, 4-5 weeks
6. **跑友 (PǎoYǒu)** — Browser GPS limitations vs native apps, 5-6 weeks, Strava competition
7. **赛季 (SàiJì)** — Niche audience (league organizers), 4-5 weeks, build after QiúJú validates sports community

---

## Sources

- [Best Fitness Tracking Apps 2026 — FitBudd](https://www.fitbudd.com/post/the-best-fitness-tracking-apps-for-2026-free-mobile-wearable-compatible)
- [11 Best Workout Accountability Apps & Tools 2026](https://bossasaservice.com/blog/workout-accountability-app/)
- [Best Fitness Apps for Groups — FitBudd](https://www.fitbudd.com/post/best-app-for-fitness-challenges-guide)
- [Why Basketball is So Popular in China — YoyoChinese](https://yoyochinese.com/blog/learn-mandarin-chinese-china-sport-culture-basketball-popularity-in-china)
- [Sports in China — Wikipedia](https://en.wikipedia.org/wiki/Sport_in_China)
- [Chin Woo Athletic Associations — Taylor & Francis](https://www.tandfonline.com/doi/full/10.1080/09523367.2025.2596045)
