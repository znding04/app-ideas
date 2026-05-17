# ljding.app App Ideas

> Research-backed app opportunities for the ljding.app ecosystem — updated 2026-05-06

---

## Existing Apps

| App | Subdomain | Description | Status |
|-----|-----------|-------------|--------|
| 找谁玩 | hangwith.ljding.app | Friend hangout tracker with relationship scoring | ✅ Live |
| 玩点啥 | arcade.ljding.app | Classic game arcade (Pong, Snake, 2048, Tetris) | ✅ Live |
| 学点啥 | learn.ljding.app | Serious self-learning platform (no gamification) | 🚧 In Progress |

**Unified Tech Stack:** Vue 3 + Vite + Tailwind CSS + Cloudflare Workers/Pages + D1/KV

---

## Ecosystem Gaps Analysis

The current ecosystem covers **social tracking** (找谁玩), **entertainment** (玩点啥), and **learning** (学点啥). What's missing:

1. **Daily life utilities** — expense tracking, bill splitting, bookmarks
2. **Emotional wellness** — mood tracking, gratitude/journaling
3. **Personal knowledge management** — reading lists, link vaults
4. **Finance** — portfolio/investment tracking (user already does QuantConnect), daily spending awareness
5. **Health & wellness** — sleep tracking, workout logging, unified wellness dashboard
6. **Food & kitchen** — fridge/pantry inventory, recipe management *(NEW)*
7. **Shared household** — roommate coordination, chores, communal supplies *(NEW)*

---

## Suggested New Apps

### 1. 记账分摊 (split.ljding.app)

- **中文名**: 记账分摊
- **English Name**: Split Bill — Group Expense Splitter
- **Purpose**: Track shared expenses with friends, roommates, or travel groups and settle up effortlessly. Ties directly into the 找谁玩 friend network.
- **Key Features**:
  - Add expenses with payer, participants, and split method (equal, custom %, exact amounts)
  - Friend auto-complete pulling from 找谁玩 contacts (future integration)
  - "Settle up" engine: minimize transactions to resolve all debts
  - Group/pool view: who owes whom and how much
  - Expense category tags and monthly summaries
  - Lightweight enough to split a dinner tab; powerful enough for a 2-week trip
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1
- **Priority**: **High**
- **Why**: Complements 找谁玩 perfectly — after hanging out, log the expense. High utility, low complexity. Proven by apps like Splitwise and Settle Up. Every friend group needs this at least monthly. Quick to MVP with Vue + D1.

---

### 2. 心情档案 (mood.ljding.app)

