# Decision-Making & Planning Domain Research

> Research date: 2026-05-30
> Focus: Personal life decisions beyond productivity/todo — big life choices, trade-off analysis, pros/cons frameworks, life planning, major purchases, career paths, relocation, relationship decisions

---

## Market Landscape

### Existing Tools

**Pros & Cons Apps (Mobile-only)**
- **Pros & Cons - Smart Choices** (iOS/Android): Classic weighted pros/cons lists with AI feedback. Mobile-only, English-only. No decision history or outcome tracking.
- **Pros & Cons: Decision-Maker** (Android): Minimal UI for simple binary decisions. No structured frameworks.

**Decision Journals**
- **Decision Journal App** (decisionjournalapp.com): Logs decisions with reasoning, confidence, and scheduled outcome reviews. iOS-only, English-only. Good concept but minimal framework support — it's a journal, not a decision engine.
- **Decision Log** (thedecisionlog.com): AI-powered, applies mental models (5 Whys, Pre-Mortem, Second-Order Thinking). Web-based but requires account. English-only. Closest competitor in the space but lacks bilingual support and local-first privacy.
- **Yorick** (yorick.xyz): Decision journal focused on maintaining confidence after deciding. Minimal feature set.

**Enterprise/Business Decision Tools**
- **1000minds**: Multi-criteria decision-making (MCDM) with pairwise comparisons. Powerful but enterprise-priced and business-focused. Not designed for personal life decisions.
- **Decision Lens**: Portfolio prioritization for organizations. Not consumer-facing.
- **Definitive Choice**: Alternatives analysis for teams. Enterprise tool.
- **airfocus**: Weighted scoring for product teams. Not personal use.

**AI Decision Tools**
- **MyMap.AI Decision Matrix Maker**: AI generates weighted matrices from descriptions. Web-based but generic, not structured for life decisions.
- **DecTrack**: Pairwise comparison to derive weights. Web tool but limited feature set.

**Career-Specific**
- **80,000 Hours Career Decision Tool**: Excellent 9-step career decision process. Free, web-based. But career-only, English-only, not a general decision framework.

**Template/Generic Tools**
- **Notion/Asana/Lucid templates**: Decision matrix templates exist in productivity tools, but they're generic spreadsheets — no decision-specific features like outcome tracking, emotional state capture, or bias detection.

### Market Size & Trends
- Decision fatigue is a growing concern — average adult makes ~35,000 decisions/day
- "Decision science" and behavioral economics are mainstream (Kahneman, Thaler)
- AI-assisted decision-making is an emerging category but mostly enterprise
- Personal decision tools remain fragmented and low-quality

---

## Key Gaps & Opportunities

1. **No web-first bilingual decision tool exists.** Every decision app is either mobile-only (Pros & Cons) or English-only (Decision Log, Yorick). Zero coverage for EN/ZH bilingual users.

2. **No privacy-first/local-first decision tool.** Decision data is deeply personal (career choices, relationship decisions, financial trade-offs). Current tools all require accounts and cloud storage. No tool treats decision data as sensitive-by-default.

3. **No family-centered collaborative decision tool.** Chinese diaspora families make major decisions collectively (relocation, eldercare, education, property). No tool supports multi-person weighted input for family decisions. WeChat group chats are the current "tool."

4. **Decision journaling + outcome tracking is underdeveloped.** Decision Journal App and Yorick exist but are minimal. No tool combines: (a) structured decision frameworks, (b) emotional state capture, (c) scheduled outcome reviews, (d) pattern analysis across decisions over time.

5. **Life-path scenario planning for individuals doesn't exist.** Enterprise scenario planning tools are mature. Consumer tools for "should I relocate to Shanghai vs. stay in SF" with financial modeling, lifestyle trade-offs, and timeline visualization don't exist.

6. **Cross-border decision support is nonexistent.** Diaspora users face unique decisions: dual-country tax implications, cross-border property, education system comparisons, immigration pathways. No tool provides structured frameworks for these.

7. **Regret minimization and pre-mortem frameworks are blog posts, not tools.** Tim Ferriss's fear-setting, Bezos's regret minimization, pre-mortem analysis — these are popular frameworks with zero dedicated tooling. Decision Log touches this but doesn't go deep.

---

## Competitor Weaknesses

