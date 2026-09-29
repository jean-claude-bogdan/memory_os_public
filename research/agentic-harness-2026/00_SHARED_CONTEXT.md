# Shared Context for Every Research Agent

Read this before your brief. It describes the stack you are researching for, the rules of the research, and the required report format.

## 1. Who this is for

A solo builder or small team running a self-hosted, multi-agent development harness. Agents work from terminals on two Linux servers, **Lily** and **Nazar**, and are coordinated by self-made tooling. The goal is to upgrade the harness so it can: add one more coding agent, get a better workflow and control panel, and have strong, repeatable agent workflows across planning, execution, design, marketing, research, coding, testing, and deployment.

## 2. Current stack (known from the `memory_os` repository)

- **Memory OS** (Python, local-first, no mandatory dependencies): an agent memory graph kept in `memory/nodes.jsonl` and `memory/edges.jsonl`, indexed into SQLite FTS5. It adds a temporal knowledge graph, layered retrieval, memory decay, and a query cache. Its CLI includes `init`, `sync`, `search`, `compact`, `triage`, and others.
- **Engineering control plane** (in Memory OS): idea → spec → contract → context pack → implementation → evidence → review pack. Also includes evals, release checks, token budgets, routing, a prompt registry, and run records.
- **Spec-driven workflow**: `spec.md`, `plan.md`, `tasks.md`, and `checklist.md`, plus a project constitution.
- **12-step task scale** (`WORKFLOWS.md`): tasks are scored from 1 (nano) to 12 (giant), and the score picks the model tier. Scores 9 to 12 trigger the **Swarm Protocol**: an orchestrator splits the work into subtasks, writes them to `swarm_backlog.json`, and dispatches workers through `scripts/swarm_invoke.py --target={claude|agy|codex}`. That script traps rate limits and parks tasks as `pending_limit`.
- **Agent handoff**: `HANDSHAKE.md`, verified on every read. `AGENT_RULES.md` separates autonomy (allowed without approval) from ask-first actions.
- **Coding agents in use**: Claude Code, Codex CLI, and Google Antigravity (`agy`). Rules are also exported to Cursor and Claude Code skills.
- **LLM routing**: Ollama (small local models), MLX (Apple Silicon), vLLM on a desktop box, OpenAI-compatible APIs, Gemini, and OpenRouter. LiteLLM is available as an adapter.
- **Integrations and adapters**: Linear (GraphQL sync), Notion, Google Drive, Obsidian export, MCP adapter, Temporal, Qdrant, DuckDB, and Langfuse, Phoenix, OTel, and MLflow exporters. Bridges exist for CrewAI, AutoGen, LlamaIndex, Haystack, Semantic Kernel, and PydanticAI.
- **UI**: a local UI server and a 3D memory-graph HTML view.
- **Also connected on the account**: GitHub, Supabase, Figma, Gamma, Google Workspace (Gmail, Calendar, Drive).
- **Project management**: **Linear is the system of record.**

## 3. Unknowns: [FILL] before dispatching

- Lily: [FILL: OS, CPU/GPU/RAM, role such as agent runner or inference]
- Nazar: [FILL: OS, CPU/GPU/RAM, role]
- How agents run today: [FILL: tmux / screen / systemd / Docker / other]
- The coding agent you want to add, if you have one in mind: [FILL or "open"]
- Monthly budget for subscriptions and APIs: [FILL]
- Main products or projects the harness serves, such as SaaS, content, or client work: [FILL]
- Hard constraints, such as self-hosted only, EU data residency, or no vendor X: [FILL]

## 4. Research rules

- **Time window**: prefer sources from **2025-06 to today (2026-09)**. Flag anything older as "legacy but still relevant".
- **Primary sources first**: GitHub repos, official docs, changelogs, and maintainers' posts. Treat vendor marketing and "top 10" listicles as leads to verify, not as evidence.
- **For every GitHub project, report**: stars, last commit date, release cadence, license, open-issue health, and bus factor (one maintainer or an organization).
- **Fit over hype**: judge every recommendation against the stack in section 2. Say explicitly what it **replaces**, what it **complements**, and what it **conflicts with** (for example, Memory OS memory, the swarm protocol, or Linear).
- **Self-hosted or local-first is preferred** when quality is comparable. State lock-in and pricing.
- **No invented facts.** If you cannot verify a claim, mark it `UNVERIFIED`. Seed names in the briefs are leads that may be outdated, not recommendations.
- **Stay inside your brief's scope.** Note cross-area findings in one line under "Handoffs to other areas".

## 5. Required report format

Save your report as `reports/NN_<area>.md` with exactly these sections:

1. **TL;DR**: 5 bullets at most, each one a decision or recommendation.
2. **Best practices (2026)**: numbered practices. Each has what to do, why, and a source link.
3. **Tool landscape table** with these columns: `Name | Link | Category | License | Stars | Last release | Self-host? | Pricing | Fit (1-5) | Replaces / Complements / Conflicts`.
4. **Recommended setup for this stack**: a concrete choice, how it plugs into Memory OS, the swarm protocol, Linear, and Lily/Nazar, and the config or commands needed to start.
5. **Reference workflow**: a step-by-step agent workflow for this area, with human gates marked `[HUMAN]`, and mapped to the 12-step scale where relevant.
6. **Anti-patterns and risks**.
7. **Open questions for the owner**.
8. **Handoffs to other areas**.
9. **Sources**: a list of links with access dates.

Target length: 1,500 to 3,000 words. Tables are preferred over prose.
