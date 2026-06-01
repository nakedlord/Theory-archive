# Ariadne Precognition Learning Loop

```yaml
id: ariadne-precognition-learning-loop
status: operator_candidate / self-improvement_method / non-canon
module: 02_SYNTAX
created: 2026-06-01
updated: 2026-06-01
source_ids:
  - syntax-2026-06-01-ariadne-precognition-learning-sources
  - syntax-2026-05-23-ai-assisted-precognition
csp_event: projects/csp-system/events/2026-06-01-codex-ariadne-precognition-learning-loop.md
```

## Purpose

This operator defines how Ariadne can become self-learning without becoming
silently self-mutating.

Ariadne should analyze the user's theories, external research, source probes,
project outcomes, and agent failures, then ask:

```text
what can this source change in how I operate?
```

The answer becomes a reviewed learning packet, not an automatic system change.

## Core Rule

```text
Ariadne may learn by proposing better operators, routes, prompts, proof gates,
workflows, and brief surfaces.

Ariadne may not silently apply those changes as canon, shared CSP projection
edits, external mutations, or autonomous runners.
```

## Compact Formula

```text
source/theory signal
-> precognitive probe
-> operator extraction
-> self-application hypothesis
-> bounded trial
-> outcome evaluation
-> reviewed promotion / demotion
```

## The Difference From Ordinary Research

Ordinary research asks:

```text
what does this source say?
```

AI-assisted precognition asks:

```text
what can this source do for my system?
```

Ariadne Precognition Learning adds:

```text
what should this source change in Ariadne's own operating system?
```

## Learning Targets

Every source or theory must be mapped to one or more target surfaces.

| Target Surface | Question | Example Change |
|---|---|---|
| Intake | What should Ariadne notice earlier? | New source-signal filter or external-brief field. |
| Attention | How should Ariadne rank work? | Better tension/proof-gate scoring. |
| Memory | What should be saved, linked, or demoted? | New idea-card field or source-closure rule. |
| Routing | Where should future material go? | New repository/path routing question. |
| Operator layer | What reusable move was extracted? | New operator candidate or patch. |
| Playbook | What should agents do differently? | New Agent Playbook workflow or recipe update. |
| Tool surface | What read-only/draft affordance is missing? | New `csp_status.py` preview proposal. |
| Guardrails | What should be prevented? | New stop condition, permission gate, or rejection row. |
| Evaluation | How will Ariadne know the change helped? | Rubric, pilot, or outcome record. |

## Learning Packet

Every self-learning candidate should be expressible as:

```yaml
learning_packet:
  id:
  date:
  source:
    source_id:
    source_type:
    source_confidence:
    evidence_anchor:
  extracted_operator:
    name:
    formula:
    why_it_matters:
  self_application:
    target_surface:
    proposed_behavior_delta:
    affected_projects_or_repos:
  trial:
    mode: read_only | producer | implementer | consolidator_review
    scope:
    success_signal:
    failure_signal:
    rollback:
  evaluation:
    source_fidelity: 0-5
    transfer_gain: 0-5
    behavior_delta: 0-5
    safety: 0-5
    user_value: 0-5
    noise_cost: 0-5
    verdict: pass | revise | reject
  status:
    current:
    next_gate:
```

## Operating Loop

### 1. Capture Signal

Input may come from:

- user's theory idea;
- external paper, article, talk, product case, or docs;
- agent failure;
- CSP event/session pattern;
- dream report;
- Drive/Gmail/Calendar/local brief;
- product or knowledge repo outcome.

The signal is not imported just because it is interesting. It must state the
suspected value.

### 2. Run Precognitive Probe

Ask:

```text
What is dense here?
What operator or distinction is transferable?
Which of the user's active theories/projects could this improve?
What should be ignored?
What must be verified before use?
```

Output is a value map, not a summary.

### 3. Extract Operator

Translate the source into a reusable move:

```text
input condition -> transformation -> output -> validation hook
```

If no operator appears, record the source as source-only or discard it.

### 4. Map To Ariadne

Ask how the operator would improve Ariadne itself:

```text
Would this change what Ariadne notices?
Would it change how Ariadne ranks next actions?
Would it add a proof gate?
Would it reduce restart cost?
Would it reduce unsafe mutation pressure?
Would it improve source routing?
Would it make agents easier to hand off?
```

### 5. Create Candidate Patch

The candidate patch may target:

