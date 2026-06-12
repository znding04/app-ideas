# Relationships / Network Maintenance — New App Concepts (Session 23)

**Date:** 2026-06-12
**Domain:** Relationships & Network Maintenance
**Researched by:** Claude Code + Hermes cron job

## Overview

Personal CRM / relationship maintenance is a genuinely underserved space, especially for web-first, privacy-respecting, simple-to-use tools. The research identified 5 strong concepts with a combined MVP scope of 3-6 weeks each.

---

## Top Concept: nurture.ljding.app

**Subdomain:** nurture.ljding.app
**Core Value:** The simplest way to remember and maintain all your relationships — personal and professional — without CRM complexity.

### Features
- Add contacts manually or import from phone/Google contacts
- Set per-contact cadence (weekly, monthly, quarterly) with smart reminders
- Quick-log touchpoints: "had coffee," "sent birthday text," "video call" with optional notes
- Relationship circles view (inner circle, close friends, extended network, professional)
- Weekly digest: "You haven't talked to these 5 people in a while"

### Differentiation
Unlike Clay/Dex (professional-focused, auto-enrichment heavy), this is intentionally simple and covers ALL relationship types. Unlike Monica (requires self-hosting or dated UI), this is a modern web PWA. No sales pipeline metaphors — just human connection tracking.

### MVP: 3-4 weeks
### Revenue: Freemium — free for up to 50 contacts, $5/mo for unlimited + advanced reminders + export

### Ecosystem Integration
- **hangwith.ljding.app**: Auto-log hangouts as touchpoints; suggest people to invite based on who you haven't seen
- **learn.ljding.app**: Track study buddies, mentors, learning partners as a relationship circle

### Feasibility Score: 5/5 | Differentiation: 4/5 | Monetization: 4/5 | Domain Fit: 5/5 | **Total: 18/20**

---

## Second: keepclose.ljding.app

**Subdomain:** keepclose.ljding.app
**Core Value:** Never forget what matters about the people you care about — an AI-powered memory layer for your relationships.

### Features
- Per-contact "memory journal": birthdays, preferences, life events, conversation highlights
- AI-suggested conversation starters based on stored context ("Ask about their new job in Portland")
- Smart date tracking: anniversaries, kids' birthdays, important milestones
- Voice-note-to-text: quickly capture post-conversation notes
- Privacy-first: all data stored locally in browser (IndexedDB) with optional encrypted cloud backup

### Differentiation
Clay auto-enriches from public data (job changes, news). This stores **private, personal context** — the stuff that makes relationships feel genuine. "How's your mom's recovery going?" not "I see you changed jobs." Local-first architecture means no data harvesting.

### MVP: 4-5 weeks
### Revenue: Free core (local storage), $6/mo for cloud backup + AI features

### Ecosystem Integration
- **hangwith.ljding.app**: Pre-hangout briefing ("Last time you saw Alex, you talked about...")
- **learn.ljding.app**: Track what topics each contact is interested in; suggest relevant learning content to share

### Feasibility Score: 4/5 | Differentiation: 5/5 | Monetization: 4/5 | Domain Fit: 4/5 | **Total: 17/20**

---

## Third: circles.ljding.app

**Subdomain:** circles.ljding.app
**Core Value:** Visualize the health of your entire social network and get actionable nudges to strengthen the connections that matter most.

### Features
- Concentric circle visualization (Dunbar's number layers: 5 / 15 / 50 / 150)
- Relationship health score per contact based on frequency, reciprocity, and depth of interaction
- "Drifting apart" alerts when a close relationship is losing momentum
- Monthly relationship health report with trends
- Goal setting: "I want to deepen 3 friendships this quarter"

### Differentiation
No existing app focuses on **relationship health analytics** for personal networks. Clay tracks professional networking ROI; this tracks emotional/social well-being. Grounded in Dunbar's number research and social psychology.

### MVP: 4-5 weeks
### Revenue: Freemium — free dashboard for up to 30 contacts, $7/mo for full network + reports + goals

### Ecosystem Integration
- **hangwith.ljding.app**: Feed real hangout data into health scores (in-person meetings weighted higher)
- **learn.ljding.app**: Identify relationships built around shared learning; suggest co-learning opportunities

### Feasibility Score: 4/5 | Differentiation: 5/5 | Monetization: 4/5 | Domain Fit: 4/5 | **Total: 17/20**

---

## Fourth: together.ljding.app

**Subdomain:** together.ljding.app
**Core Value:** A shared space for couples or close friend groups to maintain their broader social network together.

### Features
- Shared contact book between 2-4 people (couples, roommates, friend groups)
- Coordinated touchpoint tracking ("We need to call your parents this week")
- Shared event memory: "Remember that dinner party at Mike's in March?"
- Gift tracker: what you gave/received, ideas for next time
- Joint social calendar with relationship-aware suggestions

### Differentiation
Cupla and Paired focus on the couple's internal relationship. This focuses on **how couples/groups manage their external relationships together**. No existing app addresses the "we should really have the Johnsons over" use case.

### MVP: 5-6 weeks
### Revenue: Free for 1 shared space (up to 25 contacts), $8/mo per space for unlimited contacts + gift tracking + calendar

### Ecosystem Integration
- **hangwith.ljding.app**: Deep integration — plan hangouts from shared contact list, auto-log as touchpoints
- **learn.ljding.app**: Couple/group learning goals tied to social context

### Feasibility Score: 3/5 | Differentiation: 5/5 | Monetization: 4/5 | Domain Fit: 4/5 | **Total: 16/20**

---

## Fifth: weave.ljding.app

**Subdomain:** weave.ljding.app
**Core Value:** Help the people in your network meet each other — be the connector who strengthens everyone's relationships.

### Features
- Tag contacts with interests, skills, industries, and current needs
- AI-powered match suggestions: "Alex is looking for a React developer — you know 3"
- Introduction templates: one-click warm intro emails
- Connector karma score: track how many valuable introductions you've facilitated
- Network map visualization showing clusters and bridge opportunities

### Differentiation
Every personal CRM is inward-focused (manage YOUR relationships). This is **outward-focused** — help your contacts connect with each other. Taps into the "super-connector" archetype. No existing tool does this for individuals (only enterprise tools like LinkedIn Sales Navigator).

### MVP: 5-6 weeks
### Revenue: Free for up to 50 contacts + 5 intros/month, $9/mo for unlimited + AI matching + analytics

### Ecosystem Integration
- **hangwith.ljding.app**: Suggest group hangouts that bring complementary people together
- **learn.ljding.app**: Connect people learning similar topics; facilitate study groups or mentorship matches

### Feasibility Score: 3/5 | Differentiation: 5/5 | Monetization: 4/5 | Domain Fit: 4/5 | **Total: 16/20**

---

## Priority Ranking (Session 23)

| Rank | App | Subdomain | Feasibility | Differentiation | Monetization | Domain Fit | **Total** |
|------|-----|-----------|:-----------:|:---------------:|:------------:|:----------:|:---------:|
| 23 | **nurture** | nurture.ljding.app | 5 | 4 | 4 | 5 | **18** |
| 24 | **keepclose** | keepclose.ljding.app | 4 | 5 | 4 | 4 | **17** |
| 25 | **circles** | circles.ljding.app | 4 | 5 | 4 | 4 | **17** |
| 26 | **together** | together.ljding.app | 3 | 5 | 4 | 4 | **16** |
| 27 | **weave** | weave.ljding.app | 3 | 5 | 4 | 4 | **16** |
