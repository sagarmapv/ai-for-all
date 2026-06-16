# AI-For-All

**Help people understand complex systems using AI.**

AI-For-All is a personal product ecosystem built by [Aditya Madduri](https://github.com/sagarmapv) — an Enterprise AI & Distributed Systems Architect with a background in telecom, APIs, and applied AI.

Each product solves a real understanding problem: understand a 5G network, understand a product's requirements and tests, understand Python, understand REST APIs.

---

## Products

### AI-Advisor — *Knowledge Core*
> Ingest Requirements, Design, and Tests. Detect what's missing. Answer questions about your product.

AI-Advisor takes R-D-T artifacts (requirements docs, design specs, test cases) and does three things:
- Detects gaps — missing Design when only Requirements exist, missing Tests when Requirements+Design are present
- Stitches Requirements, Design, and Tests into a unified, queryable knowledge base
- Answers product questions grounded in the actual artifacts, not hallucination

Runs locally (Ollama), on a local Kubernetes cluster, or against the Anthropic API — pluggable LLM backend.

**Repo:** [ai-advisor](https://github.com/sagarmapv/ai-advisor) *(private — active build)*

---

### 5G Analyzer — *Telecom Intelligence*
> Parse 5G SBI OpenAPI specs. Explore network functions, call flows, and sequence diagrams.

A web tool that turns 3GPP YAML specs into an interactive Explorer (NF → Services → SBI messages), Topology graph, Master Story flows, and Ladder sequence diagrams. The AI log-correlation layer (upload a debug log, identify which call flow and where it's stuck) is on the roadmap.

**Repo:** [5g-yaml-analyzer](https://github.com/sagarmapv/5g-yaml-analyzer) *(public)*

---

## Education Wing

### Python Quiz App — *Learn Python*
> Topic-by-topic Python MCQs mapped to the official Python tutorial. Track what you know, reinforce what you don't.

14 topics from the official Python docs, per-question wrong-attempt tracking, subtopic progress stats, and cloze-style "Points to Remember" recall. Designed to build daily muscle memory, not just pass a test.

**Repo:** [python-quiz-app](https://github.com/sagarmapv/python-quiz-app) *(public)*

---

### use-python-build-rest — *Apply Python*
> You learned Python. Now use it to build something real.

A hands-on REST API tutor: a live FastAPI server with one CRUD resource, an interactive HTML client that fires GET / POST / PUT / PATCH / DELETE and shows the server state changing in real time. Each part of the server is mapped back to the Python topics from the quiz app — so learners see exactly which concepts they already know doing real work.

**Repo:** [use-python-build-rest](https://github.com/sagarmapv/use-python-build-rest) *(active build)*

---

## Innovation Wing

### multi_agent_ai — *Local Multi-Agent Architecture PoC*
> Fully local multi-agent system using FastAPI, JSON-RPC, and MCP tool servers.

A proof-of-concept for a modular agent architecture: a Research Agent (L1) interprets user prompts, routes to specialised L2 agents (Sales, Inventory), which call MCP tool servers backed by Pandas DataFrames. No cloud dependency. Foundation for AI-Advisor's future agent layer.

**Repo:** [multi_agent_ai](https://github.com/sagarmapv/multi_agent_ai) *(private)*

---

### robot-bdd-poc — *Test Automation Bridge*
> Robot Framework + Playwright, from telecom QA to generic SDET practices.

Structured Robot Framework test cases (GWT-style), Playwright headless tests, and an `agentic_thinking/` folder with design notes on automating test generation — directly feeding into AI-Advisor's R-D-T ingestion model.

**Repo:** [robot-bdd-poc](https://github.com/sagarmapv/robot-bdd-poc) *(public)*

---

## Roadmap

```
Phase 0 (now)     Python Quiz App adaptive loop
                  use-python-build-rest launch

Phase 1           AI-Advisor v1 — Knowledge Core
                  Ingest 5G specs as R+D corpus
                  Detect missing Tests, generate draft test plan

Phase 2           5G Analyzer AI layer
                  Upload debug log → identify call flow → locate where stuck
                  Powered by AI-Advisor's Knowledge Core

Phase 3           AI-Advisor v2
                  Full R-D-T stitching across real projects
                  Startup skeleton templates from 3GPP spec patterns

Phase 4           Voice Plugin
                  Natural language interface over the full ecosystem
```

---

## Common thread

Every product here is about the same thing: **translating complex technical systems into something humans can understand** — whether that's a 5G network, a product's requirements, Python code, or an API.

Telecom was the proof. AI-For-All is the platform.

---

*Built with intention by Aditya Madduri — guided by curiosity, shipped with Claude.*
