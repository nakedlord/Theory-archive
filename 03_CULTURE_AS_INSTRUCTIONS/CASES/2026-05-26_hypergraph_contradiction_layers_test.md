# Case Test — Contradiction Layers in Pairwise Graph vs Hypergraph

Status: methodological case test / non-canon
Date: 2026-05-26
Source ID: `source-2026-05-18-higher-order-instruction-networks`
Related hypothesis: `03_CULTURE_AS_INSTRUCTIONS/HYPOTHESES/2026-05-18_hypergraph_formalization_probe.md`
Related source verification: `03_CULTURE_AS_INSTRUCTIONS/SOURCES/2026-05-19_weighted_hypergraph_distance_verification.md`
Base case: `03_CULTURE_AS_INSTRUCTIONS/CASES/contradictions_and_instruction_layers.md`
CSP event: `projects/syntax/events/2026-05-26-chatgpt-hypergraph-contradiction-layers-test.md`

## Purpose

This test checks whether the hypergraph formalization probe helps analyze textual contradictions as interactions between different instruction layers.

The base case warns that a textual inconsistency should not automatically be read only as an error or only as hidden meaning. It may point to different layers of transmission, editing, mythologization, or instruction.

The test question is:

```text
Can a typed temporal hypergraph separate historical, oral, editorial, theological, instructional, mythological, and institutional layers better than a pairwise graph?
```

## Base Layer Set

The base case lists these possible layers:

- historical trace;
- oral transmission;
- editorial assembly;
- theological interpretation;
- instructional function;
- mythological amplification;
- institutional stabilization.

Let:

```text
C = contradiction / textual inconsistency
```

## Pairwise Graph Representation

A pairwise graph can represent:

```text
C -- historical_trace
C -- oral_transmission
C -- editorial_assembly
C -- theological_interpretation
C -- instructional_function
C -- mythological_amplification
C -- institutional_stabilization
```

It can also add weighted links:

```text
w(C, historical_trace)
w(C, theological_interpretation)
w(C, institutional_stabilization)
```

### What Pairwise Graph Captures

The pairwise graph captures:

- the contradiction is related to several layers;
- some layers may be more relevant than others;
- a contradiction can be linked to an instruction, a mythic image, or an institution;
- layer involvement can be scored qualitatively or quantitatively.

### What Pairwise Graph Loses

The pairwise graph struggles to represent that a contradiction may be produced by the collision of whole layer-bundles, not by a single layer-to-contradiction link.

Example:

```text
C is not just linked to theology.
C appears where historical_trace + oral_transmission + editorial_assembly meet theological_interpretation + institutional_stabilization.
```

A pairwise graph can become a dense neighborhood around `C`, but it does not clearly encode which layer-combinations are doing the explanatory work.

## Typed Temporal Hypergraph Representation

A hypergraph can represent different transmission layer-bundles as different hyperedges.

Example:

```text
e1_trace = {C, historical_trace, oral_transmission, remembered_scene, early_instruction}
e2_editorial = {C, editorial_assembly, narrative_function, sequence_repair, reader_guidance}
e3_theological = {C, theological_interpretation, mythological_amplification, hero_image, symbolic_resolution}
e4_institutional = {C, institutional_stabilization, commentary_rule, acceptable_reading, tradition_boundary}
```

Each hyperedge can carry:

```text
time profile
carrier types
instruction bundle
textual layer
weight
reinterpretation effect
```

## Layer Collision

The contradiction is not simply a node with many edges. It can be a boundary object where multiple hyperedges overlap.

```text
C = overlap / collision point between e1_trace, e2_editorial, e3_theological, and e4_institutional
```

This allows the model to represent:

```text
historical residue survives in one bundle
narrative ordering reshapes it in another bundle
theological interpretation amplifies it in another bundle
institutional commentary stabilizes acceptable reading in another bundle
```

## Distinguishing Gain

The hypergraph model adds value in four cases.

### 1. One contradiction, multiple layer-bundles

The same contradiction can belong to different transmission regimes at once.

Pairwise graph says:

```text
C is related to historical_trace and theology.
```

Hypergraph says:

```text
C is preserved by e1_trace, reshaped by e2_editorial, intensified by e3_theological, and stabilized by e4_institutional.
```

This is a real distinguishing gain.

### 2. Contradiction as interface, not object

The contradiction can be modeled as an interface between bundles rather than as a simple defective element.

This matches the base case's warning that a contradiction is not automatically an error or hidden meaning.

### 3. Layer-specific rollback

Historical rollback should not delete every supernatural, inconvenient, or contradictory element.

Hypergraph representation can ask:

```text
which hyperedge would be removed by rollback?
which hyperedge would remain?
which instruction would be lost if the layer were stripped away?
```

This is more precise than removing pairwise links one at a time.

### 4. Competing instructions

The base case says contradiction may be the trace of competing instructions:

```text
historical memory
hero image amplification
institutional stability
moral rule
```

A hypergraph can model these as competing instruction bundles rather than a single contradictory message.

## Where Hypergraph Does Not Add Enough

The hypergraph model is unnecessary when:

- the inconsistency is a simple factual mismatch;
- there is no evidence for multiple transmission layers;
- the contradiction can be explained by one editorial decision;
- a layer table gives the same result more clearly;
- the analysis lacks textual or historical verification.

In those cases, a pairwise graph or ordinary layer table is cheaper and better.

## Result

```text
Probe passes the contradiction-layer representation test, but only for multi-layer contradictions.
```

The gain is specific:

```text
Hypergraph representation can model a contradiction as an overlap/collision between layer-bundles, while pairwise graph tends to collapse the case into a dense set of links around one contradiction node.
```

## Updated Constraint

Use the hypergraph model for contradiction analysis only when:

- one contradiction participates in multiple layer-bundles;
- each bundle transmits or stabilizes a different instruction;
- rollback would affect different bundles differently;
- textual evidence can identify at least two distinct layer-functions;
- pairwise graph or layer table loses the bundle-level explanation.

Do not use it for ordinary contradictions without evidence of layer-bundle interaction.

## Status

```text
methodological pass / non-canon / needs concrete textual case with source verification
```

## Next Test

The next useful test should stop using only internal conceptual cases and move to a concrete textual example.

Candidate target:

```text
03_CULTURE_AS_INSTRUCTIONS/CASES/mark_gospel_instruction_read.md
```

Test goal:

```text
Choose one episode or contradiction and check whether the hypergraph model separates textual/narrative/theological/institutional instruction bundles better than a pairwise graph or simple layer table.
```

If no concrete episode is selected or source-verified, stop escalating the formalization.
