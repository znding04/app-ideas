# Knowledge Management App Ideas — ljding.app

**Generated:** May 2026  
**Research base:** `knowledge-research.md`

---

## Concept Overview

| # | Name | Subdomain | Value Proposition | MVP (1-5) | Complements Ecosystem | Unique Differentiator |
|---|------|-----------|-------------------|-----------|----------------------|----------------------|
| 1 | **Shuangyu** (双语) | `notes.ljding.app` | Bilingual PKM where CN/EN notes live together — cross-language search, mixed-language blocks, toggle-able UI | 4 | Learn.ljding exports study notes here; hangwith shares reading recs as linked notes | Native mixed-language blocks — write one paragraph in EN, next in CN, search finds both |
| 2 | **Inkwell** | `read.ljding.app` | Save articles, highlight passages, watch connections emerge via auto-linked knowledge graph | 3 | Captures what you read while learn.ljding tracks what you study; hangwith surfaces "share-worthy" highlights | Highlights become first-class nodes with backlinks — not just annotations trapped inside an article |
| 3 | **Lattice** | `brain.ljding.app` | Zero-config second brain: open it, start writing, PARA + daily notes + weekly review already wired up | 2 | Acts as "home base" that learn.ljding and hangwith feed into; weekly review surfaces stale knowledge | Ships with PARA + Zettelkasten hybrid — no plugins, no templates, opinionated defaults that just work |
| 4 | **Graftbook** | `graft.ljding.app` | Capture fleeting thoughts in <2 seconds, auto-cluster into evergreen notes overnight | 3 | Quick-capture during learn.ljding study sessions; social context from hangwith | Time-decay + embedding clustering: captures auto-promote to permanent notes or fade — mimics how memory works |

---

## Prioritization (2026-05-16)

### Tier 1: Build First

| Rank | App | Subdomain | MVP Ease | Rationale |
|------|-----|-----------|----------|-----------|
| 1 | **Lattice** | `brain.ljding.app` | 2/5 | Lowest complexity MVP, proves the subdomain, "gateway drug" to ecosystem |
| 2 | **Graftbook** | `graft.ljding.app` | 3/5 | Most unique angle — time-decay + auto-clustering no existing tool does well |

### Tier 2: Build Next

| Rank | App | Subdomain | MVP Ease | Rationale |
|------|-----|-----------|----------|-----------|
| 3 | **Inkwell** | `read.ljding.app` | 3/5 | Read-it-later is high-demand, good synergy with learn.ljding reading lists |
| 4 | **Shuangyu** | `notes.ljding.app` | 4/5 | Hardest technical problem (bilingual search, CJK handling), save for after core editor is proven |

---

## Rationale

**Lattice (brain.ljding.app)** — Ship in 2-3 weeks as a Next.js + Tiptap app with pre-built PARA folders, daily notes, and a weekly review dashboard. It's the lowest-friction "proof of domain" that demonstrates ljding.app ecosystem handles knowledge management, not just learning (learn) and social (hangwith).

**Graftbook (graft.ljding.app)** — Every PKM tool assumes you'll organize later. Nobody does. Graftbook flips it: captures auto-cluster via embedding similarity overnight. Notes surviving 7 days get promoted; rest fade. This is the genuinely novel angle — time-decay + clustering mimics actual memory.

**Inkwell (read.ljding.app)** — Read-it-later with highlights that become first-class backlink nodes. Higher utility than another generic notes app. Synergy: learn.ljding study materials → captures to Inkwell → highlights link to notes in Lattice.

**Shuangyu (notes.ljding.app)** — The "dream" concept but hardest to build well. Bilingual search, mixed-language blocks, proper CJK typography — these are deep technical problems. Save for after the core editor is battle-tested.

---

## Tech Stack Recommendations

- **Editor:** Tiptap (ProseMirror-based, great DX)
- **Database:** SQLite (via Drizzle) for simplicity, or Postgres for scale
- **Auth:** Better Auth or NextAuth (self-hostable)
- **Hosting:** Single Docker container (Railway/Render/Fly.io compatible)
- **Graph visualization:** 3d-force-graph or vis-network
- **i18n:** next-i18next for bilingual UI

---

## Ecosystem Fit

```
learn.ljding.app (structured learning)
        ↓ captures outputs
Lattice (brain.ljding.app) — PARA-organized permanent notes
        ↑ quick captures
Graftbook (graft.ljding.app) — fleeting → evergreen pipeline

hangwith.ljding.app (social)
        ↓ shares reading recs
Inkwell (read.ljding.app) — article highlights with social context
        ↑ links to
Lattice — highlights connected to permanent notes
```
