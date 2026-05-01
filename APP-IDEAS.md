# ljding.app App Ideas

## Existing Apps

1. **找谁玩** (hangwith.ljding.app) — Friend hangout tracker
2. **玩点啥** (arcade.ljding.app) — Game arcade

Both built with: **Vue 3 + Vite + TailwindCSS + Cloudflare Workers/Pages**

---

## Suggested New Apps

### 1. 记账本 (expense.ljding.app)

- **中文名**: 记账本
- **English Name**: Expense Tracker
- **Purpose**: Track daily expenses, manage budgets, and visualize spending habits
- **Key Features**:
  - Quick expense entry with category selection (food, transport, entertainment, etc.)
  - Monthly budget setting and progress tracking
  - Pie/bar charts showing spending distribution
  - Search and filter expense history
  - Data export to CSV
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 (SQLite) + Chart.js
- **Priority**: **High**
- **Why**: Essential daily utility, complements the "life management" theme. Easy to build with D1 database. High utility-to-effort ratio. Appeals to broad audience.

---

### 2. 习惯圈 (habits.ljding.app)

- **中文名**: 习惯圈
- **English Name**: Habit Tracker
- **Purpose**: Build and track daily habits with streaks and accountability
- **Key Features**:
  - Create custom habits with frequency (daily, weekly, custom days)
  - Streak tracking with visual calendar heatmap
  - Daily check-in with one tap
  - Weekly/monthly progress statistics
  - Habit categories and tagging
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 + Vue reactivity
- **Priority**: **High**
- **Why**: Popular Productivity category (competes with Habitica, Loop Habit Tracker). Strong retention mechanics with streaks. Vue + D1 is perfect fit. Good synergy with 找谁玩 (social accountability).

---

### 3. 世界时钟 (timezone.ljding.app)

- **中文名**: 世界时钟
- **English Name**: World Clock
- **Purpose**: Track multiple time zones for remote work and international coordination
- **Key Features**:
  - Add/remove cities with search
  - Analog and digital clock display options
  - Meeting planner: find overlapping free time across zones
  - Daylight saving time auto-adjustment
  - Quick copy time to clipboard
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare KV (for storing user city preferences)
- **Priority**: **Medium**
- **Why**: Essential tool for remote workers with international contacts. Low maintenance, high utility. Quick to build. Good showcase of Cloudflare KV.

---

### 4. 随机决定器 (random.ljding.app)

- **中文名**: 随机决定器
- **English Name**: Random Picker / Decision Maker
- **Purpose**: Break decision paralysis with random selection tools
- **Key Features**:
  - Wheel spinner with customizable options
  - Dice roller (D4, D6, D8, D10, D12, D20)
  - Coin flip
  - Random name/group picker (great for teams)
  - Shuffle list randomizer
  - Save and reuse decision sets
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + CSS animations + Cloudflare Pages
- **Priority**: **Medium**
- **Why**: Simple, fun, and shareable. Low development time, high engagement potential. Complements the "玩" (play/entertainment) theme of arcade.ljding.app. Good starter project.

---

### 5. 快手菜谱 (recipes.ljding.app)

- **中文名**: 快手菜谱
- **English Name**: Quick Recipes
- **Purpose**: Discover and store quick, simple recipes for busy people
- **Key Features**:
  - Browse recipes by category (breakfast, lunch, dinner, snacks)
  - Filter by cooking time (<15min, <30min, <1hr)
  - Search ingredients to find matching recipes
  - Save favorites with local storage
  - Step-by-step cooking mode
  - Serving size adjustment
- **Tech Stack**: Vue 3 + Vite + TailwindCSS + Cloudflare D1 (for recipe database)
- **Priority**: **Low**
- **Why**: Good daily utility but requires content (recipe data). Could be enhanced with AI-generated recipes later. Medium effort for MVP. Useful for lifestyle brand building.

---

## Recommended Next Build

### 🏆 习惯圈 (habits.ljding.app)

**Justification:**

1. **High utility + engagement**: Habit tracking apps have strong retention (streaks create daily return visits)
2. **Perfect tech match**: Vue 3 reactivity for state management, D1 for persistent data
3. **Quick to build**: No complex APIs needed, pure frontend + database
4. **Synergy with existing apps**: Social accountability features could link back to 找谁玩
5. **Proven market**: Habit tracking is a top-performing productivity category
6. **Differentiation**: Most habit apps are mobile-first; a clean web version fills a gap

**Estimated time**: 1-2 weekends for full MVP

**Follow-up opportunity**: Add social features (share streaks, friend challenges) to tie into 找谁玩 ecosystem.

---

## Appendix: Tech Stack Summary

All new apps can use:

| Layer | Technology |
|-------|------------|
| Frontend | Vue 3 + Composition API |
| Build | Vite |
| Styling | TailwindCSS 3.x or 4.x |
| Routing | Vue Router |
| Backend | Cloudflare Workers / Pages |
| Database | Cloudflare D1 (SQLite) or KV |
| Deployment | `wrangler deploy` |

This keeps the entire ljding.app ecosystem **consistent, maintainable, and fast**.