| Competitor | Key Weakness |
|-----------|-------------|
| **Pros & Cons - Smart Choices** | Mobile-only, English-only, no outcome tracking, no decision history |
| **Decision Journal App** | iOS-only, no frameworks, no AI, no collaboration, English-only |
| **Decision Log** | Requires account, no local-first option, English-only, no collaboration |
| **Yorick** | Minimal features, no frameworks, no outcome analysis |
| **1000minds** | Enterprise pricing, business-focused, not for personal decisions |
| **80,000 Hours** | Career-only, English-only, not a persistent tool (one-time use) |
| **MyMap.AI** | Generic AI output, no decision history, no outcome tracking |
| **Notion templates** | No decision-specific features, requires Notion subscription |

**Common weaknesses across all competitors:**
- None are bilingual (EN/ZH)
- None are privacy-first/local-first
- None support family/group collaborative decisions
- None connect decision-making to other life domains (finance, career, relationships)
- None offer cross-border decision frameworks for diaspora users

---

## App Concepts

### 1. 权衡 (QuánHéng) — Weighted Life Decision Engine

**One-line pitch:** Privacy-first weighted decision matrix for life's biggest choices — bilingual, web-first, no account required.

**Target user:** Young professionals (25-40) facing major life decisions: career changes, relocations, major purchases, relationship milestones. Especially Chinese diaspora navigating cross-cultural decisions.

**Key differentiator:** Combines weighted criteria scoring with pre-built templates for common life decisions (relocation, career change, home purchase, grad school). Local-first storage means your most personal deliberations never leave your device. Bilingual EN/ZH with culturally-aware templates.

**Core features:**
- Weighted decision matrix with drag-to-rank criteria importance
- Pre-built templates: Relocation, Career Change, Major Purchase, Education, Relationship
- Pairwise comparison mode to discover your true priorities (inspired by 1000minds, simplified)
- Visual radar charts showing how options compare across dimensions
- Local-first IndexedDB storage, optional encrypted cloud backup
- Bilingual EN/ZH interface with culturally-adapted templates

**Monetization:** Free core (unlimited decisions + 5 templates). $5/mo for premium templates, export to PDF, cloud sync, and decision sharing links.

| Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 5 | 5 | 4 | 5 | **19** |

---

### 2. 决策簿 (JuéCèBù) — Decision Journal with Outcome Intelligence

**One-line pitch:** Log every important decision with context, emotions, and confidence — then track what actually happened to sharpen your judgment over time.

**Target user:** Reflective individuals who want to improve their decision-making quality. Professionals, students, and anyone making consequential personal choices.

**Key differentiator:** Goes beyond simple journaling by combining: structured decision capture (context, options considered, reasoning, emotional state, confidence level), scheduled outcome check-ins (30/60/90/365 days), and pattern analysis that reveals your decision-making tendencies (overconfidence bias, emotional decisions, risk aversion patterns). Privacy-first, bilingual.

**Core features:**
- Structured decision entry: situation, options, reasoning, emotional state, confidence (1-10)
- Framework prompts: pre-mortem, regret minimization, second-order effects
- Scheduled outcome reviews with push notifications (PWA)
- Decision pattern dashboard: accuracy by category, confidence calibration, emotional correlation
- "Decision DNA" — your personal decision-making profile built from history
- Local-first with optional encrypted sync

**Monetization:** Free core (unlimited decisions + basic review reminders). $6/mo for AI-powered pattern analysis, "Decision DNA" profile, advanced frameworks, and PDF export.

| Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 4 | 5 | 4 | 5 | **18** |

---

### 3. 家议 (JiāYì) — Family Decision Hub

**One-line pitch:** Collaborative decision-making for families — anonymous voting, weighted preferences, and consensus building for the choices that affect everyone.

**Target user:** Chinese diaspora families making collective decisions: where to spend holidays, eldercare arrangements, property purchases, children's education, relocation. Also multicultural couples navigating cross-cultural life choices.

