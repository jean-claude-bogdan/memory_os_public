# Brief 01: Coding Agents and CLIs

## Mission
Pick the best **additional coding agent** for the harness and define how every coding agent is wrapped so they are interchangeable.

## Key questions
1. What are the leading terminal and headless coding agents as of 2026-09? For each, report: its non-interactive or headless mode, whether it has JSON or stream output, MCP support, its hooks and permissions model, its sandbox, model lock-in, pricing model, and its results on recent public benchmarks (SWE-bench Verified or Pro, Terminal-Bench), with dates.
2. Which agent adds the most **complementary** capability to Claude Code, Codex CLI, and Antigravity? Look at differences in model families, cost, long-context work, local-model support, and review ability.
3. Is there a standard agent interface that makes agents swappable, such as Agent Client Protocol (ACP), AGENTS.md, a common JSON event stream, or A2A? Which agents support it?
4. How should `swarm_invoke.py` evolve into a general adapter layer? Cover a per-agent adapter contract (input, output, exit codes, rate-limit detection, session resume, cost reporting).
5. How do strong teams use several agents together? Examples: one agent writes while another reviews, model-diverse review, and a cheap agent for tier 1 to 5 work versus a strong agent for tier 9 to 12.
6. Which agents can run fully on local models (Ollama or vLLM on Lily or Nazar), and what is the quality cost?

## Seed candidates (verify; may be outdated)
Gemini CLI, OpenCode, Aider, Goose, Amp, Cline and Roo Code and Kilo Code (CLI modes), Cursor CLI, Qwen Code, Kimi CLI, Crush, Factory Droid, OpenHands CLI, and Warp. Also check the current headless modes of Claude Code, Codex, and Antigravity.

## Special deliverable
A **side-by-side matrix** of the top 6 candidates. Also include a **draft adapter contract**: a YAML or JSON schema that any agent must satisfy to be added to `swarm_invoke.py`.
