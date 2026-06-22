# Digital Privacy & Personal Data Management — New Concepts

**Session 33 | 2026-06-22**

## Concept 1: JianDu (监督) — Privacy Health Dashboard

**Subdomain**: jiandu.ljding.app

### Problem It Solves

Users are overwhelmed by privacy threats but have no unified view. They check passwords manually, wonder if they've been breached, and have no idea what their overall "privacy health" looks like. Existing tools are either too complex (password managers) or too narrow (just breach checking).

### Core Features

1. **Breach Monitor**: Enter email(s) → check against HIBP → show all breaches with severity and affected data
2. **Password Health Score**: Voluntary password entry → check against common password lists + HIBP → identify reused/weak passwords
3. **Tracker Awareness**: Browser extension showing page trackers with bilingual explanations
4. **Privacy Score**: Composite 0-100 score based on breach count, password health, and tracker exposure
5. **Weekly Digest**: Email summary of new breaches, score changes, recommendations

### Value Proposition

> "Know your privacy health in one glance. JianDu watches your digital footprint so you don't have to."

### Differentiation

- **Web-first**: Unlike 1Password/Norton, no app install required
- **Bilingual**: Tracker explanations in EN/ZH — first tool to explain Western trackers to Chinese users
- **Holistic**: Combines breach + password + tracker into one score
- **Voluntary**: Users choose what to share; not a keylogger or full password manager

### Monetization

- Free: Core dashboard + 1 email check + basic score
- Premium ($3/mo): Unlimited email monitoring, weekly digests, history
- Family ($5/mo): Up to 5 members, family breach notifications

### Feasibility

- HIBP API is free for single email, paid for monitoring
- Password health requires users to voluntarily enter passwords (can hash locally)
- Tracker visualization requires browser extension (Chrome/Firefox)
- MVP: 4-6 weeks

### Strategic Fit

- High fit with privacy-first philosophy of ljding.app ecosystem
- Could integrate with learn.ljding.app (privacy education content)
- Complements rather than competes with password managers (gateway drug to privacy awareness)

---

## Concept 2: LianWang (连网) — Cross-Platform Account Inventory

**Subdomain**: lianwang.ljding.app

### Problem It Solves

Diaspora Chinese users have accounts on both Western platforms AND Chinese platforms (WeChat, Taobao, Alipay, Douyin, Bilibili). They have no single place to track these accounts. Family sharing of accounts is common but undocumented. No tool addresses the cross-cultural account management gap.

### Core Features

1. **Account Inventory**: List all accounts (EN + ZH platforms) with category, sensitivity level, last accessed
2. **Cross-Platform Search**: Search "Netflix" and "爱奇艺" (iQIYI) together — bilingual platform recognition
3. **Family Account Tracker**: Document shared accounts (streaming, payments, shopping) with family members
4. **Access Instructions**: Store instructions for next of kin ("How to access my WeChat backup")
5. **Data Residency Map**: Visual map showing where each platform stores your data (CN vs US vs EU)
6. **Export/Deletion Guide**: Step-by-step guide for requesting data export or account deletion from each platform

### Value Proposition

> "One dashboard for all your accounts — East and West. Know what you have, where it lives, and how to manage it."

### Differentiation

- **First cross-cultural account manager**: Handles both EN and ZH platforms in one tool
- **Diaspora-specific**: Addresses shared family accounts, CN data residency concerns
- **Privacy education**: Helps users understand data residency implications

### Monetization

- Free: Up to 10 accounts, basic categories
- Premium ($4/mo): Unlimited accounts, family sharing, export features
- Data Residency Report ($1 one-time): PDF report for immigration/legal purposes

### Feasibility

- Manual account entry (no scraping) — low technical complexity
- Data residency info is research-based (public information)
- Export/deletion guides require ongoing maintenance but are text-based
- MVP: 3-4 weeks

### Strategic Fit

