# Digital Privacy & Personal Data Management — Research

**Session 33 | 2026-06-22**

## Executive Summary

- **Privacy fatigue is real**: Users are overwhelmed by consent dialogs, data requests, and tracking — they want simple, proactive tools
- **Diaspora Chinese users face unique gaps**: Language barriers prevent them from understanding privacy policies (EN/ZH), managing accounts across CN/global platforms, and understanding data residency
- **Web-first privacy tools are rare**: Most privacy apps are mobile-first; browser-based tools for privacy management are underserved
- **Personal data ownership is emerging**: Users increasingly want to know WHO has their data, WHERE it's stored, and HOW to export/delete it
- **Opportunity**: Build a "privacy command center" for web users — combining password health, data broker removal, account monitoring, and consent management in one dashboard

## Market Landscape

### Existing Competitors

| App | Type | Strengths | Weaknesses |
|-----|------|-----------|------------|
| **1Password** | Password manager | Polished, strong security | Mobile-first, no free tier, no data breach monitoring |
| **Bitwarden** | Password manager | Open source, affordable | Complex UI, limited breach monitoring |
| **Proton** (Pass, VPN, Mail) | Privacy suite | Privacy-respecting, encrypted | Ecosystem lock-in, CN users face access issues |
| **DuckDuckGo** | Browser/Privacy | Simple, privacy search | Browser-only, no account monitoring |
| **LastPass** | Password manager | Feature-rich | Multiple breaches, complex pricing |
| **Norton** (LifeLock) | Identity theft | Strong brand, monitoring | Expensive, mobile-first, US-centric |
| **Have I Been Pwned** | Breach checking | Free, useful | No ongoing monitoring, single-check model |
| **Incogni** | Data broker removal | Automated removal | Privacy-focused only, no account mgmt |
| **DeleteMe** | Data broker removal | Human-assisted | Expensive, US-only |

### Market Trends (2025-2026)

1. **AI-powered privacy assistants**: ChatGPT-style tools that explain privacy policies in plain language
2. **Data broker proliferation**: More brokers collecting and selling personal data; users want removal
3. **Cross-border data anxiety**: GDPR, CCPA, PIPL (China) — users confused about which laws protect them
4. **Password health scoring**: Beyond "is this password breached" to "is this password reused/acquired"
5. **Digital estate planning**: Managing what happens to accounts/data after death or incapacity
6. **Consent fatigue**: Users want automatic consent management, not endless popups
7. **Privacy score products**: Dashboards showing overall "privacy health" across multiple vectors

## Gap Analysis

### Gap 1: Cross-Border Privacy Management (High Priority)

**Problem**: Diaspora Chinese users have accounts on both Chinese platforms (WeChat, Alipay, Taobao, Douyin) and global platforms (Google, Meta, Apple). Each has different privacy laws, data residency, and deletion processes. No tool bridges this gap.

**Specific Pain Points**:
- Can't read Chinese privacy policies → don't know what data CN apps collect
- No way to request data export/deletion from CN apps (PIPL allows this but process is CN-language-only)
- Confused about which privacy law applies when (GDPR for EU, PIPL for CN, CCPA for CA)
- Accounts on CN platforms may be accessed by family members (shared accounts common in diaspora)

**Opportunity**: Privacy dashboard that shows "your data footprint" across EN and ZH platforms, with guides for exercising rights under different laws.

**Opportunity Score**: Demand 4/5, Feasibility 3/5, Differentiation 5/5, Domain Fit 5/5

---

### Gap 2: Password + Breach Health Dashboard (Medium Priority)

**Problem**: Users have 50-200 accounts but no unified view of password health. Existing password managers don't show "passwords found in breaches" in a dashboard. Users want a free, web-based view of their overall security posture without committing to a full password manager.

**Specific Pain Points**:
- "I don't know if any of my passwords were compromised"
- Password managers are "too much commitment" for casual users
- Want breach alerts without paying for full identity protection
- Have no way to track which accounts still use old breached passwords

**Opportunity**: Free web-based dashboard that checks email against HIBP, shows password reuse patterns (via voluntary entry), and tracks "security score" over time.

**Opportunity Score**: Demand 4/5, Feasibility 5/5, Differentiation 3/5, Domain Fit 4/5

---

### Gap 3: Data Broker Presence Scanner (Medium Priority)

**Problem**: Data brokers collect and sell personal info (name, email, phone, address, purchase history). Users don't know who has their data. Removal processes are tedious and recur — brokers re-collect data.

**Specific Pain Points**:
- "Who has my personal information?"
- Want to remove data from brokers but process is time-consuming
- Some brokers specialize in specific ethnic groups (Chinese diaspora targeted)
- Chinese-language brokers (Tencent, Alibaba affiliate data brokers) are unknown to diaspora

**Opportunity**: Tool that scans known data brokers, shows "exposure level", and streamlines removal requests. Bilingual EN/ZH broker database would be unique.

**Opportunity Score**: Demand 4/5, Feasibility 3/5, Differentiation 4/5, Domain Fit 4/5

---

