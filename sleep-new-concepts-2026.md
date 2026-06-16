# Sleep & Recovery — New App Concepts & Scoring

**Date:** 2026-05-26  
**Session Focus:** Sleep & Recovery Domain — scoring and new gap analysis  
**Existing research:** sleep-research.md (2026-05-15)  
**Domain:** Sleep & Recovery  
**Status:** ✅ Researched (2026-05-15), now scored

---

## Fresh Web Research Findings (2026)

### Key Trends Driving Sleep App Opportunity

1. **Sleep anxiety as a distinct category** — Post-pandemic, orthosomnia (sleep perfectionism) is rising. Users fixate on tracker scores and worsen their sleep. Apps that address anxiety-driven insomnia WITHOUT demanding wearable data are growing.

2. **CBT-I goes digital** — Cognitive Behavioral Therapy for Insomnia is now first-line treatment. Digital CBT-I programs (Sleepio, Daybreak Health) show 70%+ success rates. Web-native, bilingual CBT-I is nonexistent.

3. **Web-first sleep tools remain a white space** — Sleep Cycle, AutoSleep, Calm, Headspace are all mobile-native. ~40% of sleep app users research sleep tools on desktop before downloading. No bilingual web-first sleep tool exists.

4. **Sleep + productivity connection gaining traction** — Research shows sleep quality directly affects next-day productivity. Tools that bridge "how I slept" → "what I should focus on today" are emerging (e.g., SleepScore apps connecting to task managers).

5. **Privacy-first sleep data** — 54% of sleep app users worry about data security. Mainland China-hosted apps (蜗牛睡眠, 潮汐) are increasingly avoided by diaspora users. Privacy-first positioning has real value.

---

## Scoring Rationale (Sleep Apps)

### Scoring Rubric
- **Feasibility** (1-5): Technical complexity, MVP timeline
- **Differentiation** (1-5): Unique angle, competitive landscape
- **Monetization** (1-5): Business model strength, price sensitivity
- **Domain Fit** (1-5): learn.ljding.app + hangwith.ljding.app synergy

---

### DreamDrift (梦漂) — dream.ljding.app (18/20)

**One-line pitch:** Web-first bilingual wind-down companion with ambient soundscapes, guided meditations, and morning reflection journal — no hardware required.

| Criterion | Score | Rationale |
|-----------|-------|-----------|
| Feasibility | 5/5 | Audio playback via Web Audio API, ambient sound mixer, wind-down timer, local storage. ~3-4 weeks MVP. No novel ML. |
| Differentiation | 4/5 | Web-first + bilingual (EN/ZH) + TCM integration. Calm ($70/yr, mobile-only, English-first) and Chinese apps (mobile-only, mainland infrastructure) leave clear gap. |
| Monetization | 4/5 | Free core (wind-down routines + 5 soundscapes). $5/mo for offline downloads + premium analytics + unlimited history. Reasonable conversion path from free. |
| Domain Fit | 5/5 | Strongest sleep ecosystem anchor: evening wind-down feeds JingXin, pre-study focus for learn, privacy-first matches ecosystem values. |

**Recommended #1 Sleep Build** — lowest risk, fastest to ship, establishes the sleep brand.

---

### RestSync (息同步) — rest.ljding.app (18/20)

**One-line pitch:** Bilingual circadian optimization for shift workers, new parents, and anyone fighting an irregular schedule — no wearables required.

| Criterion | Score | Rationale |
|-----------|-------|-----------|
| Feasibility | 3/5 | Circadian phase estimation + light exposure modeling + new parent mode. Algorithm complexity is moderate but well-researched. 5-6 weeks MVP. |
| Differentiation | 5/5 | Bilingual shift work tool with new parent mode — genuinely unique. Timeshifter covers jet lag + shift work but is English-only, mobile-only, $25/yr. Chinese-speaking essential workers have NO bilingual web tool. |
| Monetization | 5/5 | $10/mo for expert mode (unlimited schedules + recovery reports + export). Shift workers are price-insensitive (earning income). Healthcare workers + factory workers = high-LTV. |
| Domain Fit | 4/5 | Moderate learn (sleep education), strong hangwith (shift worker community matching). Fills real gap for diaspora workers. |

**Tied with DreamDrift but MORE differentiated.** Best built as #2 sleep app after DreamDrift content establishes the brand.

