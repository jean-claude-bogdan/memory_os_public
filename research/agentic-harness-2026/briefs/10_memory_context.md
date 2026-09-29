# Brief 10: Memory and Context Engineering

## Mission
Benchmark **Memory OS** against the 2026 state of the art in agent memory and context engineering. Decide what to keep, what to adopt, and what to drop.

## Key questions
1. Agent memory systems in 2026: compare architectures (temporal graphs, vector stores, hybrid retrieval, reflection and consolidation). How does Memory OS (JSONL → SQLite FTS5, temporal KG, decay, cache) compare?
2. Context engineering practice: CLAUDE.md, AGENTS.md, skills, subagents, compaction, context packs, and progressive disclosure. What measurably improves agent success?
3. Cross-agent memory: how can Claude, Codex, Antigravity, and the new agent share one memory? Consider MCP memory servers, rules export, and AGENTS.md sync.
4. Memory evals: retrieval relevance and faithfulness benchmarks (Memory OS has two eval suites; compare them with public ones).
5. Semantic search upgrade: when is embeddings plus a reranker worth it over FTS5? Local embedding models on Lily or Nazar.
6. Memory hygiene: poisoning, staleness, conflicting facts, and PII.

## Seed candidates (verify)
Zep and Graphiti, Letta, mem0, Cognee, LangMem, the MCP memory server, Claude memory tools, sqlite-vec, Qdrant (adapter exists), and LongMemEval and LoCoMo benchmarks.

## Special deliverable
A **keep, adopt, or drop table** for Memory OS components and a **prioritized Memory OS roadmap** (the top 5 changes).
