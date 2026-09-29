# Brief 02: Orchestration and Execution

## Mission
Define the best 2026 pattern for **running many coding agents in parallel** on Lily and Nazar. This covers dispatch, isolation, scheduling, retries, and merging, and it should upgrade the current Swarm Protocol.

## Key questions
1. Parallel-agent managers: compare tools built on tmux, git worktrees, and containers that run many agent sessions at once. Which ones are headless and server-friendly, as opposed to desktop-only?
2. Isolation: compare git worktrees, containers per task, devcontainers, and microVMs. What is the right default for each task tier?
3. Durable execution: when is a workflow engine such as Temporal, Inngest, Hatchet, Restate, or DBOS worth it over a JSON backlog and a queue? Memory OS already has a Temporal adapter and a SQLite queue.
4. Scheduling across two servers: how should work be split between Lily and Nazar? Consider placement, concurrency limits, pooling subscription rate limits, and resuming after `pending_limit`.
5. Orchestrator patterns: compare orchestrator-worker, planner-executor-verifier, and a Kanban pull model. What does the evidence say about when multi-agent setups beat a single agent and when they hurt?
6. Merging and conflicts: compare file-ownership locks, stacked PRs, a merge queue, and automatic rebasing.
7. Long-running autonomy: checkpoints, resume, loop and budget guards, and "stop and ask" triggers.

## Seed candidates (verify)
claude-squad, vibe-kanban, Conductor, Crystal, Sculptor, container-use (Dagger), uzi, OpenHands, SWE-agent and mini-swe-agent, LangGraph, Temporal, Inngest, Hatchet, the Claude Agent SDK, and the OpenAI Agents SDK.

## Special deliverable
A **target execution architecture diagram** (Mermaid) showing Linear issue → dispatcher → isolated worker (per agent) → evidence → PR → review. Also give a **swarm_backlog.json v2 schema**.