- **中文名**: 心情档案
- **English Name**: Mood Journal — Emotional Wellness Tracker
- **Purpose**: Log daily moods, identify emotional patterns, and build self-awareness over time. Lightweight emotional health companion.
- **Key Features**:
  - One-tap mood entry (😊 😐 😔 😤 😴 on a 5-point scale) with optional note
  - Tag entries with activities (work, social, exercise, screen time)
  - Calendar heatmap view showing mood history
  - Weekly/monthly mood trend charts
  - AI-generated insights (pattern detection: "You tend to feel worse on Mondays")
  - Private, offline-first with optional cloud sync
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Chart.js
- **Priority**: **High**
- **Why**: Mental health apps are a top-growing category. Web-based mood trackers are rare (most are mobile). Emotional wellness pairs well with social connection (找谁玩's relationship tracking). Low competition in the Chinese-language web space. GDPR/privacy-friendly by design.

---

### 3. 收藏夹 (vault.ljding.app)

- **中文名**: 收藏夹
- **English Name**: Link Vault — Personal Bookmark Manager
- **Purpose**: Save, organize, and rediscover links. Tags + AI auto-tagging + full-text search across your saved web.
- **Key Features**:
  - Save URLs with title, description, and tags (manual + AI auto-tag via page content)
  - Full-text search across titles, descriptions, and extracted page content
  - Folder/category hierarchy + flat tag system
  - Read-it-later status (unread, reading, done)
  - Import/export bookmarks (JSON, HTML)
  - Browser extension (future): save from any page
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Cloudflare Workers (fetch + parse page metadata)
- **Priority**: **Medium**
- **Why**: Browser bookmarks are broken for most people. Pinboard, Raindrop.io, and Notion databases all solve parts of this. A clean, fast, no-nonsense Chinese-friendly version fills a gap. Can showcase Cloudflare Workers' fetch/proxy capabilities.

---

### 4. 读书笔记 (read.ljding.app)

- **中文名**: 读书笔记
- **English Name**: Reading List — Book Tracker & Notes
- **Purpose**: Track reading progress, take chapter notes, and build a personal knowledge base from books. Complements 学点啥.
- **Key Features**:
  - Add books (title, author, ISBN lookup via Open Library API)
  - Track status: Want to Read → Reading → Done
  - Chapter-by-chapter reading progress
  - Notes per chapter (Markdown editor)
  - Highlights/quotes collection
  - Tags and search across all notes
  - Reading statistics: books per month, pages per day, reading streak
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Open Library API (free)
- **Priority**: **Medium**
- **Why**: 学点啥 already attracts learning-focused users. A reading tracker rounds out the "serious learning" ecosystem. Book tracking + note-taking is a proven combination (Readwise, Matter, Instapaper). Complements QuantConnect/finance hobby. Low external API dependency for MVP.

---

### 5. 倒就碑 (倒了就忘) (note.ljding.app)

- **中文名**: 倒就碑
- **English Name**: Stash — ephemeral note & quick capture tool
- **Purpose**: Ultra-fast thought capture with automatic expiration. Drop a note, set a timer, it's gone. For people who want to offload thoughts without cluttering their notes app.
- **Key Features**:
  - One-click note creation (title + optional body, max 280 chars for main note)
  - Auto-delete after: 1 hour, 24 hours, 7 days, 30 days (user picks)
  - Optional "extend" tap to push expiry
  - No folders, no tags — just a chronological stream
  - Optional PIN lock per note
  - Clean, minimal UI optimized for speed
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 (TTL-based cleanup via worker cron)
- **Priority**: **Low**
- **Why**: Interesting concept, not many web equivalents (most ephemeral apps are mobile). Differentiated from Notion/Evernote. Quick to build. Lower utility but high novelty. Good for showcasing Cloudflare cron triggers.

---

## Recommended Next Build

### 🏆 记账分摊 (split.ljding.app)

**Rationale:**

1. **Direct ecosystem synergy**: 找谁玩 tracks *who* you hang with; 记账分摊 tracks *what you spent*. Post-hangout workflow: "We just ate at X — let me log the expense and split it." Same user, same friend groups, immediate value.
2. **Proven market**: Splitwise has millions of users. Settle Up, Tricount, and SplitWise are consistently top-grossing finance apps. Demand is validated.
3. **Quick MVP**: Core logic is straightforward — add expense, assign participants, calculate net balances. Vue + D1 handles it perfectly.
4. **Daily/weekly retention**: Friend groups split bills regularly (dinners, trips, concerts), creating natural return visits.
5. **Monetization path**: Future premium features (expense categories, charts, currency conversion) could support a subscription.
6. **Differentiation**: Most split-bill apps are mobile. A clean web version with Chinese-language support fills a clear gap.

**Estimated MVP**: 1–2 weekends  
**Follow-up**: Push settle-up notifications via email (Cloudflare Email Routing), integrate with 找谁玩 friend list

---

## Tech Stack Reference

All apps use the established ljding.app stack:

| Layer | Choice |
|-------|--------|
| Frontend | Vue 3 (Composition API) + Vite |
| Styling | Tailwind CSS 3/4 |
| Routing | Vue Router 4 (hash mode) |
| Backend | Cloudflare Workers |
| Database | Cloudflare D1 (SQLite) or KV |
| Deployment | `wrangler deploy` |
| Auth | Same OAuth pattern as 找谁玩 (Google/GitHub/Apple) |

This keeps the ecosystem **consistent, fast, and free to host**.

---

---

## PKM / Second Brain Apps (Researched 2026-05-03)

> Personal Knowledge Management is a ~$5B market with significant underserved gaps. Generated 3 concepts from Claude Code research.

### Concept 1: **Sparks** — "PKM that works with your brain, not against it."

- **Subdomain**: sparks.ljding.app
- **Purpose**: Neurodivergent-first knowledge tool — zero-config capture, gentle review nudges, calm minimal UI designed to reduce overwhelm
- **Core Features**:
  - One-tap capture (voice, text, photo, screenshot; no categorization required)
  - Calm UI — muted palette, no sidebar tree, content surfaces contextually
  - Gentle nudges — adaptive reminders that adjust to your rhythm (missed review = no guilt)
  - Visual/spatial canvas — arrange ideas spatially instead of hierarchically
  - Focus mode — single-note view, everything else hidden
  - AI thought-linking — show 1–2 related past notes on capture (not 47 backlinks)
  - "Brain dump" mode — stream-of-consciousness capture that AI later organizes
- **Target**: ADHD/Neurodivergent users (~15-20% of knowledge workers); secondary: anyone overwhelmed by Notion/Obsidian
- **Differentiation**: No competitor explicitly owns ADHD-first positioning. First-mover advantage.
- **Tech Stack**: SvelteKit + Tailwind (simpler than Vue, smaller bundle) + PocketBase or Supabase
- **MVP Scope (4-6 weeks)**: Web + PWA, one-tap capture, calm minimal UI, AI auto-linking, brain dump mode, gentle review system
- **Monetization**: Free (unlimited capture, basic linking) | Pro $8/mo (voice, canvas, advanced AI) | Supporter $12/mo
- **Feasibility Scores**:
  - Technical Complexity: 5/10 (simpler AI than Drift; UX design is the hard part)
  - Market Demand: 8/10 (vocal unmet demand, no incumbent owns this positioning)
  - Differentiation: 9/10 (first-mover on neurodivergent positioning)

### Concept 2: **Drift** — "Your thoughts, caught before they vanish."

- **Subdomain**: drift.ljding.app
- **Purpose**: AI-native capture tool — eliminates the "capture bottleneck" (20-60% of info never saved because it takes too long)
- **Core Features**:
  - Instant capture widget — global hotkey or floating button; type/paste/voice <5 seconds
  - Auto-organization via AI — no folders, no tags, no decisions; clusters and links by meaning
  - Browser extension — highlights, tabs, articles pulled in with context
  - Smart resurfacing — related notes appear when working on relevant topics
  - Natural language search — "that article about React Server Components from last week"
  - Daily digest — AI-generated summary of captures, connections found, review suggestions
  - Plain markdown export — no lock-in
- **Target**: Knowledge workers, developers, researchers who hoard tabs and lose ideas
- **Differentiation**: vs Obsidian (zero config), vs Notion (no sluggish app, AI is architecture not sidebar)
- **Tech Stack**: Next.js + Supabase + Claude API + Voyage AI embeddings
- **MVP Scope (4-6 weeks)**: Web app, instant capture, AI auto-tagging/clustering, natural language search, Chrome extension, daily digest
- **Monetization**: Free (100 captures/mo) | Pro $10/mo (unlimited, AI org, smart resurfacing) | Team $15/user/mo
- **Feasibility Scores**:
  - Technical Complexity: 7/10 (AI pipeline is hard; simple UI by design)
  - Market Demand: 9/10 (#1 complaint across all PKM tools)
  - Differentiation: 6/10 (Mem, Capacities in similar space; execution is the moat)

### Concept 3: **Recall** — "Notes you actually remember."

- **Subdomain**: recall.ljding.app
- **Purpose**: Note-taking with native spaced repetition — AI generates review questions from your highlights/notes
- **Core Features**:
  - Highlight any text → AI auto-generates review questions
  - Native spaced repetition — SM-2 algorithm, built-in, not a plugin
  - Smart resurfacing — forgotten notes about Topic X reappear when writing about X
  - AI question generation — paste PDF/lecture notes → get review deck in seconds
  - Connected knowledge graph — see how concepts link across notes/courses/projects
  - Progress dashboard — retention rates, streaks, knowledge gaps
  - Study session mode — focused review with interleaved topics
- **Target**: Students (med/law/STEM), researchers, lifelong learners, cert prep, language learners
- **Differentiation**: vs Obsidian+Anki (no plugin fragility, no manual card creation) | vs RemNote (modern UI, better AI)
- **Tech Stack**: Next.js + Tiptap (rich text) + Supabase (spaced repetition in Postgres is natural) + Claude API
- **MVP Scope (4-6 weeks)**: Clean note editor, highlight→AI questions, SM-2 review engine, PDF import, knowledge graph viz, mobile review mode
- **Monetization**: Free (50 notes, 20 AI questions/mo) | Student $6/mo (unlimited, PDF import) | Pro $12/mo (team study, API)
- **Feasibility Scores**:
  - Technical Complexity: 6/10 (SR algorithms well-documented; AI question gen is novel)
  - Market Demand: 8/10 (students perpetually seek better study tools)
  - Differentiation: 7/10 (RemNote is incumbent but clunky; AI generation is the wedge)

### Comparison Matrix

| | Sparks | Drift | Recall |
|---|---|---|---|
| Technical Complexity | 5 | 7 | 6 |
| Market Demand | 8 | 9 | 8 |
| Differentiation | 9 | 6 | 7 |
| **Composite** | **22** | **22** | **21** |
| Time to Revenue | Medium-Fast | Medium | Fast (students convert) |
| Moat | Community/brand | Data/habit | Habit/retention data |
| Risk | UX must be exceptional | Crowded AI-capture space | RemNote incumbent |

### Recommendation

**Sparks** has the highest differentiation (9/10) and clearest unowned positioning. No competitor explicitly serves ADHD/neurodivergent users despite massive vocal demand. If UX execution is excellent, this becomes a beloved niche product with strong word-of-mouth.

**Recall** is the safest bet for fastest revenue — students convert quickly and have recurring need. Undercuts RemNote ($15/mo) with better AI at $6-12/mo.

**Drift** has the highest raw demand but faces more competition in the AI-capture space.

**Note**: The existing ecosystem gap analysis identified **personal knowledge management** as a missing piece. These PKM concepts directly fill that gap with opinionated, differentiated takes.

---

## Health & Wellness Apps (Researched 2026-05-04)

> Full research at `HEALTH-RESEARCH.md`. Market is fatigued with subscription-heavy, wearable-dependent apps. The gap is in simple, web-first tools that track *context* (why you slept poorly) rather than just *metrics*.

### 1. 睡眠档案 (sleep.ljding.app)

- **中文名**: 睡眠档案
- **English Name**: Sleep Journal + Context Tracker
- **Purpose**: Manual sleep logging with daily context tags — track *why* sleep was good/bad, not just duration. Targets orthosomnia (anxiety from over-tracking) and users who want doctor-recommended sleep diaries without wearable dependency.
- **Key Features**:
  - Morning: log sleep quality (1-5), duration, wake count
  - Evening: tag daily factors (caffeine, exercise, alcohol, stress, late screens)
  - Correlation engine: "nights after exercise avg 7.2hrs vs late caffeine avg 5.8hrs"
  - Calendar heatmap + weekly trend charts
  - No wearables, no sensors — intentionally manual
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Chart.js
- **Priority**: **High** (Recommended 2nd app to build after split.ljding.app)
- **Why**: Low complexity (3/10), high ecosystem fit (9/10) — directly feeds mood tracker data. No web-first context-focused sleep tool exists. Ship in weeks.
- **Feasibility Scores**: Demand 7 | Complexity 3 | Differentiation 8 | Ecosystem Fit 9 | **Total: 27/40**

### 2. 健身日志 (lift.ljding.app)

- **中文名**: 健身日志
- **English Name**: Minimal Workout Logger
- **Purpose**: Spreadsheet-level flexibility with app-level UX. Fast gym-floor entry for intermediate lifters who are stuck on Google Sheets because every app is too bloated or too simple.
- **Key Features**:
  - Quick set logging (weight × reps) with large tap targets
  - Exercise database (searchable, customizable)
  - Progress charts per exercise over time
  - Custom workout templates (not pre-built programs)
  - CSV import/export for spreadsheet migration
  - PWA — works on phone in gym, desktop at home
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1
- **Priority**: **Medium** (optional, standalone)
- **Why**: Web-first workout logger is genuinely novel. Spreadsheet users are actively looking for alternatives. Activity data connects to sleep/mood ecosystem.
- **Feasibility Scores**: Demand 6 | Complexity 4 | Differentiation 7 | Ecosystem Fit 6 | **Total: 23/40**

### 3. 身心仪表盘 (wellness.ljding.app)

- **中文名**: 身心仪表盘
- **English Name**: Unified Wellness Dashboard
- **Purpose**: Web-based dashboard tying together sleep + mood + exercise + meditation into cross-domain correlations. No wearable ecosystem buy-in required.
- **Key Features**:
  - Pulls data from sleep.ljding.app, mood.ljding.app (or manual entry for activity)
  - Cross-domain correlation engine: "you sleep better on days you exercise," "mood dips after 2+ days without meditation"
  - Weekly/monthly trend charts across all domains
  - Shareable read-only link for therapist/accountability partner
  - Desktop-first (dashboard consumed on larger screens)
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Workers (correlation engine)
- **Priority**: **High** (but as capstone — build after sleep + mood trackers)
- **Why**: Highest differentiation (9/10), highest demand (8/10). No web-based wearable-free unified wellness dashboard exists. Ties entire ecosystem together.
- **Feasibility Scores**: Demand 8 | Complexity 7 | Differentiation 9 | Ecosystem Fit 10 | **Total: 34/40**

---

## Productivity & Daily Workflow Apps (Researched 2026-05-05)

> Generated via Claude Code research — market gaps in Chinese-language productivity web apps. These complement learn.ljding.app (learning) and hangwith.ljding.app (social) with daily workflow tools.

### 1. 精力档案 (track.ljding.app)

- **中文名**: 精力档案
- **English Name**: Energy Tracker — Habit & Energy Pattern Journal
- **Problem**: Most habit trackers gamify streaks but ignore energy/mood patterns, leaving users burning out without knowing why.
- **Key Features**:
  - Energy level + mood logging with one-tap entries throughout the day (peak/mid/low)
  - Weekly pattern visualization (when are you most productive?)
  - Habit stacking suggestions based on energy curves
  - Simple journaling prompts tied to low-energy moments
  - Monthly reports with actionable "schedule redesign" tips
- **Why web-first**: Quick logging via bookmark/PWA; data visualization needs screen real estate; shareable reports
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Chart.js
- **Priority**: **Medium** (fits ecosystem, moderate complexity)
- **Feasibility Scores**: Demand 7 | Complexity 4 | Differentiation 6 | Ecosystem Fit 7 | **Total: 24/40**

### 2. 深度工作 (focus.ljding.app)

- **中文名**: 深度工作
- **English Name**: Focus Planner — Deep Work Session Manager
- **Problem**: Chinese knowledge workers context-switch between WeChat, DingTalk, and tasks constantly — no tool helps them protect and plan deep work blocks.
- **Key Features**:
  - Pomodoro with configurable work/rest ratios and ambient sounds
  - Daily "3 big things" prioritization (not a full task manager)
  - Distraction log — tap to record what pulled you out, see patterns weekly
  - Calendar-aware: suggests best focus windows from free time
  - Shareable focus stats (accountability with friends)
- **Why web-first**: Always-open browser tab as workspace anchor; no app-store friction; works on any office machine
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Workers (ambient sounds via streaming)
- **Priority**: **High** (direct synergy with learn.ljding.app for study sessions)
- **Feasibility Scores**: Demand 8 | Complexity 5 | Differentiation 7 | Ecosystem Fit 8 | **Total: 28/40**

### 3. 周复盘 (review.ljding.app)

- **中文名**: 周复盘
- **English Name**: Weekly Review — Guided Reflection & Planning Ritual
- **Problem**: People know weekly reviews help but never build the habit — no lightweight, opinionated tool guides them through it in under 10 minutes.
- **Key Features**:
  - Guided 5-step weekly review flow (wins, misses, lessons, next week priorities, gratitude)
  - Auto-pulls data from other ljding apps (learning streaks, social events, focus hours)
  - Trend dashboard: are weeks getting better? Where are recurring friction points?
  - Optional Sunday evening reminder via email
  - Exportable weekly summaries (Markdown/image for sharing)
- **Why web-first**: Ritual happens at a desk; rich text input and dashboard review need a full screen; no install barrier lowers adoption
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Email Routing (reminder cron)
- **Priority**: **Medium** (aggregation layer — build after core apps)
- **Feasibility Scores**: Demand 7 | Complexity 6 | Differentiation 7 | Ecosystem Fit 9 | **Total: 29/40**

---

## Recommended Build Sequence (Updated)

|| # | App | Subdomain | Rationale |
||---|-----|-----------|-----------|
|| 1 | 记账分摊 | split.ljding.app | High utility, direct synergy with 找谁玩, proven market |
|| 2 | 深度工作 | focus.ljding.app | High demand (8/10), complements learn.ljding.app, moderate complexity |
|| 3 | 睡眠档案 | sleep.ljding.app | Low complexity, high ecosystem fit, complements mood tracker |
|| 4 | 心情档案 | mood.ljding.app | Already planned, feeds into wellness dashboard |
|| 5 | 周复盘 | review.ljding.app | Natural aggregation layer — build after core apps complete |
|| 6 | 身心仪表盘 | wellness.ljding.app | Capstone tying sleep + mood + activity together |
|| 7 | 健身日志 | lift.ljding.app | Optional standalone — weakest ecosystem connection |
|| 8 | 精力档案 | track.ljding.app | Medium priority, overlaps somewhat with mood/energy concepts |

---

## Food & Kitchen Apps (Researched 2026-05-06)

> New domain — not previously explored. Food tracking contrasts with learn.ljding.app (mental growth) and hangwith.ljding.app (social connection) by addressing **daily physical nourishment**. The kitchen is a major time sink with zero good web-first tools.

### 1. 冰箱档案 (fridge.ljding.app)

- **中文名**: 冰箱档案
- **English Name**: Fridge/Pantry Inventory Manager
- **Purpose**: Track what's in your fridge and pantry, get expiring-soon alerts, auto-generate shopping lists, and reduce food waste. For people who buy groceries but forget what they already have.
- **Key Features**:
  - Add items with name, location (fridge/freezer/pantry), quantity, purchase date, expiry date
  - "Expiring soon" dashboard — see what's going bad this week
  - Auto-generated shopping list from items below threshold (e.g., "eggs: 2 left, buy more")
  - Pantry mode: non-expiring staples (rice, pasta, oil) tracked by quantity
  - Barcode/Receipt scan to quickly add multiple items (future)
  - Recipe suggestions based on what's about to expire
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Workers (expiry cron)
- **Priority**: **Medium** (high utility, moderate complexity)
- **Why**: Food waste is a top concern for eco-conscious consumers. No clean web-first fridge/pantry tracker exists. High daily engagement potential (users check their fridge daily). Pairs with recipe manager for a full "from grocery to meal" cycle.
- **Feasibility Scores**: Demand 7 | Complexity 4 | Differentiation 7 | Ecosystem Fit 6 | **Total: 24/40**

### 2. 食谱本 (recipe.ljding.app)

- **中文名**: 食谱本
- **English Name**: Recipe Keeper — Personal Cookbook
- **Purpose**: Save, organize, and rediscover recipes. Tag by cuisine, season, diet, and difficulty. Import from URLs (，自动提取食材和步骤). Built-in meal planning and grocery list generation.
- **Key Features**:
  - Save recipes via URL import (AI extracts title, ingredients, steps, cook time)
  - Manual recipe entry with structured fields
  - Tag system: cuisine (川菜, 意大利菜), diet (素食, 无麸质), meal type (早餐, 晚餐), mood (快手, 周末)
  - Weekly meal planner — drag recipes into calendar days
  - Auto-generate grocery list from planned week's meals (deduplicates ingredients)
  - Servings scaler — adjust recipe for different group sizes
  - Cookbook mode: browse by book-style categories
  - Private by default; optional share links
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Workers (recipe URL parser with HTML extraction)
- **Priority**: **Medium** (complements fridge tracker, fits food ecosystem)
- **Why**: Every home cook saves recipes in 47 different places (Notes, screenshots, bookmarks, Word docs). A clean, Chinese-friendly recipe keeper fills a real organizational gap. Pairs naturally with fridge.ljding.app for a "what's in my fridge → what can I cook" flow.
- **Feasibility Scores**: Demand 7 | Complexity 5 | Differentiation 7 | Ecosystem Fit 7 | **Total: 26/40**

### 3. 外卖档案 (takeout.ljding.app)

- **中文名**: 外卖档案
- **English Name**: Local Restaurant Tracker — "Where Should We Eat?"
- **Purpose**: Track restaurants you've ordered from or dined at, rate them, log what you ordered, and answer "where should we eat?" with actual data instead of scrolling through Meituan/Dianping for 20 minutes.
- **Key Features**:
  - Add restaurants with name, cuisine type, location, delivery availability
  - Log visits: date, what you ordered, rating (food 1-5, delivery speed, value)
  - "Order again" quick list — your top ordered items at each place
  - Group voting: share a link, friends pick their preference, random choice or majority wins
  - Price range tracking (小人儿/小贵/奢侈)
  - Filters: cuisine, price, distance, last ordered
  - Integration potential with 找谁玩 (hangwith.ljding.app) — "we're hanging out Friday, pick a place"
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1
- **Priority**: **Low-Medium** (fun side project, lighter utility than others)
- **Why**: Chinese users already heavily use Meituan/Dianping for ordering but these apps are terrible for personal history and "where should we eat" decisions. A personal restaurant memory that feeds into social planning (找谁玩 integration) is a unique angle. Low complexity MVP.
- **Feasibility Scores**: Demand 6 | Complexity 3 | Differentiation 8 | Ecosystem Fit 7 | **Total: 24/40**

---

## Shared Household & Roommate Apps (Researched 2026-05-06)

> New domain — not previously explored. Complements 找谁玩 (social tracking) and 记账分摊 (split.ljding.app, in pipeline) with a focus on **daily shared living logistics**. Addresses the pain of coordinating with roommates or family members.

### 4. 室友记 (roommate.ljding.app)

- **中文名**: 室友记
- **English Name**: Roommate Manager — Chores, Tasks & Shared Life
- **Purpose**: Eliminate the "who bought toilet paper last time?" and "it's your turn to clean the bathroom" friction. Track shared household tasks, rotating chores, and communal supplies — without the awkwardness of a roommate confrontation.
- **Key Features**:
  - Household creation with invite codes (up to 6 members)
  - Shared task list: chores with assignee, due date, recurrence (daily/weekly/monthly)
  - Rotating chore wheel: auto-assigns based on fair rotation
  - "Communal supplies" tracker: who bought paper towels, soap, etc. and when
  - Grocery run accountability: log who paid for communal purchases (auto-settle via split.ljding.app integration)
  - Quiet hours / guest policy settings (soft rules, not enforcement)
  - Move-out checklist: track deposit-return readiness
  - Private between roommates — not public
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1
- **Priority**: **High** (direct synergy with split.ljding.app pipeline, strong utility)
- **Why**: Every shared apartment has this friction. No clean web-first roommate coordination tool exists. Integrates directly with 记账分摊 (split.ljding.app) for a full roommate finance+logistics solution. Users return daily during move-in week.
- **Feasibility Scores**: Demand 7 | Complexity 4 | Differentiation 8 | Ecosystem Fit 8 | **Total: 27/40**

### 5. 家居记 (home.ljding.app)

- **中文名**: 家居记
- **English Name**: Home Maintenance Journal
- **Purpose**: Track home appliances, maintenance schedules, warranty dates, and repair history. For homeowners or long-term renters who want to stop being surprised by "the water heater is 12 years old."
- **Key Features**:
  - Add appliances: name, purchase date, warranty expiry, expected lifespan, photo, receipt upload
  - Maintenance reminders: "clean the fridge coils quarterly," "replace HVAC filter monthly"
  - Repair log: every time something breaks, log the date, what was wrong, cost, who fixed it
  - Warranty card scanner: photograph and auto-extract dates via Workers AI
  - Home inventory mode: full list for insurance purposes (exportable)
  - Seasonal checklists: "prepare for winter," "spring cleaning"
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Workers (warranty OCR/extraction)
- **Priority**: **Medium** (more relevant to homeowners, narrower audience)
- **Why**: Most people have zero idea when their appliances were purchased or when warranties expire. Home inventory for insurance claims is a proven pain point. Differentiated from generic "home inventory" apps by focusing on maintenance *journal* (history over time) not just snapshot inventory.
- **Feasibility Scores**: Demand 6 | Complexity 5 | Differentiation 7 | Ecosystem Fit 5 | **Total: 23/40**

---

## Finance Domain — Beyond Bill Splitting (Researched 2026-05-06)

> The notes mention "Finance" as a gap but only 记账分摊 (split.ljding.app) is documented. Here's the deeper exploration.

### 6. 小账本 (pocket.ljding.app)

- **中文名**: 小账本
- **English Name**: Daily Expense Journal — Intentional Spending Tracker
- **Problem**: Budgeting apps ask you to categorize every transaction and set rigid budgets — then users quit after 2 weeks. The gap isn't "tracking spending" (banks do this), it's **understanding why you spent** and building awareness without the cognitive overhead.
- **Key Features**:
  - One-tap expense logging: amount + optional 1-line note (no categories required for MVP)
  - Monthly spending timeline: visual strip showing where money went, day by day
  - Monthly email summary: "You spent $X this month. Top categories: food 40%, transport 20%. 3 impulse purchases flagged."
  - Soft budget alerts: "You've spent 80% of your food budget with 10 days left" (not hard locks)
  - "Was it worth it?" reflection: tap an expense to answer one question — worth it / neutral / regret
  - Auto-import from bank CSV (manual upload) — category-free by default, AI can suggest categories
  - 3-month trend: are you spending more on dining out vs. cooking at home?
- **Why NOT a full budget app**: Mint died because it was overwhelming. YNAB is great but requires 15 min/day. 小账本 is the "one tap, no decisions" alternative.
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Workers (CSV parsing)
- **Priority**: **Medium** (user already uses QuantConnect; this is a spending awareness complement)
- **Feasibility Scores**: Demand 7 | Complexity 4 | Differentiation 7 | Ecosystem Fit 6 | **Total: 24/40**

---

## Recommended Build Sequence (Updated 2026-05-06)

||| # | App | Subdomain | Domain | Rationale |
|||---|-----|-----------|--------|-----------|
||| 1 | 记账分摊 | split.ljding.app | Finance | High utility, proven market, direct synergy with 找谁玩 |
||| 2 | 室友记 | roommate.ljding.app | Household | High utility, integrates with split, strong daily retention |
||| 3 | 深度工作 | focus.ljding.app | Productivity | High demand, complements learn.ljding.app |
||| 4 | 冰箱档案 | fridge.ljding.app | Food/Kitchen | Medium demand, unique web-first gap, daily engagement |
||| 5 | 睡眠档案 | sleep.ljding.app | Health | Low complexity, high ecosystem fit |
||| 6 | 心情档案 | mood.ljding.app | Health | Already planned, feeds into wellness dashboard |
||| 7 | 食谱本 | recipe.ljding.app | Food/Kitchen | Complements fridge tracker; food ecosystem expansion |
||| 8 | 身心仪表盘 | wellness.ljding.app | Health | Capstone — ties sleep + mood + activity together |
||| 9 | 小账本 | pocket.ljding.app | Finance | Spending awareness; complements QuantConnect |
||| 10 | 周复盘 | review.ljding.app | Productivity | Aggregation layer — build after core apps |
||| 11 | 家居记 | home.ljding.app | Household | Narrower audience; optional long-tail build |

**New #1 (after split): Roommate Manager** — most synergy with existing pipeline (directly pairs with split.ljding.app for roommate finance+logistics), highest demand of the new ideas, moderate complexity.

---

## Appendix: Ideas Considered but Not Included

- **AI Writing Assistant** — crowded market (Claude, ChatGPT); hard to differentiate
- **Password Manager** — security complexity too high for MVP; trust barrier
- **Habit Tracker** *(previously suggested)* — solid idea but overlaps with 找谁玩's retention mechanics; mood tracker fills emotional wellness gap instead
- **World Clock** *(previously suggested)* — useful but too narrow for a full app
- **Portfolio Tracker (SOXL, etc.)** — user already has QuantConnect for this
- **General AI Chatbot** — crowded; Claude.ai, ChatGPT own this

---

## Health & Wellness Apps (Researched 2026-05-07)

> New domain — complements learn.ljding.app (mental) and hangwith.ljding.app (social) by addressing **physical health habits**. Web-first gap: most competitors are mobile-native.

### 🏆 1. 习惯追踪 (streak.ljding.app)

- **中文名**: 习惯追踪
- **English Name**: Habit Streak Tracker with AI Coaching
- **Purpose**: Web-first habit accountability with AI micro-coaching. Daily check-ins for health habits, streak visualization, AI-generated nudges.
- **Why underserved**: Existing tools (Habitica, Streaks) are mobile-first. Web apps for habit tracking are sparse. AI coaching on top of streaks is an untapped combination.
- **Key Features**:
  - Daily check-ins for habits (sleep, hydration, exercise, meditation)
  - Streak tracking with visual progress
  - AI-generated micro-coaching tips based on user patterns
  - Weekly progress reports
  - Accountability buddies from hangwith.ljding.app network
- **Ecosystem integration**:
  - learn.ljding.app → "Learn a health topic tied to your active habit"
  - hangwith.ljding.app → share streaks with accountability buddies
- **Monetization**: Free (3 habits), $5/mo Pro (unlimited + AI insights)
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + AI (L7 route or similar)
- **Regulatory risk**: Minimal — wellness coaching, not medical advice
- **Priority**: **High** (strongest ecosystem fit of all health options)
- **Feasibility**: Demand 8 | Complexity 4 | Differentiation 7 | Ecosystem Fit 9 | **Total: 28/40**

### 🏆 2. 补剂档案 (stack.ljding.app)

- **中文名**: 补剂档案
- **English Name**: Supplement & Stack Tracker
- **Purpose**: Log supplement/vitamin stack, track subjective effects over time, get AI interaction warnings.
- **Why underserved**: Most people use spreadsheets. No dominant web-based "track + analyze" tool for supplements. Large Reddit community ready (r/supplements, r/nootropics).
- **Key Features**:
  - Log supplement stack with dosage/timing
  - AI-powered interaction warnings (contraindicated combos)
  - Track subjective effects (energy, sleep, mood) over time
  - Trend analysis: what's actually working
- **Monetization**: Free (5 supplements), $7/mo Pro (unlimited + AI + trends)
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + AI interaction check
- **Regulatory risk**: Low — explicit disclaimers, not medical advice
- **Priority**: **Medium-High** (strong niche, low competition)
- **Feasibility**: Demand 7 | Complexity 5 | Differentiation 8 | Ecosystem Fit 5 | **Total: 25/40**

### 🏆 3. 睡眠债务 (sleepdebt.ljding.app)

- **中文名**: 睡眠债务
- **English Name**: Sleep Debt Dashboard
- **Purpose**: Quantify cumulative sleep debt, project recovery timeline, AI sleep hygiene suggestions.
- **Why underserved**: Sleep trackers are hardware-bundled ($300+ rings). Standalone web dashboard for sleep debt analysis is a gap.
- **Key Features**:
  - Manual sleep logging OR wearable API sync
  - Cumulative sleep debt calculation
  - Recovery projection (how many extra hours to recover)
  - AI sleep hygiene suggestions based on patterns
- **Ecosystem integration**:
  - learn.ljding.app → sleep science educational modules
  - hangwith.ljding.app → "Sleep Recovery Week" social challenges
- **Monetization**: Free (basic), $5/mo (debt calc + trends + wearable sync)
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Wearable API (optional)
- **Regulatory risk**: Minimal
- **Priority**: **Medium-High** (clear ecosystem fit)
- **Feasibility**: Demand 7 | Complexity 4 | Differentiation 7 | Ecosystem Fit 8 | **Total: 26/40**

---

## Updated Recommended Build Sequence (2026-05-07)

| # | App | Subdomain | Domain | Rationale |
|---|-----|-----------|--------|-----------|
| 1 | 记账分摊 | split.ljding.app | Finance | High utility, proven market, direct synergy with 找谁玩 |
| 2 | 室友记 | roommate.ljding.app | Household | High utility, integrates with split |
| 3 | 深度工作 | focus.ljding.app | Productivity | High demand, complements learn.ljding.app |
| 4 | **习惯追踪** | **streak.ljding.app** | **Health** | **NEW — strongest ecosystem fit, lowest complexity** |
| 5 | 冰箱档案 | fridge.ljding.app | Food/Kitchen | Unique web-first gap |
| 6 | **睡眠债务** | **sleepdebt.ljding.app** | **Health** | **NEW — complements sleep science education** |
| 7 | 睡眠档案 | sleep.ljding.app | Health | Existing plan (similar to sleepdebt — consolidate?) |
| 8 | 心情档案 | mood.ljding.app | Health | Feeds into wellness dashboard |
| 9 | **补剂档案** | **stack.ljding.app** | **Health** | **NEW — biohacker niche, low competition** |
| 10 | 食谱本 | recipe.ljding.app | Food/Kitchen | Complements fridge tracker |
| 11 | 身心仪表盘 | wellness.ljding.app | Health | Capstone — ties sleep + mood + activity |
| 12 | 小账本 | pocket.ljding.app | Finance | Spending awareness; complements QuantConnect |
| 13 | 周复盘 | review.ljding.app | Productivity | Aggregation layer — build after core apps |
| 14 | 家务管理 | chore.ljding.app | Household | Long-tail; narrow audience |

---

## Finance Domain Research (2026-05-08)

New research identified three finance opportunities with privacy-first, web-first positioning:

### 1. SubAware (subaware.ljding.app) — Subscription Intelligence Dashboard

- **Purpose**: Track and optimize subscription spend without bank linking
- **Key Insight**: Average person spends $329/mo on 12 subscriptions, underestimates by 2.5x
- **MVP Timeline**: 3-4 weeks (lowest complexity)
- **Priority**: Build first — fastest validation, no Plaid dependency
- **See**: [Full research](./finance-research.md)

### 2. SpendSense (spendsense.ljding.app) — Financial Literacy Through Real Spending

- **Purpose**: Learn personal finance by analyzing your actual spending patterns
- **Key Insight**: Education apps teach theory, budget apps track money — nothing bridges both
- **MVP Timeline**: 4-6 weeks
- **Priority**: Build second — strongest learn.ljding.app integration
- **See**: [Full research](./finance-research.md)

### 3. HouseFund (housefund.ljding.app) — Shared Household Financial Awareness

- **Purpose**: Help households (roommates, couples) build shared financial awareness beyond bill splitting
- **Key Insight**: Splitwise tracks debts, nothing manages shared financial life
- **MVP Timeline**: 6-8 weeks
- **Priority**: Build third — strongest hangwith.ljding.app integration, most complex
- **See**: [Full research](./finance-research.md)

---

*Full research details available in [finance-research.md](./finance-research.md)*

---

## Creativity Domain Research (2026-05-10)

New domain explored — not previously covered. Creativity tools complement learn.ljding.app (mental growth) and hangwith.ljding.app (social connection) by addressing **creative expression and ideation**.

### Key Trends Driving Creativity Tools
1. **Voice interfaces maturing** — Web Speech API reliable cross-browser; voice-first creative tools now viable
2. **Constrained creativity rising** — Wordle proved appetite for daily bounded creative challenges
3. **Lo-fi/ambient explosion** — 14M+ lo-fi Girl subscribers; music tools overwhelmingly complex for casual use
4. **Micro-video dominance** — Loom proved demand; editing remains closed ecosystem or mobile-only
5. **Scene-based editing** — Keynote-style (not Premiere-style) micro-video underexploited on web

### 1. Verse — verse.ljding.app

- **中文名**: 写作约束
- **English Name**: Constrained Creative Writing with Daily Prompts
- **Purpose**: Structured writing tool enforcing creative constraints — daily prompts, word limits, form templates (haiku, six-word memoir, micro-essay) — with anonymous community feed
- **Why NOW**: Wordle proved bounded creativity works. Long-form tools (Notion, Docs) offer freedom when users need guardrails. No web app combines prompts + constraints + community.
- **Key Features**:
  - Daily constrained prompts (word count, form, theme)
  - Anonymous submission feed
  - No account required for MVP
  - learn.ljding.app: writing practice for language learning
  - hangwith.ljding.app: social layer, collaborative constraint chains
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1
- **Priority**: **High** (easiest MVP at 5/5, strongest differentiation)
- **Feasibility**: Demand 7 | Complexity 2 | Differentiation 8 | Ecosystem Fit 8 | **Total: 25/40**

### 2. Riff — riff.ljding.app

- **中文名**: 头脑风暴画布
- **English Name**: Voice-to-Idea-Map Brainstorming Canvas
- **Purpose**: AI-powered brainstorming canvas that turns freeform voice rambles into structured idea maps
- **Why NOW**: Web Speech API mature but no tool bridges voice → organized structure. People think out loud but capture loses translation. Voice-first ideation is genuine whitespace.
- **Key Features**:
  - Voice capture → structured idea map via AI
  - Canvas editor for organizing clusters
  - learn.ljding.app: knowledge gap visualization for students
  - hangwith.ljding.app: group brainstorming with real-time merging
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Web Speech API + LLM API
- **Priority**: **High** (highest ecosystem fit, strong differentiation)
- **Feasibility**: Demand 7 | Complexity 4 | Differentiation 9 | Ecosystem Fit 9 | **Total: 29/40**

### 3. Tone — tone.ljding.app

- **中文名**: Lo-Fi 音乐工作坊
- **English Name**: Lo-fi Loop Creator via Grid Sequencer
- **Purpose**: Web-based sound sketchpad for lo-fi loops and ambient soundscapes — no musical knowledge required
- **Why NOW**: Web Audio API mature but underutilized. Lo-fi is dominant background-audio category. BandLab/Soundtrap are full DAWs — overkill for casual vibe building.
- **Key Features**:
  - Grid sequencer with curated royalty-free samples
  - Loop export for video/study use
  - No musical training needed
  - montage.ljding.app: audio tracks for micro-videos
  - learn.ljding.app: study session background audio
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Web Audio API + Tone.js
- **Priority**: **Medium** (niche but passionate audience)
- **Feasibility**: Demand 6 | Complexity 6 | Differentiation 8 | Ecosystem Fit 7 | **Total: 27/40**

### 4. Montage — montage.ljding.app

- **中文名**: 微视频编辑器
- **English Name**: Scene-Based Micro-Video Editor
- **Purpose**: Browser-based micro-video editor for stitching screen recordings and webcam clips — no timeline, just scenes
- **Why NOW**: Loom proved quick video demand but closed ecosystem. CapCut mobile-first. Scene-based (Keynote-style) editing underexploited on web. Desktop users creating screen content have no good browser option.
- **Key Features**:
  - Scene-based editing (add/reorder/delete scenes)
  - Screen recording + webcam capture
  - Text overlays and annotations
  - Export to MP4 (sub-2-min clips for MVP)
  - learn.ljding.app: lesson recaps from instructors
  - hangwith.ljding.app: video responses in social threads
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + MediaRecorder API + WebCodecs
- **Priority**: **Medium** (highest demand but most complex — defer)
- **Feasibility**: Demand 8 | Complexity 8 | Differentiation 8 | Ecosystem Fit 8 | **Total: 32/40**

---

## Updated Build Sequence (2026-05-10)

| # | App | Subdomain | Domain | Rationale |
|---|-----|-----------|--------|-----------|
| 1 | 记账分摊 | split.ljding.app | Finance | High utility, proven market, direct synergy with 找谁玩 |
| 2 | 室友记 | roommate.ljding.app | Household | High utility, integrates with split |
| 3 | 深度工作 | focus.ljding.app | Productivity | High demand, complements learn.ljding.app |
| 4 | 习惯追踪 | streak.ljding.app | Health | Strongest ecosystem fit, low complexity |
| 5 | **写作约束** | **verse.ljding.app** | **Creativity** | **NEW — easiest MVP (5/5), direct learn synergy** |
| 6 | 冰箱档案 | fridge.ljding.app | Food/Kitchen | Unique web-first gap |
| 7 | 睡眠债务 | sleepdebt.ljding.app | Health | Complements sleep science education |
| 8 | 睡眠档案 | sleep.ljding.app | Health | Existing plan |
| 9 | 心情档案 | mood.ljding.app | Health | Feeds into wellness dashboard |
| 10 | 补剂档案 | stack.ljding.app | Health | Biohacker niche, low competition |
| 11 | 食谱本 | recipe.ljding.app | Food/Kitchen | Complements fridge tracker |
| 12 | **头脑风暴画布** | **riff.ljding.app** | **Creativity** | **NEW — highest ecosystem fit (9/10), voice-first differentiation** |
| 13 | 身心仪表盘 | wellness.ljding.app | Health | Capstone — ties sleep + mood + activity |
| 14 | 小账本 | pocket.ljding.app | Finance | Spending awareness; complements QuantConnect |
| 15 | 周复盘 | review.ljding.app | Productivity | Aggregation layer — build after core apps |
| 16 | Lo-Fi 音乐 | tone.ljding.app | Creativity | Niche but passionate; audio ecosystem build |
| 17 | 微视频编辑 | montage.ljding.app | Creativity | High demand, technically complex — defer |
| 18 | 家居记 | home.ljding.app | Household | Narrower audience; long-tail |

---

## Travel & Trip Planning Domain (Researched 2026-05-13)

> Full research at `travel-research.md`. Travel planning is dominated by booking-first platforms; the actual *planning* and *coordination* layer is fragmented. Web-native, group-first, privacy-conscious travel tools are a genuine whitespace.

### 1. roam.ljding.app — Content-to-Itinerary Converter

- **中文名**: 行程助手
- **English Name**: Turn any travel content into an actionable itinerary
- **Purpose**: Paste a Xiaohongshu post, YouTube video, or blog URL — get a structured itinerary in seconds. Bridges the inspiration-to-plan gap that no current tool addresses.
- **Key Features**:
  - URL-to-itinerary AI extraction (Xiaohongshu, TikTok, YouTube, blogs)
  - Template marketplace — browse and fork community-shared itineraries by destination
  - Smart adaptation — adjust imported plans for your dates, budget, pace, group size
  - Bilingual Chinese/English itinerary output
  - Local tips layer (transit cards, tipping, SIM cards)
  - Export to Google Calendar, Apple Calendar, PDF, or shareable link
  - learn.ljding.app: destination language/culture lessons surfaced
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare Workers (LLM content parsing) + D1
- **Priority**: **Tier 1 — Build First** (lowest complexity, unique hook)
- **Feasibility**: Demand 8 | Complexity 2 | Differentiation 8 | Ecosystem Fit 7 | **Total: 25/30**

### 2. trip.ljding.app — Collaborative Group Trip Planner

- **中文名**: 旅行规划
- **English Name**: Group trip planning that actually works for friends
- **Purpose**: Real-time collaborative itinerary builder with group decision tools, shared packing lists, budget splitting, and offline PWA access.
- **Key Features**:
  - Multiplayer itinerary editing (Cloudflare Durable Objects)
  - Group voting on destinations, restaurants, activities
  - Shared availability calendar — find dates that work for everyone
  - Smart packing lists with weather-aware suggestions
  - Per-person and group expense tracking (integrates with split.ljding.app)
  - Offline PWA with cached map tiles
  - Shareable trip links — no account needed to view
  - hangwith.ljding.app: pull friend groups directly
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Durable Objects + Mapbox GL JS
- **Priority**: **Tier 1 — Highest Value** (strongest ecosystem fit, hardest moat)
- **Feasibility**: Demand 8 | Complexity 7 | Differentiation 9 | Ecosystem Fit 9 | **Total: 33/40**

### 3. wander.ljding.app — Private Travel Journal

- **中文名**: 旅行足迹
- **English Name**: Private travel journal and memory keeper
- **Purpose**: Trip timeline from photos (EXIF), check-ins, and notes. World map of everywhere you've been. Privacy-first — nothing public unless you choose.
- **Key Features**:
  - Auto-timeline from photo EXIF data + manual entries
  - World map visualization of travel history
  - Trip stats: countries, distance, cuisines, patterns
  - Selective sharing via hangwith.ljding.app
  - "On this day last year" nostalgia notifications
  - All content private by default; encrypted storage
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + R2 (photo storage)
- **Priority**: **Tier 2 — Completes the lifecycle**
- **Feasibility**: Demand 6 | Complexity 3 | Differentiation 7 | Ecosystem Fit 7 | **Total: 23/30**

### Recommended Build Order

| Rank | App | Rationale |
|------|-----|-----------|
| 1 | **roam.ljding.app** | Fastest MVP (weeks), unique hook, bilingual differentiation, viral by nature |
| 2 | **trip.ljding.app** | Highest long-term value, strongest hangwith synergy, durable moat via group collaboration |
| 3 | **wander.ljding.app** | Completes the lifecycle (plan → journal); best after trip exists |

---

## Updated Build Sequence (All Domains — 2026-05-14)

| # | App | Subdomain | Domain | Rationale |
|---|-----|-----------|--------|-----------|
| 1 | 记账分摊 | split.ljding.app | Finance | High utility, proven market, direct synergy with 找谁玩 |
| 2 | 深度工作 | focus.ljding.app | Productivity | High demand, complements learn.ljding.app |
| 3 | 旅行内容转换 | roam.ljding.app | Travel | Fastest MVP, unique hook |
| 4 | 室友记 | roommate.ljding.app | Household | High utility, integrates with split |
| 5 | 习惯追踪 | streak.ljding.app | Health | Strongest ecosystem fit, low complexity |
| 6 | 写作约束 | verse.ljding.app | Creativity | Easiest MVP (5/5), direct learn synergy |
| 7 | 冰箱档案 | fridge.ljding.app | Food/Kitchen | Unique web-first gap |
| 8 | 睡眠债务 | sleepdebt.ljding.app | Health | Complements sleep science education |
| 9 | 旅行规划 | trip.ljding.app | Travel | Highest ecosystem value, group collaboration moat |
| 10 | 睡眠档案 | sleep.ljding.app | Health | Existing plan |
| 11 | 心情档案 | mood.ljding.app | Health | Feeds into wellness dashboard |
| 12 | 补剂档案 | stack.ljding.app | Health | Biohacker niche, low competition |
| 13 | 食谱本 | recipe.ljding.app | Food/Kitchen | Complements fridge tracker |
| 14 | 头脑风暴画布 | riff.ljding.app | Creativity | Highest ecosystem fit (9/10), voice-first |
| 15 | 旅行足迹 | wander.ljding.app | Travel | Completes lifecycle; post-trip journaling |
| 16 | 身心仪表盘 | wellness.ljding.app | Health | Capstone — ties sleep + mood + activity |
| 17 | 小账本 | pocket.ljding.app | Finance | Spending awareness; complements QuantConnect |
| 18 | 周复盘 | review.ljding.app | Productivity | Aggregation layer — build after core apps |
| 19 | Lo-Fi 音乐 | tone.ljding.app | Creativity | Niche but passionate; audio ecosystem build |
| 20 | 微视频编辑 | montage.ljding.app | Creativity | High demand, technically complex — defer |
| 21 | 家居记 | home.ljding.app | Household | Narrower audience; long-tail |
| 22 | 家庭看板 | family.ljding.app | Parenting | **NEW — broadest parenting audience, strongest hangwith synergy** |
| 23 | 成长地图 | grow.ljding.app | Parenting | **NEW — highest differentiation, bilingual milestone bridge** |
| 24 | 宝贝日志 | baby.ljding.app | Parenting | High demand, shares data model with GrowthMap |
| 25 | 时光册 | moments.ljding.app | Parenting | Most emotionally resonant, highest technical complexity |

---

## Parenting & Family Domain (Researched 2026-05-14)

> New domain — not previously explored. Addresses family coordination, child development tracking, and cross-border bilingual family sharing. Complements learn.ljding.app (learning) and hangwith.ljding.app (social) with a **family** layer. Key insight: no competitor offers web-first + privacy-conscious + bilingual (Chinese-English) + simple + ad-free.

### Key Market Gaps
- **Privacy-first family coordination** — existing tools are either ad-heavy (Cozi) or surveillance-heavy (FamilyWall, Life360)
- **Chinese diaspora bilingual tools** — 10M+ Chinese families in US/Canada with no web tool bridging both languages
- **Cultural milestone integration** — Chinese celebrations (百日宴, 抓周) absent from all Western apps
- **Cross-border sharing** — sharing with grandparents in China without using mainland-China-hosted services

### 1. 家庭看板 (family.ljding.app)

- **中文名**: 家庭看板
- **English Name**: FamilyBoard — Shared Family Task & Chore Board
- **Purpose**: A privacy-first, kanban-style family coordination board for chores, schedules, and daily coordination. No GPS, no surveillance — just shared visibility.
- **Key Features**:
  - Shared kanban board: Today / This Week / To-Do / Done columns
  - Quick-add tasks with assignee and optional due date
  - Recurring tasks (trash day, piano practice)
  - Simple meal plan row — "what's for dinner" without recipe complexity
  - Bilingual UI (Chinese/English) for grandparents
  - No location tracking, no screen time monitoring
  - Optional daily digest via shareable link
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + WebSockets
- **Priority**: **Tier 1 — Build First** (broadest audience, lowest content requirement)
- **Feasibility**: Demand 8 | Complexity 4 | Differentiation 8 | Ecosystem Fit 8 | **Total: 28/40**

### 2. 成长地图 (grow.ljding.app)

- **中文名**: 成长地图
- **English Name**: GrowthMap — Bilingual Developmental Milestone Tracker
- **Purpose**: Track child milestones with bilingual guidance bridging Western WHO and Chinese pediatric frameworks. Includes age-appropriate activity suggestions in both languages.
- **Key Features**:
  - Visual milestone timeline: motor, language, cognitive, social-emotional
  - Bilingual milestone descriptions (WHO + Chinese pediatric context)
  - "What to try this week" — 2-3 bilingual activity suggestions
  - Cultural milestone integration (百日宴, 抓周, first haircut traditions)
  - Photo + note journal per milestone
  - Shareable visual timeline for grandparents
  - Anti-anxiety design: "every child develops at their own pace"
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + R2
- **Priority**: **Tier 1 — Highest Differentiation** (bilingual milestone bridge is genuinely unique)
- **Feasibility**: Demand 7 | Complexity 4 | Differentiation 9 | Ecosystem Fit 9 | **Total: 29/40**

### 3. 宝贝日志 (baby.ljding.app)

- **中文名**: 宝贝日志
- **English Name**: BabyLog — Privacy-First Baby Tracking
- **Purpose**: One-tap logging for feed, sleep, diaper, and milestones. Works offline, no account required to start, caregiver sharing via unique link.
- **Key Features**:
  - One-tap logging: breast/bottle/solid feed, sleep, diaper, medication
  - Offline-first via service worker; syncs when online
  - Shareable caregiver link — no account needed to view or log
  - Bilingual UI toggle with bilingual milestone descriptions
  - Growth charts (height/weight/head) with percentile curves
  - Daily/weekly summary: "today baby ate X times, slept Y hours"
  - Chinese cultural milestones (百日, 抓周) included
  - JSON/CSV export; data in Cloudflare D1 under user control
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Service Workers
- **Priority**: **Tier 2** (build after GrowthMap to share data model)
- **Feasibility**: Demand 9 | Complexity 3 | Differentiation 7 | Ecosystem Fit 7 | **Total: 26/40**

### 4. 时光册 (moments.ljding.app)

- **中文名**: 时光册
- **English Name**: MomentsBook — Private Family Photo Journal
- **Purpose**: Ad-free, bilingual family photo journal with cross-border sharing optimization. No social media, no upsells — just private family memories.
- **Key Features**:
  - Chronological photo journal with child age auto-calculation
  - Private sharing via link — no viewer account needed (grandparents just bookmark)
  - Bilingual captions — English with optional Chinese translation
  - CDN optimized for slow China connections
  - Simple reactions (❤️) for viewer engagement
  - No ads, no print shop, no merchandise upsells
  - PDF yearbook export for local printing
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + R2 + Images
- **Priority**: **Tier 2** (highest technical complexity — image pipeline)
- **Feasibility**: Demand 8 | Complexity 5 | Differentiation 7 | Ecosystem Fit 6 | **Total: 26/40**

### Parenting Domain Recommended Build Order

| Rank | App | Score | Rationale |
|------|-----|-------|-----------|
| 1 | 家庭看板 (family.ljding.app) | 28 | Broadest audience, establishes family data model, fastest to MVP |
| 2 | 成长地图 (grow.ljding.app) | 29 | Highest differentiation, bilingual white space, content layer on family model |
| 3 | 宝贝日志 (baby.ljding.app) | 26 | High demand, shares child profile model with GrowthMap |
| 4 | 时光册 (moments.ljding.app) | 26 | Most emotionally resonant; build last for image pipeline maturity |

---

*Full creativity research available in [creativity-research.md](./creativity-research.md)*
*Full travel research available in [travel-research.md](./travel-research.md)*
*Full parenting research available in [parenting-research.md](./parenting-research.md)*

---

## Social Accountability / Habit Accountability Apps (Researched 2026-05-17)

> New domain — bridges the gap between personal habit tracking and social accountability. The habit tracking market is $14.94B (2026) growing to $50.21B by 2035. Social accountability achieves 76% success vs 43% solo (StickK data). Key gap: no web-first, privacy-focused, Chinese-bilingual accountability app exists.

### Recommended Build Order

|| Rank | App | Subdomain | MVP Ease | Rationale |
||------|-----|-----------|----------|-----------|
|| 1 | 打卡圈 (DǎKǎ Quān) | daka.ljding.app | 5/5 | Lowest complexity, highest demand (打卡 culture), natural viral invite loop, privacy-first differentiator |
|| 2 | 督伴 (DūBàn) | duban.ljding.app | 3/5 | 1:1 accountability partner matching with configurable stakes, builds on daka infrastructure |

### Tier 2: Explore Later

|| Rank | App | Subdomain | MVP Ease | Rationale |
||------|-----|-----------|----------|-----------|
|| 3 | 共进 (GòngJìn) | gongjin.ljding.app | 3/5 | Couples/family goal sync — highest differentiation but smaller target audience |
|| 4 | 约定 (YuēDìng) | yuedin.ljding.app | 2/5 | Commitment contracts with payment stakes — most complex, best as premium layer |
|| 5 | 醒我 (XǐngWǒ) | xingwo.ljding.app | 2/5 | Wake-up accountability — niche focus, good integration with sleep.ljding.app |

*Full social accountability research available in [social-accountability-research.md](./social-accountability-research.md)*
