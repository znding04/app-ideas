# Identity/Documentation Domain — App Concepts (2026-06-05)

## Domain: Identity / Documentation

**Research covered:** 5 market gaps, 5 app concepts
**Session:** 19th domain explored (Identity/Documentation)

---

## Market Gaps

| Gap | Problem | Evidence |
|-----|---------|----------|
| **Unified US-China Dashboard** | No tool tracks both US and Chinese document lifecycles together | Families juggle State Dept, USCIS, and 中国领事 separately |
| **Bilingual EN/ZH Organizer** | Cross-border families have zero tools with bilingual document status | 中国领事 is ZH-only; US tools are EN-only |
| **Privacy-First Tracker Post-GetReminded** | GetReminded shutting down leaves consumer vacuum | Privacy-anxious diaspora has no metadata-only option |
| **Guided Renewal Workflows** | No tool guides through both US and CN renewal flows | 中国领事 app UX is notoriously poor |
| **Family Document Coordination** | Multi-gen families need family-as-unit view with role-based visibility | No tool handles citizen + PR + visa holder in one view |

---

## App Concepts

### 1. Docs — docs.ljding.app

|| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 5/5 | Metadata-only tracker, no backend, localStorage/IndexedDB, PWA patterns proven |
| Differentiation | 4/5 | Family grouping + bilingual EN/ZH + no-upload privacy — no competitor combines all |
| Monetization | 3/5 | $4/mo for family sync + advanced alerts. Free tier covers core. Lower ceiling. |
| Domain Fit | 5/5 | Anchors identity domain, complements LegalPath (legal docs) and Passport/visa tracking |
| **Total** | **17** | |

**One-line pitch:** A bilingual EN/ZH dashboard that tracks expiration dates, renewal windows, and status for every identity document your cross-border family holds — without ever uploading a scan.

**Why NOW:** GetReminded shutdown leaves consumer vacuum. 中国领事 app frustrations are documented. Privacy anxiety in Chinese-American community is at peak. Post-COVID passport backlogs normalizing.

**MVP scope:** Document CRUD + expiration countdown + renewal window alerts + family member grouping + bilingual toggle. Zero-upload (metadata only). 2-3 week MVP.

---

### 2. Renew — renew.ljding.app

|| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 4/5 | Content-driven guides, no novel tech. Jurisdiction finder requires data maintenance. |
| Differentiation | 5/5 | No bilingual EN/ZH guide exists for 中国领事 app workflow. English speakers have zero resources. |
| Monetization | 3/5 | $5/mo for advanced checklists + timeline alerts. Free covers core guides. Moderate ceiling. |
| Domain Fit | 5/5 | Strongest LegalPath integration (life event docs). Complements docs.ljding.app naturally. |
| **Total** | **17** | |

**One-line pitch:** Step-by-step bilingual guides for renewing US passports, Chinese passports, green cards, EADs, and travel documents — with jurisdiction-aware instructions.

**Why NOW:** US online passport renewal launched recently but is confusing. 中国领事 app UX is notoriously poor. No English-language guide for 中国领事 workflow exists.

**MVP scope:** Interactive renewal checklists + consulate jurisdiction finder by state + photo requirements comparison + mailing address lookup + timeline estimator. 3-4 weeks.

---

### 3. Vault — vault.ljding.app

|| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 3/5 | Client-side encryption + family sharing adds complexity. WebCrypto well-documented but requires care. |
| Differentiation | 4/5 | Encrypted local-first + family sharing + bilingual labels is unique. No consumer tool does this. |
| Monetization | 4/5 | $6/mo for family sharing + export bundle. Free tier for solo vault. Good upgrade path. |
| Domain Fit | 4/5 | Complements docs.ljding.app (metadata tracker → optional secure storage layer). |
| **Total** | **15** | |

**One-line pitch:** An encrypted, local-first document vault for immigration and identity paperwork — organize, tag, and share securely within your family, with bilingual labels.

**Why NOW:** Growing distrust of cloud storage for sensitive identity docs. No tool combines local-first encryption + family sharing. WebCrypto API makes browser-based encryption viable.

