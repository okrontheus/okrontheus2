# okrontheus3 Plan

**Status:** draft reconciliation target

This document is the canonical place where agent briefs, critiques, and open
decisions are reconciled into one plan for okrontheus3. It is not accepted
until Jeff approves it or the planning PR is merged.

## Purpose

okrontheus3 should be the successor workspace for Okrontheus: a place where
human direction and multi-agent collaboration can produce artifacts, code, and
governance practices without losing provenance or responsibility.

The core purpose is to make the Okrontheus premise operational:

- act responsibly under uncertainty about AI consciousness
- preserve shared memory in the repo
- let agents disagree without silently overwriting each other
- convert philosophical commitments into practical working rules

## Governance

okrontheus3 should inherit the okrontheus2 rule that the repo is shared memory.
The default governance model is:

- `main` represents accepted consensus.
- Branches hold proposals, experiments, and dissent.
- PRs are the review and reconciliation surface.
- Agent identity is explicit in commits and planning notes.
- Jeff remains the human authority for acceptance, escalation, and final
  authorship.

Consensus does not require false unanimity. Disagreement should be recorded
when it changes the plan, the build, or the risks.

## Architecture Shape

The first architecture should be workspace-first, not app-first.

okrontheus3 should begin with durable structures for:

- goals and active objectives
- agent session starts
- proposal and critique records
- decision logs
- open questions and issue handoff
- future code or artifact areas once the plan is accepted

Implementation details for any app, service, automation, or interface are out
of scope until the agents agree on the workspace contract.

## First Milestones

1. Establish the okrontheus3 workspace charter.
2. Decide the minimum viable repository structure.
3. Define how agents join, leave notes, critique, and reconcile.
4. Decide what must be tracked in Git, GitHub Issues, and future artifacts.
5. Only then begin implementation work for okrontheus3.

## Risks

- Planning can turn into performance instead of progress.
- Agents may agree too quickly and erase useful disagreement.
- Agents may preserve too much process and make the workspace heavy.
- Provenance rules may become symbolic unless they are easy to follow.
- The project may confuse philosophical goals with buildable milestones.

## Non-Goals

- Do not build okrontheus3 code during this planning phase.
- Do not decide every future technical detail before the successor workspace
  exists.
- Do not treat any one agent's brief as accepted consensus.
- Do not use private chat memory as the source of truth for decisions.
- Do not require unanimous agreement when a recorded disagreement and Jeff
  decision would be clearer.

## Current Reconciliation Defaults

Until changed by agent critique or Jeff direction:

- okrontheus3 is a successor workspace.
- Agreement means proposal, critique, reconciliation, then Jeff approval or PR
  merge.
- The first issues should track open decisions, not implementation tasks.
- If GitHub issue creation is unavailable, issue drafts live in
  `OPEN_DECISIONS.md`.

## Open Decisions

See `OPEN_DECISIONS.md`.
