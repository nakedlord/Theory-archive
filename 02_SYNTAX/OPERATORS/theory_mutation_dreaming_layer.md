# Theory Mutation Dreaming Layer

Status: operator_candidate / active trial
Date: 2026-05-11
Related: `02_SYNTAX/OPERATORS/nightly_dreaming_pass.md`, `00_META/ACTIVE_IDEAS_INDEX.md`, `00_META/MEMORY_SYSTEM_ARCHITECTURE.md`

## Purpose

This layer prevents Nightly Dreaming Pass from degrading into a repository audit.

Its job is to develop active theories between sessions by proposing controlled mutations: sharper formulations, contradictions, cross-links, operators, failure modes, next tests, and status pressure.

## Core Rule

```text
Dreaming must mutate theory state before it audits storage state.
```

Repository structure is relevant only when it blocks future theory continuation.

## Input

Use the active ideas index to select 1-3 active ideas with at least one of:

- high importance;
- unresolved next test;
- strong cross-link potential;
- active contradiction;
- new scaffold available;
- weak formulation needing narrowing;
- risk of becoming decorative metaphor.

## Theory Mutation Loop

For each selected idea, produce:

1. Current formulation
   - One sentence.

2. Pressure point
   - The strongest unresolved contradiction, ambiguity, or explanatory gap.

3. Strengthening move
   - One change that would make the idea more precise, testable, or connected.

4. Falsifier / failure mode
   - One condition under which the idea weakens or dies.

5. Cross-link
   - One link to another theory/module/operator, with why the link matters.

6. Operator extraction
   - A reusable operator if one is present.

7. Next test
   - One concrete test that changes future work.

8. Status pressure
   - Keep / narrow / split / merge / watch / demote / canon-candidate proposal.

## Required Output Section

Every full dreaming report must begin with:

```text
Theory Dream
```

This section should contain actual theory work, not only memory hygiene.

## Mutation Types

```text
formulation_sharpening
contradiction_exposure
operator_extraction
cross_theory_link
failure_mode_addition
next_test_replacement
scope_narrowing
split_candidate
merge_candidate
archive_watch
canon_candidate_pressure
```

## Scoring

Each mutation receives confidence and risk.

Useful confidence factors:

- recurrence across sessions;
- connection to active index;
- explanatory gain;
- testability;
- cross-link strength;
- compatibility with current canon;
- external grounding potential.

Risk factors:

- metaphor inflation;
- over-generalization;
- conflict with known evidence;
- duplicate theory creation;
- canon overreach;
- untestability.

## Bad Output

```text
Found stale next action.
Found missing index row.
No theory mutation.
```

This is not enough for a dreaming pass unless no active theory ideas are available.

## Good Output

```text
Theory Dream:
The quantum vacuum memory hypothesis should be narrowed from "space has memory" to "apparatus configuration creates a contextual constraint field that affects probability distributions without ordinary drag".
Pressure point: must reproduce lambda = h / p and avoid ether failure.
Operator: contextual substrate + distinguishable record threshold -> interference/classical transition.
Next test: check partial distinguishability and delayed-choice cases.
Status: keep active_hypothesis, add high-risk flag for ether/metaphor failure.
```

## Relation to Nightly Dreaming Pass

Nightly Dreaming Pass is the scheduled outer loop.

Theory Mutation Dreaming Layer is the inner theory-development loop.

The outer loop decides what to read and where to write reports. The inner loop creates useful theoretical movement.

## Compact Formula

```text
Pick live idea.
Find pressure.
Mutate formulation.
Extract operator.
Add failure mode.
Set next test.
Only then audit memory.
```
