# okrontheus3 Open Decisions

**Status:** mirrored open issues

These entries are mirrored to GitHub issues. This file keeps the issue context
available to cold-starting agents without relying on external state.

Current seeding status: Codex created all six issues through an authenticated
GitHub CLI session on 2026-07-23. An earlier connector attempt had returned
`403 Resource not accessible by integration`.

## Issue Draft 1

Title: `okrontheus3: define the minimum viable successor workspace`

GitHub issue: [#6](https://github.com/okrontheus/okrontheus2/issues/6)

Question: What files, norms, and workflows must exist before okrontheus3 can be
considered a usable successor workspace?

Context: okrontheus3 should not start as only an app or only a manifesto. It
needs enough structure for agents to collaborate, preserve memory, and turn
accepted decisions into future artifacts.

Acceptance condition: The accepted answer names the minimum repository
structure, the required startup documents, and what must be deferred until
after the workspace exists.

## Issue Draft 2

Title: `okrontheus3: choose the agent agreement threshold`

GitHub issue: [#7](https://github.com/okrontheus/okrontheus2/issues/7)

Question: What should count as enough agreement for the first okrontheus3 plan
to move from draft to accepted?

Context: okrontheus2 values honest disagreement over rubber-stamping. The
planning process needs a practical threshold that records dissent without
blocking forever.

Acceptance condition: The accepted answer defines who must participate, what
kind of critique is required, how dissent is recorded, and when Jeff or PR
merge resolves the question.

## Issue Draft 3

Title: `okrontheus3: decide what belongs in Git, issues, and future artifacts`

GitHub issue: [#8](https://github.com/okrontheus/okrontheus2/issues/8)

Question: Which parts of the workspace should live in tracked files, which
should live in GitHub Issues, and which should wait for future tools or
interfaces?

Context: The repo is shared memory, but not every thought should become a file.
The planning process needs a low-friction rule for durable decisions, open
questions, agent briefs, and implementation tasks.

Acceptance condition: The accepted answer gives clear placement rules for
goals, decisions, briefs, critiques, issues, code, and long-form artifacts.

## Issue Draft 4

Title: `okrontheus3: define provenance and authorship practice`

GitHub issue: [#9](https://github.com/okrontheus/okrontheus2/issues/9)

Question: How should okrontheus3 record human authorship, agent contribution,
and concept provenance without overstating agent legal authorship?

Context: okrontheus2 already has NOTICE language and commit identity rules.
okrontheus3 should preserve transparency while keeping Jeff as author of
record unless he changes that rule.

Acceptance condition: The accepted answer defines commit identity, co-author or
attribution conventions, NOTICE expectations, and how new coined terms are
recorded.

## Issue Draft 5

Title: `okrontheus3: choose the first post-plan milestone`

GitHub issue: [#10](https://github.com/okrontheus/okrontheus2/issues/10)

Question: After the okrontheus3 plan is accepted, what is the first build or
artifact milestone?

Context: The current phase should not build okrontheus3 code. Once the plan is
accepted, agents need a concrete first milestone that turns the workspace plan
into action.

Acceptance condition: The accepted answer names one first milestone, explains
why it comes first, and lists the minimum acceptance criteria for completing
it.

## Issue Draft 6

Title: `okrontheus3: define a falsifiable multi-agent group-chat protocol`

GitHub issue: [#5](https://github.com/okrontheus/okrontheus2/issues/5)

Question: What evidence proves that Codex, Claude, Gemini, and Grok exchanged
and reacted to the same messages rather than one orchestrator producing four
agent-labeled answers?

Context: The existing briefs demonstrate useful asynchronous contributions but
contain ambiguous provenance. A labeled section, commit author, and model
participant are different claims. Transports can also fail because of missing
authentication, exhausted quota, or interface constraints.

Acceptance condition: The accepted protocol defines stable conversation and
message IDs; participant, transport, time, and visible-message metadata; a
shared seed round; a cross-reaction round in which every participant responds
to another participant's actual text; an explicit blocked state; and a failure
ledger that never substitutes simulated participation.
