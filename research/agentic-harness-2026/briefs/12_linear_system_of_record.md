# Brief 12: Linear as the System of Record

## Mission
Make **Linear** the single control surface for all agent work: agents take issues, report progress, and link PRs, and humans approve inside Linear.

## Key questions
1. Linear's agent platform in 2026: agent users, agent sessions and activities API, delegation, webhooks, the official MCP server, and Triage Intelligence. What is available and what are the limits?
2. Which coding agents natively integrate with Linear (assign an issue → the agent opens a PR)? How would a self-hosted agent on Lily or Nazar register as a Linear agent?
3. Mapping: how should the 12-step score, swarm subtasks, agent assignment, `pending_limit`, and evidence map onto Linear fields (labels, estimates, custom fields, sub-issues, cycles)?
4. Two-way sync design between Linear, Git specs, and Memory OS without duplicate truth. What does the current `linear_sync.py` need?
5. GitHub ↔ Linear automation: branch naming, PR linking, auto-status transitions.
6. Reporting: cycle metrics for agent throughput and cost per issue.

## Seed candidates (verify)
Linear Agents API and SDK, Linear MCP, Linear webhooks, Linear ↔ GitHub integration, and the Linear integrations of Codex, Cursor, Devin, Factory, and Claude.

## Special deliverable
A **Linear workspace blueprint** (teams, workflow states, labels, custom fields, templates) and an **agent ↔ Linear event contract**.
