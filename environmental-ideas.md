# LüWu / 绿屋 (Green Home) — App Concept

**Domain:** Environmental / Green Living
**Subdomain:** luwu.ljding.app
**Score:** 18/20
**Status:** Recommended #1 Environmental App
**Session:** 17 — 2026-06-03

## One-Line Pitch
Zero-waste household tracker tailored for Chinese-American kitchens — log food waste, track reusable container cycles, and get culturally relevant tips (bulk tea sourcing, tofu-container reuse, etc.).

## Key Differentiator
Waste categories and meal-planning suggestions calibrated to Chinese-American grocery habits (99 Ranch runs, Asian produce shelf-life, tofu-container reuse), not generic Western diets.

---

## Concept Details

### Problem It Solves
Chinese-American households generate food waste patterns that Western apps don't understand:
- Bulk produce from Asian grocery stores (99 Ranch, H Mart, Great Wall) with different shelf-life characteristics
- Reusable container systems common in Chinese cooking (tiffin boxes for dim sum leftovers, tofu container reuse)
- Cultural foods with specific waste streams (rice cooker overflow, fish bones, bok choy stems)
-跨国家庭 food shipping (care packages from China with packaging waste)

### Core Features (MVP)
1. **Food Waste Logger** — Quick-entry waste logging with Chinese food categories (青菜,豆腐,肉类,海鲜,点心)
2. **Reusable Container Tracker** — Track container cycles (lunch box → home → wash → reuse)
3. **Smart Tips Engine** — Culturally relevant zero-waste tips:
   - "Your bok choy stems can be pickled in 2 days"
   - "Tofu container → seed starter (follow this guide)"
   - "Rice overflow → crispy rice recipe"
4. **Kitchen Carbon Dashboard** — Weekly/monthly carbon saved by waste reduction
5. **Shopping Helper** — Predict produce shelf-life based on Chinese grocery patterns

### Bilingual EN/ZH Features
- Full Chinese food category taxonomy
- Chinese recipe suggestions for reducing waste
- Bilingual tips and educational content
- Chinese calendar integration for festival food waste tracking (春节, 中秋)

### Tech Stack (Recommended)
- **Frontend:** Vue 3 + Vite PWA
- **Storage:** Local-first (IndexedDB) + optional cloud sync
- **Charts:** D3.js for carbon visualization
- **Notifications:** Service Worker for shopping reminders

### Monetization
- Free: Core tracking + 50 logs/month
- $5/mo: Unlimited logs + smart tips + kitchen carbon dashboard + data export
- $8/mo: Family multi-user + cross-device sync + premium tips library

### Ecosystem Integration
- Complements learn.ljding.app (sustainable living content courses)
- Could feed food waste data into GreenBridge's household carbon model
- Works standalone as first environmental entry point

### Build Time
3-4 weeks MVP

### Competitive Landscape
- **Olio** (UK-based, Western food focus) — no Chinese food categories
- **NoWaste** (generic food tracker) — no cultural calibration
- **FoodKeeper** (USDA app) — English only, US-centric, no waste tracking
- **ClearMetal** (supply chain) — B2B, not consumer

### White Space
No app combines:
1. Chinese-American kitchen waste tracking
2. Reusable container cycle management
3. Culturally relevant zero-waste recipe suggestions
4. Bilingual EN/ZH throughout

## Research Sources
- environmental-research.md (session 17)
- food-kitchen-research.md (session 10) — overlaps with food waste tracking

## Next Steps
1. Survey Chinese-American households about food waste pain points
2. Build Chinese food category taxonomy
3. Create culturally relevant zero-waste tip database
4. Design reusable container tracking UX