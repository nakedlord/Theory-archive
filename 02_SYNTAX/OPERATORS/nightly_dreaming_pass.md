# Nightly Dreaming Pass

Status: operator_candidate / active trial
Date: 2026-05-11
Source: ChatGPT + CSP automation design
Related: `00_META/MEMORY_SYSTEM_ARCHITECTURE.md`, `00_META/ACTIVE_IDEAS_INDEX.md`, `02_SYNTAX/OPERATORS/versioned_semantic_memory_lifecycle.md`, CSP `projects/codex-ops/`

## Purpose

Nightly Dreaming Pass is a scheduled offline reflection operator for SynTax/CSP.

Its function is not to make the system autonomous in the strong sense. Its function is to let the system review accumulated state between sessions, detect tensions, propose idea mutations, score candidate patches, and hand useful work to the human or Codex/consolidator.

The pass must produce value without silently rewriting canon.

## Core Rule

```text
Dreaming may observe, score, propose, and write append-only reports.
Dreaming may not canonize, delete, merge, or rewrite memory directly.
```

## Position in Architecture

```text
CSP / codex-ops              = automation coordination and dream reports
Theory-archive              = durable theory and idea-state source of truth
SynTax memory architecture  = active ideas, operators, hypotheses, next tests
Codex/consolidator          = applies reviewed changes
Human                       = approves high-impact direction changes
```

## Input Set

The pass should read:

- `context-state-protocol/AGENTS.md`
- `context/GLOBAL_INDEX.md`
- `context/REPOSITORY_REGISTRY.md`
- `context/KNOWLEDGE_ROUTING.md`
- `context/REPOSITORY_REQUESTS.md`
- `projects/codex-ops/*`
- `projects/syntax/RUNTIME.md`
- relevant active session cards
- `Theory-archive/00_META/ACTIVE_IDEAS_INDEX.md`
- `Theory-archive/00_META/MEMORY_SYSTEM_ARCHITECTURE.md`
- only relevant idea cards/operators selected by the active index and runtime state

The pass should not read the entire archive blindly unless explicitly running a deep audit.

## Dreaming Procedure

### 1. Ingest

Collect recent events, active sessions, active ideas, conflicts, next actions, and open consolidation markers.

### 2. Detect

Find:

- stale next actions;
- duplicate idea candidates;
- missing idea cards;
- missing CSP events for theory changes;
- unresolved `needs_consolidation`;
- branch/locality risks;
- delivery gaps;
- weak or noisy ideas;
- ideas whose next test has changed;
- candidates for operator extraction.

### 3. Mutate

Propose, but do not apply:

- idea-card revision;
- weighted association update;
- scaffold addition;
- failure-mode addition;
- next-test replacement;
- split/merge/archive candidate;
- new operator candidate;
- cross-link candidate.

### 4. Score

Each candidate receives a confidence score.

Recommended factors:

```text
confidence =
  recurrence
+ cross_link_strength
+ active_idea_match
+ novelty_delta
+ testability
+ source_quality
- conflict_risk
- noise_risk
```

Do not inflate confidence above `0.85` unless the same signal appears in at least two independent sources/files.

### 5. Gate

Preserve only candidates that change at least one future behavior:

- future recall;
- future reasoning path;
- theory status;
- consolidation priority;
- project routing;
- open conflict;
- next test;
- operator registry candidate.

Reject decorative insights.

### 6. Output

Every run should return a visible report with:

- Findings;
- Dream Packet;
- Idea mutations;
- Patch candidates;
- Kill / merge / archive proposals;
- Next concrete action.

When write access is available, every run may also write append-only artifacts under CSP:

```text
projects/codex-ops/dreams/YYYY-MM-DD-nightly-dream.md
projects/codex-ops/events/YYYY-MM-DD-nightly-dreaming-pass.md
```

## Output Categories

Use explicit classes:

```text
observe          = useful signal, no action yet
suggest          = possible improvement, low risk
candidate_patch  = structured patch proposal requiring review
needs_human      = user decision needed
needs_codex      = implementation/consolidation needed
reject/noise     = intentionally discarded signal
```

## Forbidden Actions

The pass must not:

- edit module canon files;
- edit shared CSP projection files;
- delete idea cards;
- merge idea cards;
- mark a hypothesis as canon;
- rewrite `ACTIVE_IDEAS_INDEX.md` directly;
- close conflicts directly;
- update `RUNTIME.md` directly;
- hide its result in memory without visible delivery.

## Relation to Versioned Semantic Memory Lifecycle

Versioned Semantic Memory Lifecycle governs normal session memory:

```text
Index first.
Recall narrowly.
Reason with idea-state.
Write only meaningful deltas.
Version everything.
Consolidate separately.
```

Nightly Dreaming Pass applies the same discipline between sessions, at system level.

## Relation to Memory System Architecture

Memory System Architecture defines the durable idea-state model.

Nightly Dreaming Pass is a scheduled operator that checks whether the current memory state remains useful, routed, testable, and non-noisy.

## Minimal Useful Result

A successful run does not need many insights.

A successful run can be one of:

- one stale next action identified;
- one high-confidence candidate patch;
- one idea-card mutation proposal;
- one noise/rejection signal;
- one human/Codex handoff;
- confirmation that no durable change passed the worthiness gate.

## Trial Criteria

After several runs, evaluate:

- Did it surface useful work?
- Did it reduce restart cost?
- Did it catch stale state?
- Did it propose non-obvious but valid idea mutations?
- Did it produce noise?
- Did it respect producer/consolidator boundaries?
- Did the report reach the user visibly?

## Compact Formula

```text
Sleep over the graph.
Find tension.
Mutate candidates.
Score risk.
Preserve only deltas.
Wake the human with usable work.
```
