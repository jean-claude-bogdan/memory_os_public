# Brief 09: Deployment and Infrastructure

## Mission
Define how agent work gets **shipped safely**, and how Lily and Nazar themselves are run and kept reproducible.

## Key questions
1. Agent-in-CI: compare GitHub Actions with Claude Code, Codex, or Gemini actions, self-hosted runners on Lily or Nazar, and cost and security trade-offs.
2. Preview environments for each PR or agent branch: which options are self-hosted and which are managed? Supabase branching is available.
3. Self-hosted PaaS options for small servers: compare Coolify, Dokploy, Kamal, and CapRover.
4. Server reproducibility: compare Nix, Ansible, and Docker Compose. How do you rebuild Lily or Nazar from scratch?
5. Remote access and networking: Tailscale, Cloudflare Tunnel, and SSH hardening for agent servers.
6. Release safety: feature flags, canary releases, automatic rollback, and who can merge to main (human-only gate).
7. GPU and inference ops if Lily or Nazar serve local models: compare vLLM, SGLang, llama.cpp, and Ollama for serving and scheduling alongside agents.

## Seed candidates (verify)
anthropics/claude-code-action, openai/codex-action, google-github-actions/run-gemini-cli, Coolify, Dokploy, Kamal, Tailscale, Cloudflare Tunnel, Nix and NixOS, Ansible, Supabase branching, and Vercel and Netlify previews.

## Special deliverable
A **deployment pipeline diagram** (branch → CI → preview → review → merge → deploy → monitor → rollback) and a **server bootstrap checklist** for Lily and Nazar.
