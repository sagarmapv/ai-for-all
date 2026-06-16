# AI-For-All — Port Registry

Every project must check this file before picking a port. No two projects share a port.

## Assigned ports

| Port | Project | Component | Notes |
|------|---------|-----------|-------|
| 5000 | `5g-visualizer` | Flask backend | |
| 8001 | `multi_agent_ai` | MCP tool server / main server | Fixed from 8000 (clashed with local k8s gateway on WSL) |
| 8002 | `multi_agent_ai` | Inventory agent | |
| 8003 | `multi_agent_ai` | Sales agent | |
| 8004 | `use-python-build-rest` | FastAPI backend | Fixed from 8000 |
| 8080 | `ai-advisor` | AI-Advisor API | |

## Reserved / system (do not use)

| Port | Owner |
|------|-------|
| 8000 | Local k8s gateway (WSL) |
| 11434 | Ollama (system) |

## Next available

`8005` — claim it here when a new project needs a port.