### Gap 4: Consent Management & Tracker Visualization (Lower Priority)

**Problem**: Websites track users via hundreds of trackers. Users have no visibility into what follows them, and consent dialogs are overwhelming.

**Specific Pain Points**:
- "What trackers are on this page?"
- Want to block tracking without technical knowledge
- Existing tools (uBlock, Privacy Badger) are too technical
- Consent popups are annoying but legally required — users want auto-decline

**Opportunity**: Browser extension that visualizes page trackers, auto-declines non-essential cookies, and shows "tracker load" score per site. Bilingual EN/ZH explanations of what each tracker does.

**Opportunity Score**: Demand 3/5, Feasibility 4/5, Differentiation 3/5, Domain Fit 3/5

---

### Gap 5: Digital Legacy Planner (Lower Priority)

**Problem**: No one talks about what happens to digital accounts after death or incapacity. Existing solutions are either legal-only (lawyers) or too complex (enterprise tools).

**Specific Pain Points**:
- Family members don't know all digital accounts of deceased relative
- Want to leave "digital inheritance" instructions to family
- Don't want accounts to become dormant or be accessed by strangers
- CN platforms (WeChat, Alipay) have specific inheritance requirements

**Opportunity**: Web-based digital estate planner with account inventory, instructions for next of kin, and guides for CN-platform inheritance. Privacy-respecting (data stored locally or with clear encryption).

**Opportunity Score**: Demand 3/5, Feasibility 3/5, Differentiation 5/5, Domain Fit 4/5

## User Need Deep Dive: Diaspora Chinese Context

### Unique Needs Not Addressed by Current Tools

1. **Bilingual privacy policy reading**: Ability to understand what Chinese apps (WeChat, Taobao, Douyin) actually collect — most diaspora can't read CN privacy policies

2. **Cross-platform account inventory**: One place to track accounts on both EN and ZH platforms (not split into "Western" and "Chinese" tools)

3. **Data residency awareness**: Understanding that data for CN platforms is stored in CN servers under CN law jurisdiction

4. **Family account sharing norms**: CN families commonly share accounts (streaming, shopping, payments) — Western privacy tools assume individual accounts

5. **Export/deletion rights under PIPL**: China's Personal Information Protection Law grants rights to request data export and deletion — but the process is entirely in Chinese

## Recommended Subdomain Concepts

### Tier 1: Build First

| Concept | Subdomain | Description |
|---------|-----------|-------------|
| **JianDu (监督)** | jiandu.ljding.app | "Watch over me" — Privacy health dashboard with breach monitoring, password scoring, and tracker awareness. Bilingual EN/ZH. |
| **LianWang (连网)** | lianwang.ljding.app | "Connect net" — Cross-platform account inventory for tracking accounts on both EN and ZH services. One dashboard, full picture. |

### Tier 2: Build Next

| Concept | Subdomain | Description |
|---------|-----------|-------------|
| **XiaoXi (消息)** | xiaoxi.ljding.app | "Message/news" — Privacy notification center that aggregates breach alerts, data broker exposure, and account changes across connected services. |
| **QuanWang (全网)** | quanwang.ljding.app | "Whole net" — Data broker presence scanner showing who has your data, with streamlined removal workflows. |

### Tier 3: Explore Later

| Concept | Subdomain | Description |
|---------|-----------|-------------|
| **YiChan (遗产)** | yichan.ljding.app | "Legacy/inheritance" — Digital estate planner with account inventory and next-of-kin instructions. |
| **TongYi (同意)** | tongyi.ljding.app | "Consent" — Consent management helper that auto-declines non-essential cookies and explains trackers in bilingual terms. |

## Competitive Analysis: Web-First Privacy Tools

| Tool | Web-Based? | Free Tier | EN/ZH Bilingual | Diaspora-Focused |
|------|-----------|-----------|-----------------|------------------|
| 1Password | Partially | No | No | No |
| Bitwarden | Yes | Yes | No | No |
| Proton | Yes | Limited | No | No |
| HIBP | Yes | Yes | No | No |
| Incogni | Yes | No | No | No |
| DeleteMe | No | No | No | No |
| **JianDu (proposed)** | **Yes** | **Yes** | **Yes** | **Yes** |

## Opportunity Scoring

| Domain | Opportunity Score | Rationale |
|--------|------------------|-----------|
| Digital Privacy | 78/100 | High demand, strong differentiation for bilingual web-first tool, fits privacy-first ecosystem philosophy |

**Breakdown**: Market Demand 30/30, Feasibility 20/25, Differentiation 20/25, Strategic Fit 8/20

## Next Steps

1. Validate "JianDu" concept with potential users (diaspora Chinese who care about privacy)
2. Research HIBP API integration for breach checking
3. Investigate data broker databases (both Western and Chinese)
4. Draft MVP scope for account inventory feature
5. Consider pilot with privacy-conscious learn.ljding.app users

## Related Files

- Previous research in this series: All domain research files in this directory
- Existing apps: learn.ljding.app, hangwith.ljding.app

---

*Research compiled: 2026-06-22*