- Unique white space — no competitor addresses diaspora Chinese cross-platform account management
- Could integrate with elder care apps (managing parent's accounts)
- Privacy-respecting (all data stored locally or encrypted)

---

## Concept 3: QuanWang (全网) — Data Broker Scanner

**Subdomain**: quanwang.ljding.app

### Problem It Solves

Data brokers collect and sell personal information. Users don't know who has their data. Removal is tedious and brokers re-collect data. Existing tools like Incogni focus on US brokers, but Chinese data brokers are also prevalent in diaspora communities.

### Core Features

1. **Broker Scan**: Enter name/email/phone/address → search known data broker databases
2. **Exposure Score**: Rate how exposed you are (0 = no results, 100 = everywhere)
3. **Broker Database**: Bilingual directory of both Western and Chinese data brokers with:
   - What data they collect
   - How to request removal
   - Whether they accept removal requests
4. **Automated Removal**: For supported brokers, pre-fill removal request (requires user auth)
5. **Re-check**: Periodically re-scan to see if data re-appeared
6. **Family Members**: Can add family members (elder parents) who may be more exposed

### Value Proposition

> "See who's selling your data. QuanWang exposes the data brokers and helps you disappear."

### Differentiation

- **First bilingual broker database**: EN/ZH broker list with removal guides for each
- **Chinese broker coverage**: Addresses Tencent/Alibaba/ByteDance affiliate brokers unknown to diaspora
- **Family protection**: Extend protection to elderly family members who are high-value targets

### Monetization

- Free: Basic scan (3 brokers), exposure score
- Premium ($5/mo): Full scan (100+ brokers), automated removal, monthly re-check
- Family ($8/mo): Protect up to 5 family members

### Feasibility

- Requires building/maintaining broker database (ongoing research)
- Automated removal requires compliance with each broker's specific process
- Legal complexity in different jurisdictions
- MVP: 6-8 weeks (broker database is the bottleneck)

### Strategic Fit

- High privacy positioning — fits ecosystem values
- Could integrate with identity documentation apps (proof of identity for removals)
- Strong differentiator vs Western-only privacy tools

---

## Concept 4: YiChan (遗产) — Digital Legacy Planner

**Subdomain**: yichan.ljding.app

### Problem It Solves

No one plans for digital death. When someone passes, family members struggle to access or close accounts. Existing solutions are either legal-only (expensive lawyers) or too complex (enterprise tools). Chinese platforms have specific inheritance requirements that diaspora families don't know about.

### Core Features

1. **Account Inventory**: List all digital accounts (same as LianWang but focused on legacy)
2. **Legacy Instructions**: Per-account instructions: "How to access", "How to close", "What happens if unclosed"
3. **CN Platform Guide**: Specific guides for WeChat, Alipay, Taobao, Douyin inheritance processes
4. **Trusted Contact**: designate who receives instructions (single person, not embedded in app)
5. **Document Vault**: Store important documents (will, ID copies) with encrypted access for trusted contact
6. **Auto-Expiration**: If not accessed for X months, send instructions to trusted contact

### Value Proposition

> "Your digital life, organized for those you leave behind. YiChan ensures your accounts are handled with care."

### Differentiation

- **Bilingual CN platform guides**: No other digital estate tool covers WeChat/Alipay inheritance
- **Privacy-first**: Instructions stored encrypted, only accessible by trusted contact
- **No lawyer required**: Makes digital estate accessible to everyone

### Monetization

- Free: Basic inventory (up to 20 accounts), generic instructions
- Premium ($4/mo): Unlimited accounts, CN platform guides, document vault (1GB)
- Family Legacy ($6/mo): Multi-person inventory, family trusted contact network

### Feasibility

- Data storage and encryption required
- CN platform inheritance info requires ongoing research (platforms change policies)
- Legal disclaimer needed (not legal advice)
- MVP: 4-6 weeks

### Strategic Fit

- Natural extension of LianWang (account inventory)
- Complements elder care apps (managing parent's digital legacy)
- High emotional value — users who sign up become advocates

---

## Prioritization Recommendation

### Immediate (Build First)

1. **JianDu** — Quickest to build, clearest value proposition, strongest differentiation (bilingual breach + password dashboard)

### Second (Expand Ecosystem)

2. **LianWang** — Addresses unique diaspora gap, shares infrastructure with JianDu

### Later (High Complexity)

3. **QuanWang** — Requires broker database maintenance, legal complexity
4. **YiChan** — High emotional value but requires careful legal handling

---

*Concepts compiled: 2026-06-22*
*See also: digital-privacy-research-2026.md for market analysis*
