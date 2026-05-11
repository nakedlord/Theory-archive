# Memory System Architecture

Status: active architecture / needs review
Date: 2026-05-11
Sources: SynTax/R Theory discussion + Memoir analysis

## Purpose

This file defines the integrated Git-based memory architecture for theory work.

It combines two layers:

1. Memoir-like infrastructure: versioned memory, semantic paths, namespaces, branch awareness, lifecycle hooks, worthiness gates, provenance, rollback.
2. SynTax/R Theory idea-state layer: weighted associations, scaffolds, analogy levels, operator extraction, failure modes, revision history, next tests.

## Core Principle

```text
Memory should not be a global variable or a transcript archive.
Memory should be a versioned, routed, status-aware scaffold for continuing thought.
```

## Roles of the Repositories

```text
Theory-archive              = durable theory and idea-state source of truth
context-state-protocol      = coordination, events, sessions, routing, runtime projection
Memoir-like local layer     = optional recall/cache/hook layer for agent sessions
ChatGPT/Codex session       = temporary reasoning runtime
```

The canonical durable content remains in readable Git files. A Memoir-like layer may be used as an acceleration / recall layer, but must not replace canonical files.

## Stolen / Integrated Mechanisms From Memoir

### 1. Versioned Memory

Every durable memory update should be traceable through Git commits or memory commits.

Required capability:

```text
who wrote this -> when -> why -> what changed -> how to revert
```

### 2. Semantic Paths

Memory items should live at meaningful paths rather than opaque IDs.

Examples:

```text
ideas.weighted_association_scaffolded_continuity
syntax.operators.scaffolded_continuity
r_theory.hypotheses.associative_frame_escape
projects.syntax.sessions.chatgpt_theory_continuation
```

In file storage, semantic paths map to human-readable file paths.

### 3. Namespaces

Different memory types must not be flattened into one space.

Recommended namespaces:

```text
theory:active_ideas
syntax:operators
r_theory:hypotheses
csp:sessions
csp:events
repo:onboard
project:onboard
metrics:turns
metrics:code
```

### 4. Branch / Context Awareness

Memory should respect branch or project state.

A branch-local experiment must not silently pollute canonical memory.

Required rule:

```text
if memory was produced on a side branch, mark it branch-local until consolidated into canonical main/master.
```

### 5. Lifecycle Hooks

Theory sessions should follow a lifecycle similar to Memoir's hooks:

```text
SessionStart       -> inject memory index / active idea hints
UserPromptSubmit   -> recall relevant active ideas before answering
Stop / TurnEnd     -> capture durable idea-state changes
SessionEnd         -> update session card / event if needed
```

In ChatGPT this is manual/protocol-driven. In Codex/Claude Code it may be automated.

### 6. Read / Write Asymmetry

Reads should be easy and frequent. Writes should be filtered.

```text
read automatically when relevant
write only through worthiness gate
consolidate shared projection files separately
```

### 7. Worthiness Gate

Do not save every interesting sentence.

Save only if at least one is true:

- a new operator appeared;
- an existing idea changed status;
- a weighted association changed the idea's gravity;
- a new scaffold was added;
- a failure mode was discovered;
- a next test changed;
- a canon candidate or rejection appeared;
- a routing/protocol decision changed future work.

### 8. Onboard Snapshots

Every durable project/theory module should have a compact re-entry snapshot:

```text
what this module is
what is active
what is not active
where to read next
what is stale
what should be tested next
```

For Theory-archive, `00_META/ACTIVE_IDEAS_INDEX.md` is the current re-entry map for active ideas.

### 9. Provenance / Blame

Every important memory should answer:

```text
source session / event
source repo path
commit hash
confidence/status
reason for saving
```

### 10. Rollback / Deprecation

Bad memory must be reversible without deleting the whole store.

Use statuses:

```text
rejected
archived
obsolete
deprecated
conflicted
```

Preserve why the rollback/deprecation happened.

## Integrated Memory Flow

### Session Start

1. Read CSP runtime/session card.
2. Read `00_META/ACTIVE_IDEAS_INDEX.md`.
3. Select only relevant idea cards.
4. Inject a compact re-entry state.

### During Reasoning

1. Identify whether the input updates an active idea.
2. Identify weighted associations.
3. Identify scaffolds.
4. Classify analogy levels.
5. Extract or update operators.
6. Check failure modes.
7. Identify next test.

### Turn End

1. Decide whether the change passes the worthiness gate.
2. Update or create an idea card.
3. Add a CSP event with repo/path/commit metadata.
4. Update session card if the working state changed.
5. Leave shared CSP projection files to consolidator.

## Difference From Flat Memory

Flat memory stores:

```text
we discussed X
```

Idea-state memory stores:

```text
X is active_hypothesis
it appeared because of Y
its strongest weighted links are A/B/C
its scaffolds are P/Q/R
its extracted operator is O
it fails when F
next test is T
```

## Relation to Memoir

Memoir is valuable as a storage/retrieval/runtime pattern:

- git-like memory;
- semantic paths;
- branch awareness;
- lifecycle hooks;
- worthiness gate;
- context injection;
- auto-capture;
- rollback/blame.

But this architecture adds a cognitive layer Memoir does not provide by default:

- idea status;
- weighted associations;
- scaffolded continuity;
- analogy-level classification;
- operator extraction;
- failure modes;
- next tests.

## Compact Rule

```text
Memoir-like infrastructure gives memory control.
SynTax idea-state schema gives memory meaning.
R Theory explains why weighted associations and scaffolds matter.
CSP records who changed what and what must happen next.
```
