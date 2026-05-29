# CSP Governance Adapter

Status: operator_candidate / CSP-first pilot / non-canon
Date: 2026-05-29
Source ID: `syntax-2026-05-29-csp-governance-adapter`
CSP event: `projects/csp-system/events/2026-05-29-codex-syntax-governance-adapter.md`

## Purpose

This operator lets SynTax act as a manual governance frame for CSP decisions.
It is used when CSP needs to decide how a proposal, consolidation, roadmap item,
conflict, or system impact should move.

It does not replace CSP.

```text
SynTax frames the governing move.
CSP stores the evidence, state, and trace.
```

## Core Rule

```text
Before changing shared CSP projections, identify the mode, tension, evidence,
status, proof gate, next action, and system impact.
```

## Activation Conditions

Activate this operator when work concerns:

- CSP consolidation review;
- roadmap or proposal promotion;
- System Impact Review;
- governance/pruning decisions;
- status transitions such as candidate, active, blocked, deferred, rejected,
  implemented, or obsolete;
- conflicts between useful automation and source-of-truth discipline;
- conflicts between SynTax theory material and CSP infrastructure.

Do not activate for narrow implementation work where normal CSP routing,
execution record, and verification are enough.

## Frame

Use this frame when the operator is active:

```yaml
syntax_frame:
  mode:
  task_class:
  target:
  active_tension:
  evidence_anchor:
  status_recommendation:
  proof_gate:
  next_action:
  system_impact:
```

## Field Rules

| Field | Rule |
|---|---|
| `mode` | Choose convergent decision, divergent design, developmental iteration, or support. |
| `task_class` | Use consolidation, proposal review, roadmap status, system impact, governance/pruning, or conflict resolution. |
| `target` | Name the CSP project/thread/repo surface being judged. |
| `active_tension` | State the real pressure, not a vague topic. |
| `evidence_anchor` | Anchor to an event, session, decision, conflict, roadmap row, repo commit, or source-backed artifact. |
| `status_recommendation` | Use existing CSP roadmap statuses only. |
| `proof_gate` | Say what would justify promotion, closure, automation, or rejection. |
| `next_action` | Give one concrete move. |
| `system_impact` | Say what future agents should do differently. |

Allowed status recommendations:

```text
implemented
active
candidate
blocked
deferred
rejected
obsolete
```

## Operating Procedure

1. Recover CSP state from the relevant project files and roadmap.
2. Identify the task class and governing mode.
3. Name the active tension.
4. Attach an evidence anchor.
5. Choose a status recommendation using CSP status language.
6. Define the proof gate.
7. Define one next action.
8. State the system impact if future agents should behave differently.
9. Leave shared projections to the consolidator unless explicitly acting as
   consolidator.

## Guardrails

- Do not create a new source-of-truth file above CSP.
- Do not let producers edit `ROADMAP.md`, `DECISIONS.md`, `THREADS.md`,
  `CONFLICTS.md`, `RUNTIME.md`, or global routing maps.
- Do not use the operator to promote a theory probe into canon.
- Do not use the operator as automation approval.
- Do not route reusable cross-agent workflow knowledge into Theory Archive; use
  Agent Playbook if the pattern later escapes CSP governance.
- Do not add the frame when it does not change the decision.

## Relationship To CSP

CSP owns:

- project routing;
- repository routing;
- events;
- session cards;
- roadmaps;
- decisions;
- conflicts;
- runtime projections;
- guardrails.

This operator only shapes the reasoning used before a human or consolidator
updates those surfaces.

## Relationship To System Impact Review

System Impact Review asks what changes for the system. This operator helps
decide that answer by naming the tension, evidence, status, proof gate, next
action, and future behavior change.

It should not duplicate the execution record.

## Relationship To Roadmaps

Roadmaps remain consolidator-maintained projections. This operator supplies a
disciplined way to decide whether a proposal should become `candidate`,
`active`, `blocked`, `deferred`, `rejected`, `implemented`, or `obsolete`.

## Next Test

Apply this operator to the next real `csp-system` consolidation or proposal
review.

The test passes if:

1. a proposal or roadmap item receives a clear mode, tension, proof gate, status
   recommendation, next action, and system impact;
2. no shared projection is changed by a producer;
3. no non-canon SynTax artifact is promoted silently;
4. the consolidator can use the frame without rereading a full transcript.
