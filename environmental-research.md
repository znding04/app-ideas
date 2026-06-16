# Environmental / Green Living Research — Session 17 (2026-06-03)

## Research Focus
Carbon footprint tracking, sustainable living, eco-friendly product discovery, cross-border green living for Chinese-American diaspora.

---

## Key Findings

### Gap 1: Food Carbon — Meal-Level Granularity
Most apps track broad food categories (beef vs. vegetables) but miss supply chain nuance: seasonal vs. out-of-season produce, local vs. imported, packaging type, frozen vs. fresh. A PWA could use receipt/barcode scanning for per-meal emissions with ingredient-level granularity.

### Gap 2: Travel Carbon — Multimodal Trip Tracking
Travel tracking typically asks users to manually log "a flight" or "a drive." Misses mixed-mode trips (drive to train station, train to city, rideshare to hotel), layover routing inefficiencies, vehicle-specific factors. A PWA with geolocation + mapping APIs could passively detect transport mode switches.

### Gap 3: Household Utility Disaggregation
Current apps pull monthly bills and assign flat carbon numbers. They don't show which behaviors drive consumption — heating schedules, appliance usage, standby loads. Green Button data standard could power hourly consumption → real-time carbon intensity mapping.

### Gap 4: Supply Chain Transparency (EN/ZH)
No bilingual app lets diaspora families scan a product (Taobao, Amazon, 99 Ranch) and see a unified sustainability score covering both US and China supply chains. Existing tools (Good On You, HowGood) are English-only, US-centric, don't index Chinese manufacturers or certifications (China Environmental Labeling / 中国环境标志).

### Gap 5: Cross-Border Green Product Discovery
No cross-border "green registry" for diaspora families to find verified eco-friendly products they buy/send between US and China — baby formula, health supplements, skincare, household goods. Parents on Pinduoduo/JD importing from US lack bilingual ingredient/material breakdowns and eco-cert equivalences (EPA vs. MEE standards).

### Gap 6: Carbon Footprint for China Travel
No app calculates full carbon cost of US-China family trips (transpacific flights, domestic 高铁/ flights, hotel stays) with culturally relevant offsets — e.g., reforestation projects in ancestral province, 高铁 vs. domestic flight comparison with real-time Chinese rail data. Existing carbon trackers (MyClimate, Wren) don't integrate China's domestic transport APIs.

---

## App Concepts Generated

| # | Name (EN/ZH) | Subdomain | One-Line Pitch | Key Differentiator | Feasibility |
|---|---|---|---|---|---|
| 1 | **GreenBridge / 绿桥** | `greenbridge.ljding.app` | Track and offset carbon footprint for transpacific travel, including flights, logistics, and family shipments to/from China. | Pre-built carbon models for popular US–China routes (LAX↔PVG, SFO↔PEK) plus haul-shipping & care-package offsets. | 4 |
| 2 | **LüWu / 绿屋 (Green Home)** | `luwu.ljding.app` | Zero-waste household tracker tailored for Chinese-American kitchens — log food waste, track reusable container cycles, culturally relevant tips. | Waste categories and meal-planning calibrated to Chinese-American grocery habits (99 Ranch runs, Asian produce shelf-life). | 5 |
| 3 | **ClearSource / 清源** | `clearsource.ljding.app` | Scan product barcode to see full supply-chain story — factory location, labor rating, environmental certifications — bridging CN manufacturing data with US retail. | Bilingual integration with Chinese regulatory databases (企查查/天眼查 APIs) and US certifications (EPA, USDA Organic). | 2 |
| 4 | **HaoPin / 好品 (Good Goods)** | `haopin.ljding.app` | Cross-border discovery platform for verified green products from US indie brands and vetted Chinese DTC brands, with consolidated shipping. | Curated bilingual marketplace merging US "clean beauty/zero-waste" brands with CN-originated sustainable alternatives, plus group-buy (拼团). | 3 |
| 5 | **GreenCircle / 绿圈** | `greencircle.ljding.app` | Community sustainability challenges for Chinese-American families and hometown associations — compete on energy savings, composting streaks, neighborhood cleanups. | WeChat Mini-Program companion + English-first mobile app so grandparents and grandkids can participate; leaderboards tied to real community orgs (同乡会, church groups). | 4 |

---

## Bilingual EN/ZH Opportunities (Diaspora-Specific)

1. **Supply chain certificates**: 中国环境标志 (China Environmental Labeling) ↔ EPA Energy Star — no tool bridges these for consumers
2. **跨国家庭碳核算**: Households sending care packages (海运/空运), visiting family (过年回家), importing from Taobao/JD — unique carbon footprint patterns
3. **Culturally relevant offsets**: Tree planting in ancestral province (e.g., 广西, 福建) vs. generic carbon credits
4. **Green product discovery for Chinese grocery habits**: Products from 99 Ranch, H Mart, Taobao, JD, WeChat Mall — none have eco-scores in one place

---

## Monetization Options
- Freemium: carbon calculator free, offset purchases + premium route data paid
- Marketplace affiliate: HaoPin takes commission on verified green product sales
- B2B: enterprise carbon tracking for small businesses importing from China
- White-label: sustainability reports for Chinese-American community organizations

## Web-First PWA Feasibility
- Carbon calculators: highly feasible as PWA, no native APIs needed
- Barcode scanning: browser camera API supports this natively
- China domestic transport data: public 高铁 APIs available
- Smart meter integration: Green Button data standard is web-accessible
- Cross-border product database: most complex, requires ongoing data curation