# Brief 06: Design and UI Workflows

## Mission
Define the best agent-assisted **design → code → visual QA** loop for product UIs. Figma is already connected.

## Key questions
1. Figma ↔ code agents: what can the Figma MCP (Dev Mode and write-back) and Code Connect do in 2026? What are their limits?
2. Generative UI tools and whether their output is production-grade: compare v0, Lovable, Bolt, Claude artifacts and design tools, and others.
3. Design systems for agents: shadcn registries and MCP, token pipelines, Storybook MCP, and component documentation that agents can read.
4. Visual QA: screenshot diffing, Playwright-driven visual review by agents, and accessibility checks (axe).
5. How should brand and design rules be encoded so every agent follows them? Consider skills, rules files, and design-lint.
6. Where is a human designer gate needed, and where is it not?

## Seed candidates (verify)
Figma MCP, Code Connect, shadcn/ui registry and MCP, Storybook, Chromatic, Playwright MCP, v0, Lovable, Anima, Builder.io, Tokens Studio, and Style Dictionary.

## Special deliverable
A **design pipeline** with one tool per step, plus a **"design rules" skill template** that agents load.
