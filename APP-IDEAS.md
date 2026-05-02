# ljding.app App Ideas

> Research-backed app opportunities for the ljding.app ecosystem — updated 2026-05-02

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

The current ecosystem covers **social tracking** (找谁玩) and **entertainment** (玩点啥) + **learning** (学点啥). What's missing:

1. **Daily life utilities** — expense tracking, bill splitting, bookmarks
2. **Emotional wellness** — mood tracking, gratitude/journaling
3. **Personal knowledge management** — reading lists, link vaults
4. **Finance** — portfolio/investment tracking (user already does QuantConnect)

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

## Appendix: Ideas Considered but Not Included

- **AI Writing Assistant** — crowded market (Claude, ChatGPT); hard to differentiate
- **Password Manager** — security complexity too high for MVP; trust barrier
- **Habit Tracker** *(previously suggested)* — solid idea but overlaps with 找谁玩's retention mechanics; mood tracker fills emotional wellness gap instead
- **World Clock** *(previously suggested)* — useful but too narrow for a full app
- **Portfolio Tracker (SOXL, etc.)** — user already has QuantConnectProjects for this
