# Agentic Harness Research, 2026

This folder breaks down the research needed to upgrade the multi-agent harness that runs on the **Lily** and **Nazar** servers.

## How to dispatch

1. Fill in the `[FILL]` fields in `00_SHARED_CONTEXT.md`. It takes about 5 minutes and every agent depends on it.
2. For each brief in `briefs/`, send one research agent **`00_SHARED_CONTEXT.md` followed by the brief**, in that order.
3. Collect the reports into `reports/NN_<area>.md`, using the same numbers as the briefs.
4. Run brief `13_synthesis.md` last, with all reports attached. It produces the target architecture, the stack decision, and a migration plan.

The briefs are independent. Briefs 01 to 12 can run in parallel.

| # | Area | Main decision it feeds |
|---|---|---|
| 01 | Coding agents and CLIs | Which coding agent to add, and how to wrap it |
| 02 | Orchestration and execution | How work is dispatched, isolated, and run in parallel |
| 03 | Control panel and observability | What the new control panel is built on |
| 04 | Planning and specs | Idea → spec → Linear issue → task flow |
| 05 | Research workflows | Deep-research agent pipeline |
| 06 | Design and UI | Design → code loop |
| 07 | Marketing and content | Content and growth agent loop |
| 08 | Testing, QA, and evals | Verification gates and agent evals |
| 09 | Deployment and infrastructure | CI/CD, server ops, and preview environments |
| 10 | Memory and context engineering | Memory OS roadmap versus off-the-shelf tools |
| 11 | Security, sandboxing, and governance | Permissions, secrets, and prompt-injection defense |
| 12 | Linear as the system of record | Linear ↔ agents ↔ GitHub integration |
| 13 | Synthesis (run last) | Target architecture and migration plan |