---

### SleepScore (眠分) — sleep.ljding.app (16/20)

**One-line pitch:** Device-free sleep quality tracker that turns subjective experience into actionable correlations — with bilingual CBT-I coaching cards.

| Criterion | Score | Rationale |
|-----------|-------|-----------|
| Feasibility | 4/5 | CRUD + correlation engine + charts. Factor correlation is moderately complex but standard. Morning check-in + weekly insight generation. ~4 weeks MVP. |
| Differentiation | 4/5 | Subjective-first + actionable correlations + bilingual coaching cards is underserved. Sleep Cycle/AutoSleep focus on hardware; SleepScore focuses on behavior change. |
| Monetization | 3/5 | $5/mo for unlimited tracking + premium insights. Lower ceiling than DreamDrift/RestSync — sleep diary apps are expected to be free. |
| Domain Fit | 5/5 | Strong learn (CBT-I course integration), strong hangwith (sleep challenge accountability groups), serves as clinical export bridge. |

**Lower priority** — more competitive space (many sleep trackers), lower differentiation from general sleep apps.

---

### NightNest (夜巢) — nest.ljding.app (16/20)

**One-line pitch:** Family sleep coordination hub — track household sleep patterns, share bilingual bedtime routines, and help everyone sleep better together.

| Criterion | Score | Rationale |
|-----------|-------|-----------|
| Feasibility | 4/5 | Multi-user sync + family roles + shared wind-down sequences + WebSocket real-time sync. 5-6 weeks for full MVP. More complex than individual apps. |
| Differentiation | 5/5 | Family sleep hub is genuinely novel — no competitor treats the household as the unit of analysis. Cross-generational (baby through grandparent) + bilingual bedtime coordination fills unique niche. |
| Monetization | 3/5 | $3/mo per family. Lower per-user revenue but multi-person household = natural bundle. Revenue ceiling lower than other sleep apps. |
| Domain Fit | 4/5 | Perfect synergy with parenting apps (BabyLog, FamilyBoard), learn (sleep education), hangwith (family accountability). Requires parenting ecosystem to be established first. |

**Lower priority for now** — depends on parenting apps being live first. Highest ceiling when ecosystem matures.

---

## Sleep Domain Rankings Summary

| Rank | App | Subdomain | Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|------|-----|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 1 | **DreamDrift** | dream.ljding.app | 5 | 4 | 4 | 5 | **18** |
| 1 | **RestSync** | rest.ljding.app | 3 | 5 | 5 | 4 | **18** |
| 3 | **SleepScore** | sleep.ljding.app | 4 | 4 | 3 | 5 | **16** |
| 3 | **NightNest** | nest.ljding.app | 4 | 5 | 3 | 4 | **16** |

### Top Recommendation

**DreamDrift first (3-4 week MVP, lowest risk, establishes sleep brand + audience). RestSync second (highest differentiation, bilingual shift worker white space).**

SleepScore and NightNest are strong but lower priority — SleepScore faces competitive pressure from device-based trackers, and NightNest requires the parenting ecosystem to be established first.

---

## New Gaps Identified

Beyond the existing 4 concepts, fresh research surfaced 2 additional gaps:

### Gap 5: Sleep Anxiety Companion
**Core insight:** Orthosomnia (sleep perfectionism) is rising post-pandemic. Users get anxious from tracking, then can't sleep because they're anxious about their sleep scores. No app addresses sleep anxiety specifically without wearables.

**Concept sketch:** An app that deliberately DOESN'T track sleep. Instead, it helps anxious sleepers let go of tracking while providing evidence-based CBT-I techniques. No scores, no data, just calming guidance. Bilingual.

### Gap 6: Sleep Debt Visualizer
**Core insight:** Sleep debt accumulates silently over weeks. Most apps show last night's score; none show the cumulative trajectory. "You have 12 hours of sleep debt accumulated" is more actionable than "You scored 72."

**Concept sketch:** A web-first sleep debt calculator and recovery trajectory tool. Input bedtime/wake times → see cumulative debt → get personalized recovery schedule. For shift workers managing weekly schedules and freelancers with irregular patterns.

---

*Scoring session completed 2026-05-26. Domain status: ✅ Scored and added to PRIORITIES.md*