# Food & Kitchen — New App Concepts for ljding.app
*Generated: 2026-05-28 | Focus: Web-native, Privacy-first, Bilingual EN/ZH*
*Distinct from: MealDrift, FridgeScan, RecipeVault, CookPair*

---

## Executive Summary

Existing Food & Kitchen apps cover:
- **MealDrift** — anti-planning, random meal suggestions
- **FridgeScan** — inventory tracking with expiry alerts
- **RecipeVault** — recipe bookmarking and organization
- **CookPair** — social cooking matching

**Gap identified:** No apps address personal taste profiling, cost-per-portion for solo cooks, bilingual ingredient translation between Chinese/Western markets, food journals for dietary tracking, or gamified food waste reduction with carbon footprint.

**Recommendation:** Build **TastePrint** first (lowest complexity, high differentiation, learn synergy). Follow with **MiseBox** (high daily utility) and **SubScale** (solo cook portion calculator).

---

## 1. TastePrint — taste.ljding.app

**Pitch:** Build your personal flavor profile over time — TastePrint learns what you genuinely like (not what you should like) and suggests recipes that match YOUR palate, not algorithmic popularity.

**Key Differentiator:** Unlike RecipeVault which saves recipes, or MealDrift which suggests randomly, TastePrint learns your taste fingerprint. You rate dishes on dimensions (umami, spice, bitterness, sweetness, richness) not stars. Over time it builds a taste vector unique to you — then finds recipes you'd actually love that you've never tried. No social influence, no popularity bias.

**Core Features:**
- Taste quiz on first use: rate familiar foods 1-5 on 5 flavor dimensions
- "Taste vector" visualization — your palate in radar chart form
- Recipe feed filtered by your taste profile (similarity score shown)
- Ingredient avoidance tracking (bitterness-sensitive, capsaicin-intolerant, etc.)
- "Reverse engineering" mode: paste any recipe and see how it maps to your taste
- Bilingual flavor terms (鲜 umami, 辣 spice, 苦 bitter, 甜 sweet, 香 rich)

**MVP Complexity:** 2/5
- Taste quiz with 5-point scales
- Flavor dimension tagging for recipes (manual for MVP, crowdsourced library later)
- Recipe feed with similarity scoring
- Profile persistence with localStorage

**Ecosystem Fit:**
- learn.ljding.app: cooking skill courses mapped to taste profiles ("Learn to balance umami — recipes matching YOUR profile")
- MealDrift: taste-aware random suggestions instead of pure randomness
- FridgeScan: "What can I make?" filtered to taste preferences

---

## 2. MiseBox — mise.ljding.app

**Pitch:** Your digital mise en place — organize ingredients, prep steps, and timers in one board before you start cooking. No more mid-recipe scrambling.

**Key Differentiator:** Every other app focuses on planning WHAT to cook or saving recipes. MiseBox focuses on HOW to cook — the prep phase that separates confident cooking from anxious scrambling. It's a digital prep board, not a meal planner. Web-native multi-timer with step sequencing is genuinely underserved.

**Core Features:**
- Paste recipe URL → auto-generates mise en place board
- Ingredient checklist with section groupings (prep steps)
- Embedded timers per step (multi-timer, not just one timer)
- "Prep mode" vs "Cook mode" toggle (hides irrelevant steps)
- Voice-ready: large text mode for looking at screen while hands are dirty
- Bilingual ingredient lists (auto-translate Chinese菜市场 items to grocery equivalents)
- Step-by-step photo hints for unfamiliar techniques

**MVP Complexity:** 3/5
- Recipe URL parsing (Cloudflare Workers + LLM)
- Multi-timer system with Web Audio API
- Board UI with checkoff states
- LocalStorage persistence

**Ecosystem Fit:**
- learn.ljding.app: cooking courses with mise en place boards built-in
- RecipeVault: integration point — "Cook this recipe" → opens MiseBox board
- FridgeScan: "What's about to expire?" → MiseBox board for those ingredients

---

## 3. SubScale — portion.ljding.app

**Pitch:** Resize any recipe for 1, 2, 4 servings — SubScale calculates exact gram measurements and generates a proportional shopping list, so solo cooks never waste ingredients.

**Key Differentiator:** Every recipe app assumes 4 servings. Solo home cooks (especially in diaspora) cook for 1-2 and end up with leftover waste. SubScale solves the "recipe serves 4 but I'm cooking for 1" problem with precision scaling, not vague "half the recipe." Bonus: handles CNY-to-grams for Chinese recipes.

