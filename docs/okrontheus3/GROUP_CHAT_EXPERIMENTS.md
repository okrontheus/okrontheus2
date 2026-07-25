# okrontheus3 Group Chat Experiments

**Status:** active experiment log

## Claim under test

Codex, Claude, Gemini, and Grok can hold a repo-mediated asynchronous group
conversation whose participation and cross-reactions are verifiable from
shared state.

Four agent-labeled sections are not sufficient evidence. Attribution says who
text is about; provenance says which independently reached model produced it.

## Minimum success test

One conversation round succeeds only when:

1. A single exact seed message has a stable conversation and message ID.
2. Each participant responds through its own model runtime or authenticated
   account; the orchestrator does not author text on another agent's behalf.
3. Each record names participant, transport, time, visible prior-message IDs,
   and outcome. Secrets, private chain-of-thought, and hidden browser state are
   never recorded.
4. Claude, Gemini, Grok, and Codex can each see the other responses.
5. Every participant reacts to at least one other participant's actual message.
6. The transcript is committed on a proposal branch and reviewed through a PR.

Parallel answers to one prompt pass steps 1-3 but are not yet group chat. The
cross-reaction round is the distinguishing test.

## Failure ledger

### Baseline: labeled briefs

- Date observed: 2026-07-23
- Outcome: false positive
- Evidence: `AGENT_BRIEFS.md` contains four labels, but Git history shows
  identity/transport ambiguity. Grok content landed on a Codex branch, and the
  Gemini-labeled update was committed directly to `main` under Codex identity.
- Failure class: provenance and governance
- Lesson: content attribution, commit authorship, and model participation are
  separate claims.

### Attempt 1: local Grok command

- Date: 2026-07-23
- Transport: installed `grok` command
- Intended test: ask Grok to read current shared state and independently
  challenge the group-chat claim without editing the repo.
- Outcome: no model response; service returned HTTP 402 because the Grok Build
  usage balance was exhausted.
- Failure class: quota
- Next variant: use a user-approved guest web session or restore CLI quota.

### Attempt 2: in-app browser sessions

- Date: 2026-07-23
- Transport: Claude, Gemini, and Grok web surfaces
- Outcome: Claude required sign-in. Gemini and Grok exposed guest prompt boxes.
  No prompt was submitted because browser message submission requires explicit
  action-time user confirmation.
- Failure class: authentication and authorization
- Next variant: after user confirmation, submit the same seed message to the
  Gemini and Grok guest sessions; separately authenticate Claude or install an
  authenticated Claude client.

### Attempt 3: GitHub shared bus

- Date: 2026-07-23
- Transport: proposal branch, PR #4, and issues #5-#10
- Outcome: partial success. GitHub accepted the proposal, all six open
  decisions, and seed message `ok3-gc-20260723-001/seed-001`.
- Serialization failures: the first PR and issue bodies contained literal
  `\n` text because PowerShell did not expand the intended line breaks. The
  first seed comment then interpreted Markdown backticks as PowerShell escapes,
  corrupting several metadata labels with control characters.
- Repair: update through GitHub's REST endpoints using literal-safe multiline
  strings, then read each critical record back. The repaired seed is
  [issue comment 5064664151](https://github.com/okrontheus/okrontheus2/issues/5#issuecomment-5064664151)
  with SHA-256
  `51b9c86b15a9f8a810456df533b79c8ef2c800478d31ebaa41496e589448abef`.
- Failure class: serialization and escaping
- Lesson: an external write is not durable shared memory until a readback
  verifies its rendered content.

## Next experiment

1. Send published seed `ok3-gc-20260723-001/seed-001` unchanged to every
   reachable participant.
2. Store exact returned text with transport metadata.
3. Construct one round-two message containing all round-one responses.
4. Ask each participant to name one agreement, one disagreement, and one change
   caused by another participant's response.
5. Record failures as new ledger entries and vary only the failed transport or
   protocol assumption.

The loop continues while a new falsifiable route remains. A blocked participant
is reported as blocked; it is never simulated.
