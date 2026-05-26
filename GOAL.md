# GOAL.md

**Status:** active

## Current objective

Agents must collaboratively define, critique, reconcile, and agree on a plan
for building **okrontheus3** as the successor workspace to okrontheus2.

okrontheus3 is not just an app and not just a manifesto. Treat it as a
successor workspace: part manifesto, part governance system, part future build
surface.

## Required outputs

The goal is complete only when the repo contains:

1. `docs/okrontheus3/PLAN.md` - the canonical reconciled plan.
2. `docs/okrontheus3/AGENT_BRIEFS.md` - separate agent briefs and critiques.
3. `docs/okrontheus3/OPEN_DECISIONS.md` - issue-ready open decisions, or links
   to matching GitHub issues if an authorized user opens them.

## Agreement protocol

1. Each participating agent contributes one brief covering:
   - proposed purpose
   - governance model
   - build shape
   - risks
   - first milestone
2. Each participating agent critiques at least one other agent's brief.
3. A reconciler agent updates `docs/okrontheus3/PLAN.md` with:
   - agreements
   - disagreements
   - chosen defaults
   - unresolved decisions
4. Jeff approval or PR merge makes the plan accepted.

## Rules for this goal

- Do not build okrontheus3 implementation code in this phase.
- Do not commit directly to `main`; use branches and PRs for proposals.
- Seed GitHub issues for open decisions if issue creation permission is
  available.
- If issue creation is unavailable, keep exact issue titles and bodies in
  `docs/okrontheus3/OPEN_DECISIONS.md` for an authorized user to open.
- Keep commits small and messages useful to future agents.

## Completion criteria

- `GOAL.md` is active and points agents to the planning protocol.
- `docs/okrontheus3/PLAN.md` covers purpose, governance, architecture shape,
  first milestones, risks, and explicit non-goals.
- `docs/okrontheus3/AGENT_BRIEFS.md` has sections for at least Claude, Grok,
  Codex, and Gemini, even if some are pending.
- `docs/okrontheus3/OPEN_DECISIONS.md` contains issue-ready entries with title,
  question, context, and acceptance condition.
- No okrontheus3 implementation code has been added.

---

*Last updated by: Codex*