**Core Features:**
- Paste any recipe URL → auto-detects serving size and rescales to target
- Gram-precision scaling (not just "divide by 4")
- Shopping list generator for target servings
- "Fridge check" mode: see what you have vs what's needed
- Common ingredient auto-conversion (1 cup flour → 120g)
- Chinese recipe support: 适量 (适量) conversion with suggested amounts
- Leftover portions: "This makes 6 servings; you need 2. Save 4 portions?"

**MVP Complexity:** 2/5
- Serving size parsing and math
- Ingredient unit normalization (volume → weight)
- Shopping list generation
- Basic Chinese recipe detection

**Ecosystem Fit:**
- FridgeScan: portion-adjusted "what's expiring" suggestions
- RecipeVault: "Resize" button on saved recipes
- learn.ljding.app: cooking courses that teach portion scaling
- SplitPact (finance): cost-per-portion tracking for budget meal prep

---

## 4. WasteTrace — waste.ljding.app

**Pitch:** Track your household food waste with carbon footprint estimates — WasteTrace gamifies reduction by showing your environmental impact in real time, with streaks for waste-free weeks.

**Key Differentiator:** FridgeScan tracks what's in your fridge; WasteTrace tracks what's NOT eaten. Food waste tracking apps exist (e.g., Too Good To Go) but focus on saving surplus food, not tracking household waste volume. Carbon footprint estimates give environmental context that raw weight numbers lack. Privacy-first: no shame, just data.

**Core Features:**
- Quick-log food waste: category (produce, dairy, protein, grain, prepared), estimated weight
- Carbon footprint estimate per category (food waste CO2e database)
- Weekly/monthly waste dashboards with trends
- "Waste-free streak" gamification — 7 days of zero logged waste = badge
- Comparison mode: "You saved 2.3kg food waste this month vs last month"
- Bilingual category names (生鲜 produce, 乳制品 dairy, 蛋白质 protein)
- Tips library: specific advice per waste category (e.g., "Produce: store herbs in water like flowers")

**MVP Complexity:** 3/5
- Waste category CRUD with estimates
- CO2e calculation engine (public data)
- Dashboard with trend visualization (Chart.js or similar)
- Gamification layer (streaks, badges)
- Browser notification reminders

**Ecosystem Fit:**
- FridgeScan: "Items about to expire" → logged as potential waste if not used
- learn.ljding.app: food waste reduction education content
- QuotaGuard (finance): hidden costs of food waste quantified
- GoalSprint (finance): waste reduction as a savings goal

---

## 5. FoodMemo — memo.ljding.app

**Pitch:** A food journal for tracking what you eat and how you feel — FoodMemo helps people with food sensitivities, gut health concerns, or elimination diets identify patterns without apps that are clinical or diet-focused.

**Key Differentiator:** MyFitnessPal tracks macros. FoodMemo tracks how food makes you feel. For the Chinese diaspora, dietary needs often involve Traditional Chinese Medicine considerations (e.g., "凉" foods, "热气") alongside Western nutrition. This app bridges both frameworks. No calorie counting, no diet plans — just pattern discovery.

**Core Features:**
- Quick meal logging: what you ate, portion size, timestamp
- Symptom tracking: energy, bloating, digestion, skin, mood (5-point scales)
- Tag system: dietary frameworks (TCM冷/热, FODMAP, gluten-free, dairy-free, elimination phase)
- Pattern detection: "You report low energy 3x this week — all after pasta meals"
- Ingredient linking: trace symptoms to specific ingredients across meals
- Bilingual symptom vocabulary (腹胀 bloating, 消化不良 poor digestion, 乏力 low energy, 皮肤发痒 skin itch)
- Export for healthcare providers (PDF summary)

**MVP Complexity:** 4/5
- Meal + symptom logging with tagging
- Cross-meal ingredient tracking
- Simple correlation hints ("noticed after X")
- PDF export generation

**Ecosystem Fit:**
- learn.ljding.app: nutrition education, TCM food principles course
- TastePrint: taste preferences may correlate with dietary needs
- Health domain: bridges food tracking with wellness tracking

---

## 6. SpiceLane — spice.ljding.app

**Pitch:** A bilingual recipe app for Chinese diaspora cooking in Western kitchens — SpiceLane translates Chinese cooking techniques, converts Chinese supermarket ingredients to local equivalents, and explains TCM food properties in English.

**Key Differentiator:** RecipeVault bookmarks Chinese recipes; SpiceLane TEACHES Chinese cooking fundamentals. Most Chinese recipe apps either assume access to Chinese supermarkets or don't explain techniques. SpiceLane closes the gap: here's how to make 鱼香茄子 without 郫县豆瓣酱 — here's what to substitute, here's why it works. Dual-framework explanations (Western technique + TCM property).

