# Productivity App Concepts — Session 21 (2026-06-09)

> Market research from AI productivity tools sector (2025-2026)
> Existing apps: Drift, Handoff, Review, Compass, Tempo (productivity); Lattice, Graftbook, Inkwell, Shuangyu (PKM)
> Generated via Claude Code from market trend analysis

---

## Concept 1: Cadence — `cadence.ljding.app`

**Framework**: Adaptive Ritual-Stacking Engine

**Value Proposition**: Chains micro-habits into adaptive daily routines, adjusting sequence and timing based on completion patterns and energy self-reports.

**Top 3 Features**:
1. Drag-and-drop ritual chain builder with conditional branches (if skipped X, substitute Y)
2. Energy curve tracker that learns your peak windows and auto-suggests routine reordering
3. Weekly rhythm report with streak analytics and friction-point identification

**Differentiation from Notion/Obsidian**: Those tools treat habits as static checklists. Linear ignores personal routines entirely. Cadence models routines as adaptive chains, not flat lists — it reacts to your actual behavior rather than shaming you for missed checkboxes.

**Tech Stack**: Next.js + Supabase + Edge Functions, PWA-first, local-first with CRDT sync (Yjs), optional CalDAV integration

**MVP Ease**: 3/5

---

## Concept 2: Verdict — `verdict.ljding.app`

**Framework**: Temporal Decision-Journal with Feedback Loops

**Value Proposition**: Captures context, options, and reasoning at decision-time, then prompts revisits to close the feedback loop — so you actually learn from past choices.

**Top 3 Features**:
1. Decision capture form with weighted criteria matrix, confidence level, and emotional state tagging
2. Scheduled revisit prompts (30/90/180 days) that surface original reasoning alongside actual outcomes
3. Decision pattern dashboard showing biases, blind spots, and domains where your calibration is off

**Differentiation**: Notion/Obsidian are themselves sources of context-switching, not solutions for it. Linear tracks work decisions but not personal/strategic ones. Verdict treats decisions as first-class objects with temporal feedback loops.

**Tech Stack**: SvelteKit + SQLite (Turso) + Resend for email nudges, markdown export, optional LLM summarization for pattern detection

**MVP Ease**: 2/5

---

## Concept 3: Switchboard — `switchboard.ljding.app`

**Framework**: Attention-Fragmentation Quantifier

**Value Proposition**: Logs context switches, measures ramp-up friction, generates a weekly attention-fragmentation report to defend deep work time.

**Top 3 Features**:
1. One-click context logger (keyboard shortcut or menubar) that timestamps project switches with optional friction rating
2. Fragmentation score per day/week showing switching cost in estimated lost minutes, with heatmap visualization
3. Block-scheduling suggestions that consolidate scattered similar-context work into contiguous time blocks

**Differentiation**: Notion/Obsidian are themselves sources of context-switching, not solutions for it. Linear tracks task completion but not the cognitive cost of juggling tasks. Switchboard makes the invisible tax of multitasking visible and actionable.

**Tech Stack**: Tauri (Rust + WebView) desktop app for low-overhead capture, React frontend, local SQLite, optional sync via CloudKit/Supabase

**MVP Ease**: 3/5

---

## Scoring (for PRIORITIES.md)

| App | Feasibility | Differentiation | Monetization | Domain Fit | Total |
|-----|:-----------:|:---------------:|:------------:|:----------:|:-----:|
| Verdict | 5 | 4 | 4 | 5 | **18** |
| Cadence | 4 | 4 | 4 | 5 | **17** |
| Switchboard | 4 | 5 | 4 | 4 | **17** |

## Recommended First Build: Verdict

Verdict has the lowest MVP barrier (2/5) — essentially a structured CRUD app with scheduled email nudges. Strong domain fit with the productivity ecosystem, distinct from existing apps, and high retention potential (the revisit loop keeps users coming back).
