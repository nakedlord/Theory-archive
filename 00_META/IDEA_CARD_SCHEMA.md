# Idea Card Schema

Status: active schema / needs review
Date: 2026-05-11

## Purpose

This schema turns Git memory from a transcript archive into a live idea-state system.

The goal is not only to remember what was said, but to preserve where a thought currently stands, why it matters, what associations support it, what scaffolds it depends on, what operator was extracted, and what should be tested next.

## Core Principle

```text
A useful memory stores the state of a thought, not only the text of a thought.
```

## Minimal Idea Card Fields

```yaml
id: short-stable-id
title: Human-readable title
status: raw_association | working_analogy | operator_candidate | active_hypothesis | canon_candidate | canon | rejected | archived
modules: [01_R_THEORY, 02_SYNTAX, ...]
created: YYYY-MM-DD
updated: YYYY-MM-DD
source: chatgpt | codex | human | other
importance: low | medium | high
needs_consolidation: true | false
```

## Required Sections

### Current Formulation

The compact current version of the idea. This should be enough for another session to resume without reading the whole transcript.

### Why It Appeared

What problem, mismatch, association, analogy, or user question generated the idea.

### Weighted Associations

Links that currently give the idea its weight.

Use this table:

| Link | Weight | Charge | Why |
|---|---|---|---|
| association target | low/medium/high | pleasure/pain/importance/repeated_success/unresolved_tension/explanatory_gain | why this link matters |

### Scaffolds

External supports that let the idea continue across sessions:

- files;
- patches;
- sessions;
- indexes;
- examples;
- related theories;
- open questions.

### Analogies

Analogies supporting or testing the idea. Each analogy should include its level:

- external;
- functional;
- role;
- structural;
- dynamic;
- operator;
- failure.

### Extracted Operator

The transferable mechanism extracted from the associations and analogies.

### What This Solves

Problems or limitations the idea helps solve.

### Failure Modes

Where the idea breaks, overreaches, or becomes misleading.

### Revision History

Short notes on how the idea changed across sessions.

### Next Test

The next concrete situation, question, or case where the idea should be tested.

## Status Meanings

| Status | Meaning |
|---|---|
| raw_association | Interesting activation, not yet mapped. |
| working_analogy | Mapped analogy, not yet extracted into an operator. |
| operator_candidate | Transferable mechanism has been extracted but not tested enough. |
| active_hypothesis | Strong enough to use and test, not canon. |
| canon_candidate | Ready for formal review against existing canon. |
| canon | Accepted stable theory component. |
| rejected | Tested and found misleading or wrong. |
| archived | Preserved historically but not active. |

## Memory Rule

When a new idea appears, do not store only a summary. Store:

```text
why it appeared -> what links give it weight -> what scaffold preserves it -> what operator it produced -> what test comes next
```

## Relation to SynTax and R Theory

- SynTax uses this schema as a memory/continuity operator.
- R Theory uses it as evidence for how weighted associations and external scaffolds support frame escape and recursive development of thought.
