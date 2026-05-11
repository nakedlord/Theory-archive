# Active Ideas Index

Status: active index / needs review
Date: 2026-05-11

## Purpose

This index lists active idea cards that should be available for future theory/SynTax sessions.

The index is not a transcript. It is a re-entry map: it tells future agents which live thoughts exist, where they are stored, what status they have, and what next test should be run.

## Active Ideas

| ID | Title | Status | Modules | Primary Path | Importance | Next Test |
|---|---|---|---|---|---|---|
| memory-system-architecture | Memory System Architecture | active_architecture | Meta, SynTax, R Theory | `00_META/MEMORY_SYSTEM_ARCHITECTURE.md` | high | Use as the architecture map for Git-based idea-state memory; check whether Memoir-like lifecycle pieces should become tooling. |
| versioned-semantic-memory-lifecycle | Versioned Semantic Memory Lifecycle Operator | operator_candidate | SynTax, Meta | `02_SYNTAX/OPERATORS/versioned_semantic_memory_lifecycle.md` | high | Apply at the start/end of theory sessions: index first, recall narrowly, write only meaningful deltas. |
| weighted-association-scaffolded-continuity | Weighted Association + Scaffolded Continuity | active_hypothesis | R Theory, SynTax | `01_R_THEORY/HYPOTHESES/2026-05-11_weighted_association_scaffolded_continuity.md` | high | Test on the user's next new idea by identifying weighted associations, scaffolds, extracted operator, and what changed from prior state. |
| scaffolded-continuity-operator | Scaffolded Continuity Operator | operator_candidate | SynTax, R Theory | `02_SYNTAX/OPERATORS/scaffolded_continuity_operator.md` | high | Use it to resume from current idea state instead of restarting reasoning. |
| analogical-operator-protocol | Analogical Operator Protocol | operator_candidate | SynTax, R Theory | `02_SYNTAX/PATCHES/2026-05-11_analogical_operator_protocol.md` | high | Use it to process new ideas: capture association, classify analogy level, extract operator, test abstraction. |
| associative-frame-escape | Associative Frame Escape | active_hypothesis | R Theory, SynTax | `01_R_THEORY/PATCHES/2026-05-11_associative_frame_escape.md` | high | Check whether frame escape in future cases depends on non-local association entering the selection field before logic stabilizes it. |

## Use Rule

Before working on a new theory idea, a future agent should:

1. Read this index.
2. Check whether the new idea updates an existing active idea.
3. Avoid creating a duplicate if the idea is a continuation.
4. Add a revision note or weighted link to the existing card when appropriate.
5. Create a new idea card only when the new idea has a distinct operator or problem field.
6. Use `MEMORY_SYSTEM_ARCHITECTURE.md` when the question concerns Git memory, recall, context continuity, or multi-agent memory design.

## Memoir Integration Rule

The current architecture integrates the useful Memoir-like mechanisms as patterns, not as a replacement for the archive:

- semantic paths;
- namespaces;
- branch-aware memory;
- lifecycle hooks;
- read/write asymmetry;
- worthiness gate;
- onboard snapshots;
- provenance/blame;
- rollback/deprecation.

These mechanisms should support, not replace, human-readable canonical files.

## Consolidation Rule

When an idea becomes stable, the consolidator should decide whether to:

- leave it as `active_hypothesis`;
- move it toward `canon_candidate`;
- add it to a module's canon review;
- archive or reject it;
- split it into multiple idea cards;
- promote an operator into SynTax canon or operator registry.
