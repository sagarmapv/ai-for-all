# AI-For-All — Strategy (Claude as backbone)

**One-liner:** Help people understand complex systems (code, specs, products, skills) using AI — ship one real thing, reuse its engine for the next.

## Reality map

| Product | Type | Status |
|---|---|---|
| Python Learning ([Practice-Python-Project](../Practice-Python-Project)) | Existing asset | Working quiz app; adaptive daily-practice loop not built |
| 5G Analyzer ([5g-visualizer](../5g-visualizer)) | Existing asset | Mature spec explorer; AI log-correlation layer not built (blocked on sample log) |
| **AI-Advisor** | New flagship / concept | Not started — see scope below |
| Dataset Builder | Concept | Absorbed into AI-Advisor's core engine (see below) — not a separate product anymore |
| Voice Plugin | Moonshot | Parked until AI-Advisor + 5G AI layer have real usage |

## The key insight driving this strategy

AI-Advisor's job — ingest Requirements/Design/Tests docs, detect gaps (missing Design, missing Tests), stitch R-D-T together, answer questions about the product — **requires** the exact ingest→chunk→embed→retrieve pipeline that "Dataset Builder" was meant to be.

So: **AI-Advisor v1 = Knowledge Core (ingestion/retrieval engine) + R/D/T-specific logic on top.**

Once the Knowledge Core exists as a reusable module, it becomes the engine for:
- AI-Advisor (R/D/T documents as the corpus)
- 5G Analyzer's AI layer (debug logs + 3GPP flow specs as the corpus)
- Future: Python Learning's content/explanation generation

This is the "project creates the next project" dependency chain — build the engine once inside the highest-value product, then reuse.

## Sequence

```
Phase 0 (now, days)        Python Learning adaptive loop v1
                            -> quick win, daily-use demo, builds momentum

Phase 1 (weeks 1-6)         AI-Advisor v1 (= Knowledge Core + R/D/T logic)
                            -> pick ONE small real test corpus (e.g. a slice of
                               5g-visualizer's own specs/flows as R+D, no Tests yet)
                            -> ingestion, gap detection ("Tests missing"), Q&A over R-D

Phase 2 (weeks 6-10)        Extract Knowledge Core as a standalone module
                            -> wire into 5G Analyzer: logs + flow specs -> "which
                               flow, where stuck" using the same retrieval engine

Phase 3 (later)             AI-Advisor v2 (full R-D-T stitching across real projects:
                            trading-tool, banking-tool, 5g-visualizer as test subjects)

Phase 4 (parked)            Voice Plugin — only once Phase 1-2 have real users
```

## How Claude Code is the backbone

- **Cross-project memory** (this session's memory files) holds the roadmap, vision, and decisions — so every session starts aligned, no re-explaining.
- **One coordination folder** (`AI-For-All/`) holds this strategy doc and, later, the shared Knowledge Core module spec — each product repo stays independent but references it.
- **Per-product sessions**: implementation work happens inside each repo (5g-visualizer, Practice-Python-Project, new `ai-advisor/`) with its own CLAUDE.md once conventions emerge.
- **This main session**: roadmap reviews, sequencing decisions, "what's next" — kept lightweight, no code.

## Education wing repos

| Repo | Purpose | Connection |
|---|---|---|
| `python-quiz-app` | Learn Python fundamentals (MCQ, topic tracking, Points to Remember) | Entry point |
| `use-python-build-rest` | Apply Python to build a REST API — GET/POST/PUT/PATCH/DELETE with live server state | "You learned Python, now build with it" — links back to Topics 3/4/6 of quiz app |

## Immediate next actions

1. Ship Python Learning adaptive loop v1 (level model + daily problem + memory tip) — small, self-contained, no blockers.
2. Define AI-Advisor v1 scope precisely: pick the test corpus (recommend: a small slice of 5g-visualizer's `content/flows` + `content/specs` as "Requirements + Design", deliberately with no "Tests" — perfect for demoing gap detection).
3. Scaffold a new `ai-advisor/` repo under Documents once scope is agreed.
