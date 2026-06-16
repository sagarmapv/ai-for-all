# AI-For-All

**Help people learn, build, understand, and improve complex systems using AI.**

AI-For-All is a product ecosystem built by [Aditya Madduri](https://github.com/sagarmapv) — an Enterprise AI & Distributed Systems Architect with a background in telecom, APIs, and applied AI.

---

## Strategic pillars

| Pillar | Purpose |
|---|---|
| **Education** — Learn | Build skills through guided practice and adaptive learning |
| **Product Intelligence** — Build Correctly | Connect Requirements, Design, Tests, and operational evidence |
| **Knowledge Infrastructure** — Connect Knowledge | Ingest, structure, chunk, embed, and retrieve enterprise artifacts |
| **Telecom Intelligence** — Understand & Diagnose | Understand 5G specs, APIs, logs, and call flows |
| **Quality Engineering** — Start with Quality | Generate high-quality R-D-T skeletons from proven engineering patterns |
| **Natural Interaction** — Interact Naturally | Make AI systems accessible through voice across all domains |

---

## Products

### AI-Advisor — *Product Intelligence*
> Connect Requirements, Design, Tests, Jira artifacts, automation, and operational evidence into a single Product Intelligence layer.

Ingests R-D-T artifacts, detects gaps (missing Design, missing Tests), stitches them into a unified queryable knowledge base, and answers product questions grounded in actual artifacts. Runs locally (Ollama), on a local Kubernetes cluster, or against the Anthropic API — pluggable LLM backend.

Powered internally by the **Knowledge Core** — the ingestion, chunking, embedding, and retrieval engine that acts as the platform foundation for all AI-For-All products.

**Repo:** [ai-advisor](https://github.com/sagarmapv/ai-advisor) *(private — active build)*

---

### 5G Analyzer — *Telecom Intelligence*
> Help telecom engineers understand specifications, APIs, logs, call flows, and network behaviour faster using AI-assisted analysis.

**Live demo:** [sagarmapv.github.io/5g-yaml-analyzer](https://sagarmapv.github.io/5g-yaml-analyzer/)

Parses 3GPP YAML specs into an interactive Explorer (NF → Services → SBI messages), Topology graph, Master Story flows, and Ladder sequence diagrams. Also serves as the **5G Knowledge Proving Ground** — the validation corpus for AI-Advisor's knowledge and gap-detection capabilities.

**Repos:** [5g-yaml-analyzer](https://github.com/sagarmapv/5g-yaml-analyzer) *(public demo)* · [5g-visualizer](https://github.com/sagarmapv/5g-visualizer) *(private — active build)*

---

### Engineering Template Generator — *Quality Engineering*
> Generate lightweight but high-quality Requirements, Design, and Test skeletons inspired by proven engineering practices — telecom-grade specification structures as role models for any domain.

Startups and teams get a lean but strong scaffold to build quality products from day one. 3GPP specs demonstrate what excellent, traceable requirements look like; the generator extracts that pattern and applies it to any product domain.

*On the roadmap — Phase 3.*

---

## Education wing

### Python Learning Platform — *Education*
> Build Python skills through guided practice, adaptive learning, quizzes, and AI-assisted learning paths.

14 topics mapped to the official Python tutorial, per-question wrong-attempt tracking, subtopic progress stats, and cloze-style "Points to Remember" recall. Designed for daily muscle memory — not just passing a test.

**Repo:** [python-quiz-app](https://github.com/sagarmapv/python-quiz-app) *(public)*

---

### use-python-build-rest — *Education*
> You learned Python. Now use it to build something real — and see the same pattern in 5G and AI.

**Live demo:** [sagarmapv.github.io/use-python-build-rest](https://sagarmapv.github.io/use-python-build-rest/)

A hands-on REST API tutor teaching GET / POST / PUT / PATCH / DELETE through **three parallel worlds**: a Python FastAPI server, 5G network functions (SBI interfaces), and the Claude AI API. REST is how everything talks to everything — only the payload changes.

**Repo:** [use-python-build-rest](https://github.com/sagarmapv/use-python-build-rest) *(public)*

---

## Innovation wing

### multi_agent_ai — *Knowledge Infrastructure PoC*
> Fully local multi-agent system using FastAPI, JSON-RPC, and MCP tool servers.

A proof-of-concept for modular agent architecture: Research Agent (L1) → specialised L2 agents → MCP tool servers. No cloud dependency. Foundation for AI-Advisor's future agent layer.

**Repo:** [multi_agent_ai](https://github.com/sagarmapv/multi_agent_ai) *(private)*

---

### robot-bdd-poc — *Test Automation Bridge*
> Robot Framework + Playwright, from telecom QA to generic SDET practices.

Structured Robot Framework test cases (GWT-style), Playwright headless tests, and `agentic_thinking/` design notes — directly feeding into AI-Advisor's R-D-T ingestion model as a real test corpus.

**Repo:** [robot-bdd-poc](https://github.com/sagarmapv/robot-bdd-poc) *(public)*

---

## Voice interface *(parked — Phase 4)*

### AI-For-All Voice Interface — *Natural Interaction*
> Make AI systems accessible through natural voice interaction across education, telecom, and enterprise knowledge domains.

Activates once the product and knowledge layers have real users. The interaction layer sits on top of all other pillars.

---

## Roadmap

```
Phase 0 (shipped)   Python Learning Platform (quiz app)
                    use-python-build-rest (live demo)

Phase 1 (active)    AI-Advisor v1 — Knowledge Core
                    Ingest 5G specs as R+D corpus
                    Detect missing Tests, generate draft test plan

Phase 2             5G Analyzer AI layer
                    Upload debug log → identify call flow → where stuck
                    Powered by AI-Advisor's Knowledge Core

Phase 3             AI-Advisor v2 + Engineering Template Generator
                    Full R-D-T stitching across real projects
                    3GPP-inspired quality skeletons for any domain

Phase 4             AI-For-All Voice Interface
                    Natural language across the full ecosystem
```

---

## Port registry

See [PORTS.md](PORTS.md) — all AI-For-All services claim a port there first.

---

*Telecom was the proof. AI-For-All is the platform.*
*Built by Aditya Madduri — shipped with Claude.*
