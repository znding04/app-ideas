# Home Services Domain — App Concepts for ljding.app

**Domain:** Home Services for Chinese Diaspora
**Session:** 26 (2026-06-15)
**Author:** Hermes Agent (cron job)
**Context:** Ecosystem: learn.ljding.app, hangwith.ljding.app | Stack: Vue 3 + Vite + TailwindCSS + Cloudflare Workers/D1

---

## Domain Overview

Chinese diaspora homeowners face a unique set of home services challenges:
- **Language barrier with contractors** — vetting, instructing, and billing in English is a constant friction point
- **Cultural unfamiliarity** — first-generation homeowners unfamiliar with US systems (HOA, home insurance, contractor licensing)
- **Bilateral living** — families shuttling between US and China leave homes unattended for months
- **Elder care at home** — aging parents who split time between countries need culturally competent care
- **Culturally-specific needs** — Chinese-speaking contractors, culturally appropriate meal prep, TCM-aware caregivers
- **High home ownership rate** — Chinese Americans have high homeownership rates (67% vs. 65% national average per 2023 Census data), creating a large addressable market

**Existing solutions:** Thumbtack, Angi (Angie's List), TaskRabbit — English-only, no Chinese language support, no diaspora-specific features.

---

## App Concepts

### Concept 1: 找工 (ZhǎoGōng) — Culturally-Vetted Handyman Marketplace

**Subdomain:** zhaogong.ljding.app

**One-line pitch:** A bilingual (EN/ZH) marketplace connecting Chinese homeowners with Chinese-speaking, background-checked contractors — from HVAC to landscaping to handyman jobs.

**Why NOW:**
- Contractor language barrier is the #1 pain point for Chinese homeowners (Chinese contractors who speak English well are rare outside major metros)
- Post-2020 home improvement boom continues — HomeAdvisor/Thumbtack report sustained high demand
- Growing pipeline of Chinese homeowners who need services but can't vet contractors in English
- No web-first bilingual marketplace exists — Chinese-language options are fragmented WeChat groups with no vetting

**MVP Scope:**
- Contractor profile builder (bilingual bio, trade, service area, hourly rate, insurance status)
- Bilingual job posting (describe your issue in EN or ZH, get matched to nearby contractors)
- Background check integration (Justice Giuliano API or similar)
- In-app messaging (bilingual)
- Simple escrow payment hold (funds released after job completion)
- 3-5 star rating system with EN/ZH reviews

**Ecosystem Fit:**
- **learn.ljding.app:** "Home Maintenance 101" course (U.S. homeownership basics, seasonal maintenance calendar)
- **hangwith.ljding.app:** Neighborhood groups organized by city/ZIP for local contractor recommendations; "ZhǎoGōng Verified" badge for vetted contractors

**Feasibility: 4/5**
- Marketplace mechanics are proven (Thumbtack, Angi). MVP covers: profile CRUD + job posting + messaging + ratings. Payment escrow is the complex piece but Stripe handles it. 4-5 weeks MVP.

**Differentiation: 5/5**
- No bilingual (EN/ZH) contractor marketplace exists. WeChat groups provide no vetting, no reviews, no payment protection. Thumbtack/Angi are English-only. Clear white space.

**Monetization: 4/5**
- 10% service fee on job value (marketplace standard). Featured contractor profiles ($20/mo). Insurance verification verification as premium feature ($5/mo). Strong LTV — contractors are repeat users.

**Ecosystem Fit: 5/5**
- Strongest community integration: hangwith neighborhood groups provide organic network effects for local contractors. learn.ljding.app content drives users into homeownership. Privacy-first fits ecosystem values.

**Total Score: 18/20**

---

### Concept 2: 守家 (ShǒuJiā) — Empty Home Guardian for Shuttle Families

**Subdomain:** shoujia.ljding.app

**One-line pitch:** A monitoring and coordination hub for Chinese families that spend months at a time in China, leaving their US homes unattended — alerts for leaks, breaks, temperature extremes, and trusted neighbor check-ins.

**Why NOW:**
- Families shuttling between US and China (common among 1.5-generation immigrants, professors, businesspeople) face genuine home security and maintenance gaps
- No tool combines environmental monitoring alerts + neighbor coordination + family sharing in one bilingual interface
- Smart home devices (Ring, Nest, SmartThings) exist but are scattered and require multiple apps in English only
- Home insurance claims from frozen pipes, water damage during extended absences are a real cost

**MVP Scope:**
- Multi-device status dashboard (Ring/Nest/SmartThings via Matter API, or simple WiFi sensors)
- Alert engine: temperature drop → frozen pipe warning, humidity spike → leak detection, motion → security alert
- Trusted contact network: invite 2-5 neighbors/friends as backup monitors with their own simplified alert dashboard
- Bilingual status feed (check your home status at a glance in EN or ZH)
- One-tap to emergency contacts (locksmith, plumber, trusted contractor from ZhǎoGōng)
- Family share: multiple family members can view status (adult children in US while parents in China)

**Ecosystem Fit:**
- **learn.ljding.app:** "Empty Home Management" guide — seasonal checklists, smart home setup guide
- **hangwith.ljding.app:** Neighbor network is the social graph — invites to trusted contacts come from hangwith social connections. Families can coordinate who checks what.

**Feasibility: 3/5**
- Device integration (Ring/Nest/SmartThings APIs) adds complexity. SmartThings/Matter has good API coverage but device diversity is a challenge. Fallback: manual sensor input. 5-6 weeks MVP. Reduced version could be 3-4 weeks with just camera integration.

**Differentiation: 5/5**
- No tool targets the "empty home" problem for international shuttle families. Most solutions focus on smart home automation, not family coordination across borders. Bilingual interface for parents is the key differentiator.

**Monetization: 4/5**
- $6/mo for multi-device hub + unlimited trusted contacts + alert history. $10/mo for premium (expert emergency dispatch, insurance claim documentation pack). Strong emotional value justifies premium.

**Ecosystem Fit: 5/5**
- Most culturally specific concept in the portfolio — directly serves the shuttle family lifestyle unique to Chinese diaspora. Strong emotional resonance with guilt-free travel.

**Total Score: 17/20**

---

### Concept 3: 家护 (JiāHù) — Bilingual In-Home Elder Care Coordination

**Subdomain:** jiahu.ljding.app

**One-line pitch:** A bilingual (EN/ZH) coordination platform for families managing in-home elder care — connecting families with Chinese-speaking caregivers, tracking care plans, and sharing updates across family members.

**Why NOW:**
- Chinese American families often care for aging parents at home, balancing work + caregiving across multiple households and time zones
- Professional caregiving agencies (Honor, CareLinx, Kindred at Home) serve this market but have limited Chinese language support
- Family caregivers need: caregiver vetting, care schedule coordination, medication reminders, care log sharing across family members
- No bilingual web-first coordination tool exists for this

**MVP Scope:**
- Caregiver directory: vetted Chinese-speaking in-home caregivers organized by city/specialty (dementia, post-op, mobility)
- Care schedule builder: weekly schedule with caregiver assignments, family coverage
- Care log: daily entries (meals, medication, activities, mood) — photo + text, timestamped
- Family sharing: multi-member family can view and contribute to care log
- Medication reminder system (push notifications + SMS fallback)
- Care plan document builder: physician instructions + daily routines in one shareable PDF

**Ecosystem Fit:**
- **learn.ljding.app:** Caregiving certification courses, TCM vs. Western medicine comparison modules
- **hangwith.ljding.app:** Family coordination circles (already built for 共进 GòngJìn), can extend to caregiving groups
- **ShǒuJiā (守家):** If elderly parents live alone, ShǒuJiā monitors their home while JiāHù manages their care

**Feasibility: 4/5**
- CRUD + scheduling + family sharing + medication reminders. No complex real-time features. Standard web stack. 4-5 weeks MVP.

**Differentiation: 4/5**
- Honor and CareLinx focus on matching but don't do care coordination + family sharing + bilingual in one tool. Chinese-language alternatives are WeChat groups with no structure. Clear gap fill.

**Monetization: 4/5**
- $8/mo per family (caregiver coordination + family sharing). Premium: AI-generated care insights + physician report generator ($12/mo). Family caregivers are highly motivated and emotionally invested.

**Ecosystem Fit: 5/5**
- Strong cultural fit for Chinese family values ( filial piety, family-centered care). Bridges ShǒuJiā (empty home monitoring) and 共进 GòngJìn (family goal sync). Deep integration potential.

**Total Score: 17/20**

---

### Concept 4: 好屋 (HǎoWū) — New Homeowner Onboarding Companion

**Subdomain:** haowu.ljding.app

**One-line pitch:** A bilingual (EN/ZH) guided onboarding companion for first-time Chinese American homeowners — demystifies HOA rules, home insurance, property taxes, and seasonal maintenance with checklists tailored to your home type and climate zone.

**Why NOW:**
- First-generation homeowners face a steep learning curve: HOA rules, home insurance claims, property tax appeals, seasonal maintenance schedules — entirely new territory vs. renting
- Existing resources are in English-only PDFs from government websites (IRS, HUD, local assessor offices) with no translation
- No app combines: what-to-do-when-you-close + seasonal checklists + document organizer + local agency directory in bilingual format
- Post-pandemic homeownership surge (2020-2024) created millions of first-time homeowners who are now hitting their 1-2 year mark (the hardest period)

**MVP Scope:**
- Closing checklist: documents to collect, utility transfers, insurance setup, first-year calendar
- Seasonal maintenance calendar: climate-zone-specific seasonal tasks (winterize, clean gutters, service HVAC, etc.)
- HOA guide builder: enter your HOA rules document → get a bilingual summary + FAQ + key deadlines
- Document vault: store and organize your mortgage statements, insurance policies, tax bills, contractor receipts
- Local agency directory: city-specific links to assessor, utilities, waste management, HOA management company
- Property tax appeal tracker: deadlines + guides for your state

**Ecosystem Fit:**
- **learn.ljding.app:** Homeownership course (U.S. housing system, mortgage basics, insurance 101) — forms a natural content partnership. ZhǎoGōng contractor integration for recommended maintenance providers.
- **hangwith.ljding.app:** Neighborhood homeowner groups, local recommendations, first-year homeowner support circles

**Feasibility: 5/5**
- Content-driven app with checklist logic and document storage. No complex integrations. IndexedDB for vault, simple scheduling UI. 3-4 weeks MVP — the simplest home services concept.

**Differentiation: 4/5**
- No bilingual homeownership onboarding tool exists. Most apps focus on mortgage applications (Notion, Zillow) not post-purchase education. This fills the post-close gap.

**Monetization: 3/5**
- Free core covers all basic onboarding. Premium ($5/mo) for unlimited document vault + property tax appeal tracker + advanced local guides. Lower ceiling than other concepts but large user base.

**Ecosystem Fit: 5/5**
- Gateway app — first-time homeowners become learn.ljding.app users AND ZhǎoGōng customers AND ShǒuJiā users. Strongest ecosystem integration of all concepts. Bridges renting → owning lifecycle.

**Total Score: 17/20**

---

## Summary Scoring Table

| Rank | App | Subdomain | Feasibility | Differentiation | Monetization | Ecosystem Fit | **Total** |
|------|-----|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 1 | **找工 (ZhǎoGōng)** | zhaogong.ljding.app | 4 | 5 | 4 | 5 | **18** |
| 2 | **守家 (ShǒuJiā)** | shoujia.ljding.app | 3 | 5 | 4 | 5 | **17** |
| 2 | **家护 (JiāHù)** | jiahu.ljding.app | 4 | 4 | 4 | 5 | **17** |
| 2 | **好屋 (HǎoWū)** | haowu.ljding.app | 5 | 4 | 3 | 5 | **17** |

---

## Scoring Rationale

### 找工 (ZhǎoGōng) (18/20) — Recommended #1 Home Services App
- **Feasibility 4/5**: Marketplace mechanics are proven. MVP: profile CRUD + job posting + messaging + ratings. Payment escrow via Stripe. 4-5 weeks. No novel ML needed.
- **Differentiation 5/5**: No bilingual contractor marketplace exists. WeChat groups are unvetted, no reviews, no payment protection. Thumbtack/Angi are English-only. Zero direct competitors in this space.
- **Monetization 4/5**: 10% marketplace fee is standard. Featured profiles ($20/mo). Insurance verification as premium ($5/mo). Contractors are repeat users → strong LTV.
- **Ecosystem Fit 5/5**: hangwith neighborhood groups provide organic network effects for local contractors. learn.ljding.app drives first-time users. Privacy-first aligns with ecosystem.

### 守家 (ShǒuJiā) (17/20) — Recommended #2 Home Services App
- **Feasibility 3/5**: Smart home device integration adds complexity (Ring/Nest/SmartThings APIs). SmartThings/Matter helps but device diversity is a challenge. 5-6 weeks. Fallback to manual sensor input reduces scope.
- **Differentiation 5/5**: No tool targets the "empty home" problem for international shuttle families. Most solutions focus on smart home automation, not cross-border family coordination.
- **Monetization 4/5**: $6/mo multi-device hub is reasonable for families spending months away. $10/mo for expert emergency dispatch is justified by emotional peace-of-mind value.
- **Ecosystem Fit 5/5**: Most culturally specific concept — directly serves the shuttle family lifestyle unique to Chinese diaspora. Strong emotional resonance.

### 家护 (JiāHù) (17/20)
- **Feasibility 4/5**: CRUD + scheduling + family sharing + medication reminders. No complex real-time. Standard web stack. 4-5 weeks.
- **Differentiation 4/5**: Honor/CareLinx do matching; JiāHù does coordination + family sharing + bilingual in one tool. WeChat groups have no structure. Clear gap.
- **Monetization 4/5**: $8/mo per family. Premium AI insights at $12/mo. Emotionally invested users = natural premium conversion.
- **Ecosystem Fit 5/5**: Deeply cultural — serves Chinese family values around elder care. Integrates with ShǒuJiā + 共进 GòngJìn + learn.ljding.app.

### 好屋 (HǎoWū) (17/20)
- **Feasibility 5/5**: Content-driven with checklist logic and document storage. No complex integrations. 3-4 weeks — simplest home services MVP.
- **Differentiation 4/5**: No bilingual homeownership onboarding tool. Fills post-close gap that Zillow/mortgage apps miss.
- **Monetization 3/5**: Free core with premium at $5/mo. Lower ceiling but massive user base makes up for it.
- **Ecosystem Fit 5/5**: Gateway app — first homeowners become learn + ZhǎoGōng + ShǒuJiā users. Bridges the full ownership lifecycle.

---

## Recommended Build Order

1. **好屋 (HǎoWū)** — Easiest MVP (3-4 weeks), broadest appeal, gateway to ecosystem (homeowners → learn + ZhǎoGōng)
2. **找工 (ZhǎoGōng)** — Marketplace is 4-5 weeks, highest differentiation, strongest network effects
3. **家护 (JiāHù)** — Strong cultural fit, builds on family coordination patterns from GòngJìn, 4-5 weeks
4. **守家 (ShǒuJiā)** — Most complex integration (smart home APIs), but unique diaspora angle, 5-6 weeks

---

## Cross-Ecosystem Synergies

- **好屋 → ZhǎoGōng**: Homeowners who need contractors → ZhǎoGōng marketplace
- **好屋 → ShǒuJiā**: New homeowners with smart home setup → ShǒuJiā empty home monitoring
- **家护 ↔ ShǒuJiā**: Elderly parents living alone → JiāHù coordinates care, ShǒuJiā monitors home
- **家护 → 共进 GòngJìn**: Family caregiving circles extend the family goal sync concept
- **ZhǎoGōng → learn.ljding.app**: Recommended contractors from learn's home maintenance course
