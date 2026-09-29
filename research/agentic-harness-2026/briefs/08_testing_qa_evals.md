# Brief 08: Testing, QA, and Evals

## Mission
Make "done" mean **verified**. Define the testing gates for agent-written code and the eval practice for the agents and prompts themselves. This extends the Memory OS `evidence` and `eval` commands.

## Key questions
1. What are the best practices for agent-generated tests? Consider test-first versus test-after, mutation testing to catch weak tests, property-based tests, and spotting tests the agent changed just to make them pass.
2. E2E and browser testing by agents: compare Playwright MCP, Stagehand, browser-use, and computer-use agents. Which are reliable and which are flaky?
3. AI code review: automated reviewers on PRs, and model-diverse review (for example Claude writes and another model reviews). What evidence shows it catches bugs?
4. Agent and prompt evals: compare frameworks, how to build a regression suite from real failures, LLM-as-judge calibration, and eval-driven prompt changes.
5. Harness-level benchmarks: how to measure whether a new agent or model is better on *your own* tasks (a private mini SWE-bench built from past Linear issues).
6. Gates by task tier: which checks are required at scores 1 to 5, 6 to 8, and 9 to 12?

## Seed candidates (verify)
Playwright and Playwright MCP, Stagehand, browser-use, Stryker, mutmut, Hypothesis, promptfoo, Inspect AI, DeepEval, Braintrust, OpenAI Evals, CodeRabbit, Greptile, Claude Code Review, Copilot review, and SWE-bench tooling.

## Special deliverable
A **verification gate matrix** (tier × required checks) and a design for a **private benchmark** built from the owner's Linear and GitHub history.