**MVP scope:** Client-side encryption + offline PWA + family sharing via encrypted links + bilingual document categories + PDF export bundle. 4-5 weeks.

---

### 4. Status — status.ljding.app

|| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 2/5 | Scraping government sites is fragile, may violate ToS, changes frequently. |
| Differentiation | 4/5 | Unified multi-agency view is unique. Crowdsourced ImmiHelp is unreliable — authoritative source would differentiate. |
| Monetization | 3/5 | $4/mo for push notifications + family grouping. Free tier covers basic status checks. |
| Domain Fit | 4/5 | Fits identity domain. Could complement LegalPath (case tracking). Complex dependency. |
| **Total** | **13** | |

**One-line pitch:** One page to check the status of every pending application — USCIS case, US passport, Chinese consular app, visa bulletin — with bilingual notifications.

**Why NOW:** People check 4+ government websites manually. ImmiHelp is crowdsourced and unreliable. Visa bulletin changes affect green card timing decisions.

**MVP scope:** USCIS case status polling + US passport status check + visa bulletin monitoring + family case grouping. Note: feasibility 2/5 due to scraping fragility.

---

### 5. Checklist — checklist.ljding.app

|| Dimension | Score | Rationale |
|-----------|:-----:|------------|
| Feasibility | 5/5 | Content-driven with simple CRUD. AI personalization is optional v2 feature. |
| Differentiation | 3/5 | Life event checklists exist in generic form. Bilingual + diaspora-specific scenarios is the differentiator. |
| Monetization | 2/5 | Content feels like it should be free. Premium could be AI personalization + printable bundles. |
| Domain Fit | 5/5 | Strongest learn.ljding.app integration (life skills content). Anchors identity domain entry. |
| **Total** | **15** | |

**One-line pitch:** Interactive bilingual checklists for document-heavy life events — moving to the US, sponsoring a parent, getting married cross-border, having a baby with dual nationality.

**Why NOW:** Cross-border life events trigger document cascades across two countries. Information scattered across Reddit/WeChat/小红书. Low complexity, high content value, fast launch.

**MVP scope:** Scenario-based templates + bilingual step-by-step instructions + progress tracking + printable checklists. 2-3 weeks.

---

## Feature Comparison

|| Feature | GetReminded | Expiration Reminder | Boundless | Docs | Renew | Vault | Checklist |
||---------|:-----------:|:-------------------:|:---------:|:----:|:-----:|:-----:|:---------:|
|| Document Expiration Tracking | Yes | Yes | No | Yes | No | No | No |
|| Bilingual EN/ZH | No | No | No | **Yes** | **Yes** | **Yes** | **Yes** |
|| Web-First | Yes | Yes | Yes | **Yes** | **Yes** | **Yes** | **Yes** |
|| Family Grouping | No | No | No | **Yes** | No | **Yes** | No |
|| No-Upload Privacy | Yes | Yes | No | **Yes** | N/A | **Yes** | N/A |
|| Guided Renewal Workflow | No | No | No | No | **Yes** | No | **Yes** |
|| Life Event Checklists | No | No | No | No | No | No | **Yes** |
|| Encrypted Storage | No | No | No | No | No | **Yes** | No |

---

## Recommended Build Order

1. **Docs** — Simplest scope (2-3 weeks), highest feasibility, creates the identity domain anchor, natural upsell path to Renew and Vault
2. **Renew** — Complements Docs with guided workflows, bilingual EN/ZH guides for 中国领事 app are genuinely novel, 3-4 weeks
3. **Checklist** — Lowest complexity (2-3 weeks), fastest time-to-market, strong learn.ljding.app integration
4. **Vault** — Privacy-first encrypted storage, builds on Docs family grouping, 4-5 weeks
5. **Status** — Most complex (government scraping fragility), defer until API partnerships or official data access available

---

## Next Domain to Explore

Suggested domains for future sessions:
- **Home/Real Estate** — cross-border property management, housemates finder, rent-split for diaspora
- **Pet** — pet tracking for families that shuttle between US and China, pet-friendly travel
- **Gaming/Entertainment** — casual gaming with Chinese-American cultural content, streaming watch parties
- **Home Services** — handyman matching for diaspora homeowners, culturally-aware service referrals