**Key differentiator:** No tool supports family-centered collaborative decisions. Chinese families (and many Asian families) make major decisions collectively, but currently use scattered WeChat messages. JiāYì provides: anonymous preference voting (so hierarchy doesn't suppress input), weighted criteria that the family defines together, and a "family decision history" that documents how and why choices were made. Bilingual EN/ZH essential.

**Core features:**
- Create a "family board" with invite-link sharing (no accounts needed for participants)
- Anonymous voting on options with optional reasoning
- Weighted criteria that the family defines collaboratively
- "Concerns" feature — each member can flag concerns privately, revealed only in aggregate
- Decision history timeline — what we decided and why, for family memory
- Bilingual EN/ZH with culturally-aware prompts (filial piety, face-saving, harmony)

**Monetization:** Free for 1 family board + 3 decisions/month. $4/mo for unlimited decisions, decision history, advanced voting modes, and family archive.

| Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 4 | 5 | 3 | 5 | **17** |

---

### 4. 路径 (LùJìng) — Life Path Scenario Planner

**One-line pitch:** Visualize "what if" life scenarios side-by-side — model the financial, lifestyle, and emotional trade-offs of your biggest life choices.

**Target user:** Anyone at a major life crossroads: considering relocation, career change, marriage, starting a family, going back to school. Especially useful for diaspora users weighing "stay abroad vs. return home."

**Key differentiator:** Enterprise scenario planning adapted for personal life. Visualize branching life paths with estimated financial impact, lifestyle changes, and timeline projections. No consumer tool does this — people currently use spreadsheets or gut feelings. The "stay vs. go" calculator for diaspora users (comparing cost of living, salary purchasing power, family proximity, career trajectory) is a unique hook.

**Core features:**
- Visual decision tree builder with branching scenarios
- Financial modeling: cost of living comparison, salary adjustment, savings projection
- Lifestyle dimension scoring: family proximity, career growth, social life, health access
- Timeline view: "In 1 year / 3 years / 5 years, this path looks like..."
- "Stay vs. Return" template for diaspora users (US/China comparison built-in)
- Export scenario comparison as shareable PDF

**Monetization:** Free core (2 scenarios with basic dimensions). $7/mo for unlimited scenarios, financial modeling, city cost-of-living data, and advanced timeline projections.

| Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 3 | 5 | 4 | 4 | **16** |

---

### 5. 前鉴 (QiánJiàn) — Pre-Mortem & Regret Minimization Studio

**One-line pitch:** Stress-test your decisions before you commit — structured pre-mortem analysis, fear-setting exercises, and regret minimization frameworks in one focused tool.

**Target user:** Analytical thinkers, founders, professionals, and anyone prone to analysis paralysis who needs structured frameworks to move past indecision. People who read Kahneman, Ferriss, or Bezos on decision-making.

**Key differentiator:** Takes popular decision frameworks (pre-mortem, fear-setting, regret minimization, inversion thinking) and turns them into guided, interactive exercises — not just blog posts. The "future self letter" feature lets you write to your future self explaining why you made this choice, then delivers it on a scheduled date. No tool operationalizes these frameworks.

**Core features:**
- Guided pre-mortem: "Imagine it's 1 year from now and this decision failed. Why?"
- Fear-setting worksheet (Tim Ferriss method): Define, Prevent, Repair for worst-case scenarios
- Regret minimization: "At age 80, which choice will you regret NOT taking?"
- Inversion thinking: "What would make this decision definitely wrong?"
- "Future self letter" — write your reasoning, delivered to you in 3/6/12 months
- Decision courage score — measures analysis paralysis tendency over time

**Monetization:** Free core (all frameworks, 3 active decisions). $5/mo for unlimited decisions, future self letters, courage score analytics, and archive.

| Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 5 | 4 | 3 | 4 | **16** |

---

### 6. 对比 (DuìBǐ) — Side-by-Side Life Comparison Tool

**One-line pitch:** Compare any two life options head-to-head with structured dimensions, community benchmarks, and bilingual city/school/job data.

**Target user:** Practical decision-makers comparing specific options: two job offers, two cities to live in, two schools for their kids, two apartments to rent. People who want data, not feelings.

**Key differentiator:** Purpose-built comparison tool (not a generic spreadsheet) with domain-specific dimensions pre-loaded. Comparing two cities? Get cost of living, commute, safety, schools, Chinese community size, flight distance to family. Comparing two job offers? Get total comp, growth trajectory, work-life balance, visa implications. Community-contributed benchmarks for popular comparisons (SF vs. Shanghai, FAANG vs. startup).

**Core features:**
- Pre-built comparison templates: Cities, Jobs, Schools, Apartments, Cars
- Auto-populated data for common comparisons (cost of living, salary data)
- Custom dimensions with weighted importance
- Community benchmarks: see how others scored similar comparisons
- "Deal-breaker" flags — mark dimensions where one option is unacceptable
- Bilingual EN/ZH with Chinese city/school data

**Monetization:** Free core (unlimited comparisons with manual data). $5/mo for auto-populated data, community benchmarks, and premium templates.

| Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 3 | 4 | 4 | 4 | **15** |

---

## Scoring Summary

| Rank | App | Subdomain | Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|------|-----|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 1 | **权衡 (QuánHéng)** — Weighted life decision engine | quanheng.ljding.app | 5 | 5 | 4 | 5 | **19** |
| 2 | **决策簿 (JuéCèBù)** — Decision journal with outcome intelligence | juece.ljding.app | 4 | 5 | 4 | 5 | **18** |
| 3 | **家议 (JiāYì)** — Family decision hub | jiayi.ljding.app | 4 | 5 | 3 | 5 | **17** |
| 4 | **路径 (LùJìng)** — Life path scenario planner | lujing.ljding.app | 3 | 5 | 4 | 4 | **16** |
| 4 | **前鉴 (QiánJiàn)** — Pre-mortem & regret minimization studio | qianjian.ljding.app | 5 | 4 | 3 | 4 | **16** |
| 6 | **对比 (DuìBǐ)** — Side-by-side life comparison tool | duibi.ljding.app | 3 | 4 | 4 | 4 | **15** |

---

## Recommended Build Order

1. **权衡 (QuánHéng)** — Highest score (19/20), highest feasibility (5/5). Core decision engine that anchors the domain. Web-first weighted matrix with templates is a 3-4 week MVP. Establishes the "decision" subdomain brand.

2. **决策簿 (JuéCèBù)** — Second highest score (18/20). Decision journaling complements QuánHéng (decide → journal → review outcome). 4-5 week MVP. The outcome tracking + pattern analysis is a strong long-term moat.

3. **前鉴 (QiánJiàn)** — High feasibility (5/5), quick build. Framework-driven exercises that complement both QuánHéng (pre-mortem before deciding) and JuéCèBù (fear-setting as journal entry). 2-3 week MVP — mostly guided text exercises.

4. **家议 (JiāYì)** — Strongest cultural differentiator for diaspora. Requires multi-user collaboration (invite links, anonymous voting) which adds complexity. 4-5 week MVP. Best built after ecosystem has identity/auth patterns from other apps.

5. **路径 (LùJìng)** — Highest concept ambition but moderate feasibility. Financial modeling and city comparison data require data sourcing. 5-6 week MVP. Best built after QuánHéng validates demand for structured decision tools.

6. **对比 (DuìBǐ)** — Depends on community data and auto-populated benchmarks for full value. Lowest score but practical utility is high. 5-6 week MVP. Best built last when ecosystem traffic can seed community benchmarks.

---

## Ecosystem Integration

| Decision App | Integrates With | How |
|-------------|----------------|-----|
| **权衡 (QuánHéng)** | Compass (weekly priorities), SkillAdjacent (career decisions) | Decision outcomes inform weekly priority setting; career decisions use skill data |
| **决策簿 (JuéCèBù)** | 心情簿 XinQingBu (mood), Radar (burnout) | Mood at decision time correlates with outcome quality; burnout affects judgment |
| **家议 (JiāYì)** | 共进 GòngJìn (family goals), hangwith.ljding.app | Family decisions feed into shared goals; hangwith provides the social graph |
| **路径 (LùJìng)** | TaxTwin (dual-country finance), RemiFlow (remittance) | Life path scenarios include financial modeling from finance apps |
| **前鉴 (QiánJiàn)** | 决策簿 JuéCèBù (journal), learn.ljding.app | Pre-mortem results feed journal; learn hosts decision science courses |
| **对比 (DuìBǐ)** | Roam (travel comparison), SalaryStreet (job comparison) | City comparisons for travel/relocation; salary data for job offer comparisons |

---

## Sources

- [Pros & Cons - Smart Choices (App Store)](https://apps.apple.com/us/app/pros-cons-smart-choices/id1412523961)
- [Decision Journal App](https://decisionjournalapp.com/)
- [Decision Log - AI-Powered Decision Journal](https://www.thedecisionlog.com/)
- [Yorick Decision Journal](https://www.yorick.xyz/)
- [1000minds Decision-Making Software](https://www.1000minds.com/decision-making)
- [80,000 Hours Career Decision Tool](https://80000hours.org/career-decision/article/)
- [Weighted Decision Matrix (airfocus)](https://airfocus.com/blog/weighted-decision-matrix-prioritization/)
- [DecTrack Decision Matrix](https://dectrack.com/en/methods/decision-matrix)
- [MyMap.AI Decision Matrix Maker](https://www.mymap.ai/tools/decision-matrix-maker)
- [Privacy-First App Design (Emrld Labs)](https://emrldlabs.com/blog/privacy-first-app-design/)
- [Super Productivity - Local-First](https://super-productivity.com/use-cases/privacy-productivity/)