**Core Features:**
- Chinese recipe library with technique breakdowns
- "Ingredient swap" engine: Chinese ingredient → local equivalent + why it matters
- Technique glossary: 爆炒 (stir-fry), 蒸 (steaming), 红烧 (braising) with video hints
- TCM food property labels: 温 (warm), 凉 (cool), 平 (neutral), 热 (hot), 寒 (cold)
- Bilingual recipe cards: original Chinese + English translation + audio pronunciation
- Difficulty rating for Western cooks unfamiliar with techniques
- "Suitable for" tags: vegetarian-adaptable, gluten-free version possible, etc.

**MVP Complexity:** 3/5
- Bilingual recipe database (curated set for MVP)
- Ingredient substitution matrix
- TCM property tagging system
- Technique video embed library (YouTube/腾讯)

**Ecosystem Fit:**
- learn.ljding.app: Chinese cooking courses with technique lessons
- RecipeVault: "Save Chinese recipe" → suggestion to try SpiceLane for technique support
- MiseBox: technique steps linked to SpiceLane glossary
- TastePrint: TCM properties as an additional taste dimension

---

## 7. BatchChef — batch.ljding.app

**Pitch:** Plan and execute weekend batch cooking sessions — BatchChef designs efficient cooking schedules that minimize active time, maximize parallel tasks, and portion leftovers for the week ahead.

**Key Differentiator:** MealDrift is anti-planning. BatchChef is intentional planning — but for batch cooking sessions, not daily meals. It schedules what to cook, sequences tasks to minimize oven/stovetop conflicts, and automatically calculates leftover portions for grab-and-go meals. For people who meal-prep on Sundays.

**Core Features:**
- Select 3-5 recipes for a batch session
- Automatic scheduling: what goes in oven vs stovetop vs prep stages
- Time estimate + "active time" estimate (vs passive cook time)
- Parallel task highlighting ("While soup simmers, prep the stir-fry")
- Portion division: total portions ÷ household members = individual takeaway containers
- Leftover calendar: "You have 6 portions of dal in the freezer — eat by Day 12"
- "Grab lunch" mode: what leftover containers are ready for work/school?

**MVP Complexity:** 4/5
- Recipe selection + scheduling algorithm
- Timeline visualization (Gantt-style)
- Portion division calculator
- Leftover tracking with "eat by" dates

**Ecosystem Fit:**
- FridgeScan: leftover containers tracked in inventory
- learn.ljding.app: batch cooking skill course
- SubScale: portion sizing for batch sessions
- SplitPact (finance): cost-per-portion for batch cooking budget tracking

---

## Summary Table

| App | Subdomain | MVP Complexity | Differentiation | Ecosystem Fit |
|-----|-----------|----------------|-----------------|---------------|
| **TastePrint** | taste.ljding.app | 2/5 | Personal taste AI, not crowdsourced | High (learn + MealDrift) |
| **MiseBox** | mise.ljding.app | 3/5 | Prep-first, not recipe-first | High (learn + RecipeVault) |
| **SubScale** | subscale.ljding.app | 2/5 | Gram-precision solo scaling | High (FridgeScan + RecipeVault) |
| **WasteTrace** | waste.ljding.app | 3/5 | Carbon footprint + gamification | Medium (learn + QuotaGuard) |
| **FoodMemo** | memo.ljding.app | 4/5 | TCM + Western symptom tracking | Medium (learn + Health domain) |
| **SpiceLane** | spice.ljding.app | 3/5 | Bilingual Chinese cooking education | High (learn + RecipeVault) |
| **BatchChef** | batch.ljding.app | 4/5 | Batch cooking scheduler | High (FridgeScan + SubScale) |

---

## Recommended Build Order

1. **SubScale** — 2/5 complexity, immediate utility for solo cooks, shortest path to shipped
2. **MiseBox** — 3/5, high daily utility, RecipeVault integration point
3. **TastePrint** — 2/5, most novel, strongest learn.ljding.app synergy
4. **WasteTrace** — 3/5, gamification proven to work on web, environmental trend
5. **SpiceLane** — 3/5, Chinese diaspora niche, strong differentiation
6. **BatchChef** — 4/5, batch cooking is niche but valuable
7. **FoodMemo** — 4/5, highest complexity, valuable for health niche

---

## What Makes These Distinct

Each fills a gap NOT addressed by the original four:
- **MealDrift** (anti-planning) ≠ BatchChef (intentional batch planning)
- **FridgeScan** (inventory inside) ≠ WasteTrace (tracking what's wasted)
- **RecipeVault** (bookmarking) ≠ SpiceLane (teaching techniques)
- **CookPair** (social cooking) ≠ SubScale (solo portion math)

The combined portfolio covers: taste profiling, prep boards, portion scaling, waste tracking, dietary journals, bilingual cooking education, and batch scheduling — with strong learn.ljding.app and hangwith.ljding.app integration paths.
