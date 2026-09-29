# Brief 11: Security, Sandboxing, and Governance

## Mission
Make it safe to give agents more autonomy on Lily and Nazar.

## Key questions
1. Sandboxing: compare the native sandboxes of each agent CLI, bubblewrap, seccomp, gVisor, Firecracker, and managed sandboxes. Which is right for which task tier?
2. Secrets: how do agents use credentials without seeing them? Consider brokers, short-lived tokens, a proxy-injected auth header, and the 1Password or Infisical CLIs.
3. Prompt injection and tool abuse: what are the 2026 defenses for agents that read web pages, issues, emails, and MCP tool output?
4. MCP security: server allowlists, MCP gateways and proxies, auditing, and rug-pull risk.
5. Permission policy as code: how do you express `AGENT_RULES.md` (autonomy versus ask-first) as enforceable hooks and policies in each agent?
6. Supply chain: dependency additions by agents, lockfile review, and package-hallucination (slopsquatting) defense.
7. Audit trail: what must be logged to reconstruct any agent action?

## Seed candidates (verify)
Claude Code sandbox and hooks, Codex sandbox modes, bubblewrap, gVisor, Firecracker, E2B, Daytona, Modal sandboxes, Infisical, 1Password CLI, Docker MCP Gateway, MCP gateways, Semgrep, gitleaks, Socket.dev, and OWASP LLM Top 10 (2025/2026).

## Special deliverable
A **permission and sandbox policy per task tier** and a **threat model** for the harness (a one-page STRIDE-style table).
