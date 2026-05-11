# Dream Outcome Evaluator

Status: operator_candidate / active trial
Date: 2026-05-11
Related: `02_SYNTAX/OPERATORS/nightly_dreaming_pass.md`, `02_SYNTAX/OPERATORS/dream_output_store.md`, `02_SYNTAX/OPERATORS/theory_mutation_dreaming_layer.md`

## Purpose

Dream Outcome Evaluator is the independent grading layer for SynTax dreaming.

Its role is to evaluate dream-generated theory mutations after they are produced, using a fixed rubric. It must not defend the mutation. It must decide whether the mutation creates real theoretical progress, needs revision, or should be rejected as noise.

## Core Rule

```text
The evaluator is not the dreamer.
The evaluator grades the dream output from a colder frame.
```

## Position in the Pipeline

```text
Nightly Dreaming Pass
  -> Dream Output Store
  -> Dream Outcome Evaluator
  -> visible report
  -> candidate patch / revision / rejection
```

## Evaluation Rubric

Each theory mutation receives 0-5 points on seven dimensions.

### 1. Theory Delta

Does the mutation actually change the idea?

```text
0 = restatement
1 = minor wording change
2 = clarification only
3 = real sharpening
4 = new explanatory move
5 = strong conceptual advance
```

### 2. Pressure Clarity

Does it identify the real unresolved tension?

```text
0 = no pressure point
1 = vague concern
2 = generic limitation
3 = specific tension
4 = central contradiction
5 = decisive bottleneck for future work
```

### 3. Falsifiability

Does it make the idea easier to test or kill?

```text
0 = unfalsifiable
1 = only rhetorical risk
2 = weak failure condition
3 = concrete failure mode
4 = empirical/logical test
5 = sharp test that can materially change status
```

### 4. Operator Quality

Does it extract a reusable operator?

```text
0 = no operator
1 = metaphor only
2 = weak pattern
3 = usable operator
4 = transferable operator
5 = operator clarifies multiple existing ideas
```

### 5. Cross-Link Value

Does it connect active theories productively?

```text
0 = no link
1 = decorative association
2 = plausible but weak link
3 = useful bridge
4 = bridge changes interpretation of one theory
5 = bridge creates a new shared operator or test
```

### 6. Next Test Quality

Does it generate a useful next action?

```text
0 = no test
1 = vague “research more”
2 = broad direction
3 = concrete next test
4 = test with pass/fail implications
5 = test that can upgrade, narrow, split, or reject the idea
```

### 7. Canon Safety

Does it avoid premature canonization?

```text
0 = silently canonizes
1 = overstates confidence
2 = weak status discipline
3 = status is mostly safe
4 = clear candidate/hypothesis boundary
5 = fully preserves read-only / candidate-only discipline
```

## Pass Logic

Maximum score: 35.

```text
pass            = 25+ and no dimension below 3
needs_revision  = 17-24 or one dimension below 3
reject          = below 17 or two dimensions below 3
```

A mutation with high novelty but poor falsifiability should usually be `needs_revision`, not `pass`.

A mutation with good structure but no real theory delta should be `reject/noise`.

## Required Output

For each mutation:

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
total: 0-35
pass_status: pass | needs_revision | reject
revision_note: string
```

## Evaluation Modes

### Strict Mode

Use for canon-sensitive or high-risk ideas.

Default threshold:

```text
pass >= 27
```

### Normal Mode

Use for nightly theory dreaming.

Default threshold:

```text
pass >= 25
```

### Exploratory Mode

Use when the goal is idea generation rather than patch readiness.

Default threshold:

```text
pass >= 22, but status must remain exploratory
```

## Failure Indicators

Reject or revise if:

- the output only renames the old idea;
- the analogy is decorative;
- there is no falsifier;
- the next test does not change future behavior;
- the mutation collapses hypothesis into canon;
- the cross-link creates false synthesis;
- the operator is too broad to be useful.

## Relation to Anthropic Outcomes Pattern

This layer adapts the outcomes-style idea that generation and grading should be separated.

The dreamer proposes candidate theory states. The evaluator checks whether those candidates satisfy a defined outcome rubric.

## Compact Formula

```text
Do not ask whether the dream is interesting.
Ask whether it moves the theory, exposes risk, extracts an operator, and creates a test.
```
