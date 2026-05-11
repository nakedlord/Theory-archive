# Versioned Semantic Memory Lifecycle Operator

Status: active operator candidate / needs consolidation
Date: 2026-05-11
Source: Memoir analysis integrated into SynTax memory architecture

## Purpose

This operator adds a Memoir-like lifecycle to SynTax memory work.

It defines when an agent should read memory, when it should write memory, how memory should be routed, and how to avoid flat transcript storage, context contamination, token rent, and memory drift.

## Core Rule

```text
Read memory by semantic relevance before answering.
Write memory only when the thought state changes.
Preserve memory as versioned idea state, not as a global blob.
```

## Lifecycle

### 1. SessionStart

At the start of a theory/SynTax session:

1. Read CSP runtime and session card.
2. Read `Theory-archive/00_META/ACTIVE_IDEAS_INDEX.md`.
3. Identify relevant active idea cards.
4. Inject a compact re-entry state, not the whole archive.

### 2. UserPromptSubmit

Before answering a meaningful prompt:

1. Ask: does this update an active idea?
2. If yes, read the relevant idea card.
3. If no, proceed normally.
4. If uncertain, use semantic paths / active index to narrow the search.

### 3. Reasoning

Process the idea with:

- weighted associations;
- scaffolds;
- analogy levels;
- operator extraction;
- failure modes;
- next test.

### 4. TurnEnd / Stop

After a meaningful turn:

1. Apply the worthiness gate.
2. Update existing idea card or create a new one.
3. Add a CSP event with repo, branch, path, and commit hash.
4. Update only the current session card if needed.
5. Leave shared projection/canon files to the consolidator.

## Worthiness Gate

Save memory only when at least one is true:

- new operator;
- changed status;
- new weighted association;
- new scaffold;
- new failure mode;
- new next test;
- changed routing;
- changed canon candidate state;
- a prior idea is rejected, archived, or split.

Do not save:

- decorative metaphors;
- repeated explanations;
- unchanged restatements;
- local phrasing improvements;
- one-off answers with no durable consequence.

## Semantic Path Rule

Every saved memory should have a semantic path.

Recommended pattern:

```text
<domain>.<type>.<stable_id>
```

Examples:

```text
syntax.operator.scaffolded_continuity
syntax.operator.analogical_operator_protocol
r_theory.hypothesis.weighted_association_scaffolded_continuity
theory.meta.active_ideas_index
```

The path should be stable enough for future recall.

## Namespace Rule

Do not mix memory types.

Use conceptual namespaces:

```text
ideas
operators
hypotheses
canon_candidates
sessions
events
onboard_snapshots
metrics
```

## Branch Awareness

When a memory is produced under non-canonical branch or uncertain context, mark it:

```text
branch_local: true
needs_consolidation: true
```

Do not let branch-local memory become canonical silently.

## Provenance Rule

Every durable memory should record:

- source conversation/session;
- source event;
- repository path;
- commit hash;
- status;
- reason saved;
- next test or consolidation step.

## Rollback Rule

Bad memory should be demoted, not erased by default.

Use:

```text
rejected
archived
obsolete
deprecated
conflicted
```

Record why the demotion happened.

## Relation to Existing SynTax Operators

This operator wraps and supports:

- Analogical Operator Protocol;
- Scaffolded Continuity Operator;
- Goal Module;
- Memory Governance Layer;
- Context Arbitration;
- Validation / Error Architecture.

It governs memory lifecycle. It does not replace reasoning operators.

## Compact Formula

```text
Index first.
Recall narrowly.
Reason with idea-state.
Write only meaningful deltas.
Version everything.
Consolidate separately.
```
