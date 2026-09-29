# Brief 13: Synthesis (Run Last)

## Inputs
`00_SHARED_CONTEXT.md` and all reports `reports/01` to `reports/12`.

## Mission
Merge the findings into **one coherent target harness** for Lily and Nazar.

## Deliverables
1. **Decisions table**: area | chosen tool or pattern | alternative | reason | cost/month | effort to adopt (S/M/L).
2. **Target architecture diagram** (Mermaid): Linear → dispatcher → agents (including the new one) → sandbox/worktree → evidence/evals → GitHub → deploy. Include Memory OS and the control panel, and show which parts run on Lily versus Nazar.
3. **Conflict resolution**: where reports disagree, pick one option and explain why.
4. **Migration plan** in phases (week 1, month 1, quarter 1). Each phase has Linear-ready issues with a 12-step score and acceptance criteria.
5. **What NOT to adopt**, with reasons.
6. **Updated templates to change in Memory OS**: `WORKFLOWS.md`, `SWARM_PROTOCOL.md`, `AGENT_RULES.md`, `HANDSHAKE.md`, and `swarm_invoke.py` contract. List the exact changes.
7. **Risks and open questions** for the owner.
