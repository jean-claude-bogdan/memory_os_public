# Brief 03: Control Panel and Observability

## Mission
Specify the **new control panel**: one place to see and steer every agent, run, cost, and approval across Lily and Nazar.

## Key questions
1. Which open-source agent dashboards and control planes exist in 2026, and which are worth building on rather than writing from scratch?
2. Tracing standards: what is the state of OpenTelemetry GenAI semantic conventions? Which tools accept OTel traces from coding agents such as Claude Code, Codex, and Gemini CLI, using native OTel export or hooks?
3. Observability backends: compare Langfuse, Phoenix, Helicone, Opik, Laminar, and Grafana with OTel. Consider self-hosting weight on a small server, and cost per trace.
4. Cost and usage tracking across subscriptions and API keys: per agent, per task, and per Linear issue.
5. Human-in-the-loop UX: approval queues, "agent needs input" notifications to phone or Telegram/Slack, and live terminal attach (for example web tmux, ttyd, or xterm.js).
6. Which features matter most, ranked? Consider a live session list, logs, diffs, a cost burn-down, kill/pause/resume, rate-limit status, the memory graph, and an eval dashboard.
7. Build versus buy: should the existing Memory OS UI server become the panel, or should it embed an existing tool?

## Seed candidates (verify)
Langfuse, Arize Phoenix, Helicone, Opik, Laminar, AgentOps, ccusage and similar usage trackers, Claude Code OTel/hooks, Grafana with Tempo and Loki, ttyd, Wetty, and the Linear Agent/Insights views.

## Special deliverable
A **feature spec ranked by MVP, v1, and later**, a **wireframe description** of the main screens, and the **event schema** agents must emit.
