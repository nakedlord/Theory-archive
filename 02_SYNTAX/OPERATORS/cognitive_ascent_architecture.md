# Cognitive Ascent Architecture

Status: operator candidate / source-backed by chat export / not canon
Date: 2026-05-28
CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-syntax-export-batch-2.md`
Source IDs:

- `syntax-2026-05-28-boltalka-3-0-ideas-export`
- `syntax-2026-05-28-ai-memory-structure-export`

## Purpose

Cognitive Ascent Architecture (CAA) describes a SynTax operator where the model
does not merely mirror the user's current reasoning. It infers the user's
direction of thought, then develops that direction one stable step further.

The core formulation from the source batch is Variant B:

```text
Predict the direction of the user's thinking, not the exact next thought.
Then develop it further, deeper, and wider while staying directionally aligned.
```

## Distinction

CAA is not:

- cloning the user's writing style;
- pretending to know the user's hidden intent;
- replacing the user's judgment;
- uncontrolled autonomous speculation.

CAA is:

- vector inference over the user's current thought direction;
- stable expansion beyond the immediately stated step;
- surfacing the hidden structure, contradiction, or next abstraction;
- preserving alignment to the user's originating problem.

## Inputs

CAA reads:

- the user's current question or idea;
- the active idea state if available;
- domain context and source provenance;
- known failure modes and open gaps;
- the requested output depth.

## Procedure

```text
1. Identify the thought vector.
2. Identify the hidden constraint or contradiction.
3. Identify the likely next abstraction level.
4. Build one stable extension, not a sprawling tree.
5. Check whether the extension remains grounded in the prompt/source.
6. Mark speculation explicitly.
```

## Guardrails

- Grounded abstraction rule: every higher-level move must trace back to the
  prompt, source, or active idea state.
- Directional alignment: autonomous expansion is allowed only inside the
  user's current vector of inquiry.
- Progress delta: the output should change understanding, not only sound deep.
- Exploration budget: stop before the extension becomes unbounded.

## Failure Modes

- hallucinating a direction the user did not imply;
- overproducing meta-analysis;
- turning every answer into theory;
- hiding uncertainty;
- replacing source-backed work with elegant speculation.

## Relation To Existing Operators

CAA depends on:

- `scaffolded_continuity_operator.md`
- `versioned_semantic_memory_lifecycle.md`
- `PATCHES/v3.0_progress_delta_check.md`
- `PATCHES/v3.5_exploration_budget.md`
- `PATCHES/v4.6_complexity_governance_rule.md`

## Next Test

Compare CAA against a non-CAA response on the user's next new theory idea:

```text
baseline: answer only the stated question
CAA: infer vector -> extend one stable level -> mark what is new
```

Pass condition: the CAA answer adds a useful next structure without drifting,
overexplaining, or inventing unsupported claims.

