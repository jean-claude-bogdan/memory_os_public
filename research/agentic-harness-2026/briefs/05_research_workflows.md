# Brief 05: Research Workflows

## Mission
Design a reusable **deep-research agent pipeline** for market, technical, and competitive research. Its output should flow into Memory OS as nodes with sources.

## Key questions
1. What are the 2026 deep-research architectures (plan → parallel search → read → synthesize → cite → verify)? What does the evidence show about quality?
2. Search and scraping APIs: compare quality, price, rate limits, and self-hosting options.
3. Citation integrity: how are hallucinated citations detected, and how is claim-level verification done?
4. Open-source deep-research frameworks that can run on Lily or Nazar with mixed local and cloud models.
5. How should research outputs be stored so later agents can retrieve them? Consider Memory OS node types, trust levels, source-freshness decay, and the existing temporal graph.
6. GitHub and tech-radar research: how can the harness keep checking for new repos and tools in the stack's categories, and alert only on relevant changes?

## Seed candidates (verify)
GPT Researcher, STORM, open deep-research implementations, Exa, Tavily, Firecrawl, Jina Reader, Perplexity API, Brave Search API, SearXNG, Crawl4AI, and MarkItDown (an adapter already exists).

## Special deliverable
A **research agent spec** (inputs, stages, stop criteria, output schema that maps to Memory OS nodes) and a **weekly tech-radar routine** design.