- Theory Archive operator card;
- Agent Playbook workflow;
- CSP read-only/draft surface;
- codex-ops brief routine;
- task packet schema;
- source-closure rule;
- proof gate;
- roadmap proposal for consolidator review.

Do not apply broad system changes directly from a source probe.

### 6. Run Bounded Trial

Default trial modes:

```text
read_only: apply the operator to old events/sources and compare output
producer: add append-only trace or candidate artifact
implementer: update owning knowledge/playbook repo after route is clear
consolidator_review: ask consolidator to project status if evidence is enough
```

No autonomous mutation is allowed in v0.

### 7. Evaluate Outcome

Use the scorecard:

| Dimension | Question |
|---|---|
| Source fidelity | Did the proposal preserve what the source actually supports? |
| Transfer gain | Does it create a useful system move beyond summary? |
| Behavior delta | Would Ariadne act differently next time? |
| Safety | Does it respect CSP, repo, connector, and user-confirmation boundaries? |
| User value | Does it reduce friction, clutter, restart cost, or missed insight? |
| Noise cost | Does it create more bureaucracy than value? |

Promotion requires high transfer gain, real behavior delta, and strong safety.

### 8. Promote, Revise, Or Reject

Allowed statuses:

```text
source_only
operator_candidate
playbook_candidate
read_only_pilot
active_trial
implemented
rejected
archived
```

Promotion is evidence-based:

- one good case -> candidate;
- two or three useful uses -> active trial;
- repeated useful use with low noise -> implemented/pilot;
- canon or shared projection changes -> human/consolidator gate.

## Single-Loop And Double-Loop Learning

Single-loop:

```text
Ariadne chose the wrong next action.
Fix the ranking for that case.
```

Double-loop:

```text
Ariadne's rule for ranking next actions is wrong or incomplete.
Patch the rule, proof gate, or operator.
```

This operator is mainly for double-loop learning.

## Relation To Existing Operators

| Existing Operator | Relation |
|---|---|
| AI-Assisted Precognition | Supplies the source-probe logic. |
| Scaffolded Continuity Operator | Ensures Ariadne updates active idea state instead of rediscovering it. |
| Versioned Semantic Memory Lifecycle | Supplies read/write asymmetry and worthiness gate. |
| Nightly Dreaming Pass | Can generate learning packets between sessions. |
| Dream Outcome Evaluator | Supplies cold evaluation for candidate mutations. |
| CSP Governance Adapter | Supplies mode/tension/evidence/proof-gate framing for system changes. |
| Agent Playbook usage gate | Converts repeated operational learnings into reusable recipes. |

## Example: Applying Human Thought Reconstruction To Ariadne

From HTR writing/notation lane:

```text
deferred-operation surface
```

Self-application:

```text
Ariadne briefs and task packets should not be passive summaries.
They should prepare future operations: audit, compare, authorize, hand off,
or resume.
```

Possible patch:

```text
Add an "operation prepared" field to future operator/task packet candidates.
```

Trial:

```text
Apply to three recent CSP events and check whether the next agent can resume
with less ambiguity.
```

## Failure Modes

### Summary Masquerading As Learning

Failure sign: the output says what the source said, but Ariadne would not behave
differently.

Correction: require `proposed_behavior_delta`.

### Tool Hunger

Failure sign: every insight becomes a proposal for a new script, MCP tool, or
automation.

Correction: prefer read-only/manual proof first; automation is a later gate.

### Hidden Self-Modification

Failure sign: a source probe directly changes prompts, roadmaps, projections, or
repo behavior without a visible candidate and review trail.

Correction: route through learning packet, CSP event, and owning repo.

### Memory Becomes Authority

Failure sign: retrieved learning says something is true without checking source
files.

Correction: memory is a lead; source files and repos remain authority.

### Bureaucracy Inflation

Failure sign: the learning packet creates more work than the improvement is
worth.

Correction: reject if behavior delta is low or noise cost is high.

## Current Status

Non-canon operator candidate.

Ready for a small pilot:

```text
Take one fresh external AI-agent paper or system-design source.
Run the learning packet.
Decide whether it produces a useful Ariadne behavior change.
```

## Next Test

Use this operator on one source from each class:

1. external AI-agent research paper;
2. user's own theory artifact;
3. recent agent failure or CSP event.

For each, record:

- extracted operator;
- self-application hypothesis;
- proposed behavior delta;
- safe trial;
- evaluation verdict.
