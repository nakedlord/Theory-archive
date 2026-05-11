# Dream Output Store

Status: operator_candidate / active trial
Date: 2026-05-11
Related: `02_SYNTAX/OPERATORS/nightly_dreaming_pass.md`, `02_SYNTAX/OPERATORS/theory_mutation_dreaming_layer.md`, `02_SYNTAX/OPERATORS/dream_outcome_evaluator.md`, `00_META/MEMORY_SYSTEM_ARCHITECTURE.md`

## Purpose

Dream Output Store is the intermediate storage layer for SynTax dreaming.

It separates generated dream mutations from accepted memory. A dreaming pass may create bold candidate theory states, but those candidates remain outside canon, outside active idea cards, and outside shared CSP projection files until reviewed.

## Core Rule

```text
Input memory is read-only.
Dream output is a separate candidate store.
Accepted memory changes require explicit consolidation.
```

This makes the dreaming process safer and more useful: the system can mutate ideas without silently corrupting the source of truth.

## Position in the Pipeline

```text
Active memory / idea cards
  -> Nightly Dreaming Pass
  -> Dream Output Store
  -> Dream Outcome Evaluator
  -> Visible delivery
  -> Human / Codex consolidation
  -> Accepted patches or rejected candidates
```

## Storage Location

For CSP-coordinated runs:

```text
context-state-protocol/
  projects/codex-ops/dreams/YYYY-MM-DD-nightly-dream.md
```

For theory-local future variants:

```text
Theory-archive/00_META/DREAM_OUTPUTS/YYYY-MM-DD.md
```

Current default is CSP `projects/codex-ops/dreams/`, because dreaming is an automation process and must be auditable as an operational event.

## Dream Output Packet

Each dream output should use this structure:

```yaml
dream_id: YYYY-MM-DD-nightly-dream
mode: scheduled | manual
source: chatgpt | codex | other
status: proposed
input_scope:
  csp_files: []
  theory_files: []
  selected_ideas: []
  excluded_scopes: []
mutation_phase:
  selected_ideas: []
  theory_mutations: []
evaluation_phase:
  evaluator: dream_outcome_evaluator
  rubric_scores: []
  pass_status: pass | needs_revision | reject
structural_phase:
  findings: []
delivery:
  visible_response_required: true
  delivery_channels: []
apply_status: not_applied
needs_consolidation: true
```

## Theory Mutation Record

Each theory mutation should contain:

```yaml
idea_id: string
current_formulation: string
proposed_formulation: string
pressure_point: string
strengthening_move: string
falsifier_or_failure_mode: string
cross_link:
  target: string
  reason: string
operator_extraction: string | null
next_test: string
status_pressure: keep | narrow | split | merge | watch | demote | canon_candidate
confidence: 0.0-1.0
risk: low | medium | high
```

## Evaluation Record

Each mutation receives an independent evaluation:

```yaml
mutation_id: string
scores:
  theory_delta: 0-5
  pressure_clarity: 0-5
  falsifiability: 0-5
  operator_quality: 0-5
  cross_link_value: 0-5
  next_test_quality: 0-5
  canon_safety: 0-5
pass_status: pass | needs_revision | reject
revision_note: string
```

## Apply Rules

Dream Output Store never applies changes directly.

Allowed outcomes:

```text
pass             -> candidate patch may be created
needs_revision   -> keep in dream output, no patch yet
reject           -> preserve as rejected dream output, do not delete immediately
```

## Required Separation

A dream output must distinguish:

```text
mutation proposed by the dreamer
assessment by the grader
decision by human/Codex consolidator
actual accepted memory change
```

These are separate stages. Collapsing them into one stage reintroduces silent canon mutation.

## Minimum Useful Dream Store

A useful dream store may contain only one strong mutation.

A run with no valid theory mutation should say so explicitly and record why:

```text
No theory mutation passed the worthiness gate.
Reason: selected idea had no new pressure point, no stronger formulation, and no testable delta.
```

## Forbidden Content

Dream Output Store must not contain:

- rewritten canon as if already accepted;
- direct replacement text for active idea cards without `proposed_` markers;
- hidden decisions;
- unscored mutations;
- vague insights without next test;
- structural audit only, unless no theory mutation exists.

## Compact Formula

```text
Dream boldly.
Store separately.
Grade coldly.
Apply never without consolidation.
```
