# Case Test — Mark 16:8 and Longer Ending as Hypergraph Stress-Test

Status: concrete textual stress-test / non-canon
Date: 2026-05-26
Source ID: `culture-2026-05-26-mark-ending-hypergraph-test`
Related source note: `03_CULTURE_AS_INSTRUCTIONS/SOURCES/2026-05-26_mark_ending_textual_source_note.md`
Related hypothesis: `03_CULTURE_AS_INSTRUCTIONS/HYPOTHESES/2026-05-18_hypergraph_formalization_probe.md`
Base case: `03_CULTURE_AS_INSTRUCTIONS/CASES/mark_gospel_instruction_read.md`
CSP event: `projects/syntax/events/2026-05-26-chatgpt-mark-ending-hypergraph-test.md`

## Purpose

This test moves the hypergraph formalization probe from internal methodological cases to one concrete textual stress-test:

```text
Mark 16:8 and the longer ending tradition, Mark 16:9-20
```

The question is not whether the longer ending is historically or theologically true.

The question is:

```text
Does a typed temporal hypergraph explain the transmission functions around Mark's ending better than a pairwise graph or simple layer table?
```

## Minimal Textual Premise

The case uses only a cautious premise:

```text
Mark 16:8 is an abrupt ending / ending problem in the textual tradition.
Mark 16:9-20 represents a longer ending tradition that supplies closure and appears in many later manuscript traditions.
```

The test does not require deciding whether the original Mark ended at 16:8, whether an ending was lost, or whether the longer ending is liturgical/canonical reception.

## Pairwise Graph Representation

A pairwise graph represents the ending problem as links around one node:

```text
C = Mark_ending_problem

C -- textual_witness
C -- abrupt_ending
C -- fear_and_silence
C -- resurrection_proclamation
C -- appearance_tradition
C -- canonical_stabilization
C -- institutional_use
C -- reader_closure_pressure
```

### What Pairwise Graph Captures

The pairwise graph can show that the ending problem is connected to:

- textual witnesses;
- narrative closure;
- theological proclamation;
- resurrection appearances;
- canon/institution;
- reader reception.

### What Pairwise Graph Loses

The pairwise graph tends to collapse the case into a dense neighborhood around `C`.

It can say:

```text
C is related to textual witnesses and theology and institution.
```

But it struggles to show that each layer-bundle solves a different transmission problem.

## Typed Temporal Hypergraph Representation

A hypergraph can represent different bundles around the same ending problem.

### e1_textual_witness

```text
e1_textual_witness = {
  Mark_16_8,
  abrupt_ending,
  manuscript_witness_variation,
  textual_uncertainty,
  source_critical_instruction
}
```

Function:

```text
Preserve the problem as a textual-critical object.
```

Instruction:

```text
Do not flatten the tradition; distinguish textual layers and witness status.
```

### e2_narrative_open_ending

```text
e2_narrative_open_ending = {
  Mark_16_8,
  fear,
  silence,
  unresolved_closure,
  reader_pressure,
  discipleship_failure_pattern
}
```

Function:

```text
The ending can transmit an instruction through unresolved narrative pressure.
```

Possible instruction:

```text
The reader/community must confront fear, silence, and failed proclamation.
```

### e3_theological_closure

```text
e3_theological_closure = {
  Mark_16_9_20,
  resurrection_appearance,
  proclamation_command,
  mission_expansion,
  symbolic_completion
}
```

Function:

```text
Supply theological and proclamation closure.
```

Possible instruction:

```text
The resurrection must become testimony and mission, not unresolved silence.
```

### e4_institutional_stabilization

```text
e4_institutional_stabilization = {
  Mark_16_9_20,
  canonical_use,
  liturgical_reading,
  accepted_ending_practice,
  community_stability
}
```

Function:

```text
Stabilize the text for communal transmission.
```

Possible instruction:

```text
The community needs a usable closure for teaching, reading, and institutional continuity.
```

### e5_modern_critical_reading

```text
e5_modern_critical_reading = {
  Mark_16_8,
  Mark_16_9_20,
  brackets_or_footnotes,
  textual_criticism,
  layered_reading_instruction
}
```

Function:

```text
Allow both reception history and textual uncertainty to remain visible.
```

Possible instruction:

```text
Read the text with layered discipline: do not erase either the abrupt ending or the longer reception tradition.
```

## Distinguishing Gain

The hypergraph model adds value if the Mark ending problem is not one contradiction but a bundle-intersection zone.

### 1. Different bundles solve different transmission problems

Pairwise graph says:

```text
C is linked to narrative closure and theology.
```

Hypergraph says:

```text
e2 keeps unresolved narrative pressure.
e3 supplies theological proclamation closure.
e4 stabilizes communal/canonical use.
e5 preserves modern critical layering.
```

This is a real gain.

### 2. Same textual problem, different instruction functions

The same ending problem can transmit different instructions depending on bundle:

| Bundle | Instruction function |
|---|---|
| textual witness bundle | distinguish textual layers |
| narrative open-ending bundle | confront fear/silence/unresolved discipleship |
| theological closure bundle | convert resurrection into proclamation/mission |
| institutional stabilization bundle | provide usable communal closure |
| modern critical reading bundle | preserve both uncertainty and reception history |

A simple pairwise graph can list these links but does not encode that they are competing/coexisting transmission regimes.

### 3. Layer table vs hypergraph

A layer table can describe the layers clearly.

The hypergraph is only better if it also shows overlapping carriers and competing transmission functions.

In this case it does:

```text
Mark_16_8 participates in textual, narrative, and modern-critical bundles.
Mark_16_9_20 participates in theological, institutional, and modern-critical bundles.
Modern critical reading is itself a new bundle that keeps both older bundles visible.
```

This is stronger than a static layer table because it shows how the same textual objects are reused by different transmission regimes.

## Failure / Caution

This test does not prove:

- original ending of Mark;
- theology of resurrection;
- history of the early community;
- exact manuscript genealogy;
- canonical legitimacy or illegitimacy of the longer ending.

The model only helps describe transmission functions around a textual rupture.

## Result

```text
Probe passes concrete Mark ending stress-test with restrictions.
```

The pass reason:

```text
The hypergraph model shows that Mark 16:8 / 16:9-20 is not one problem but a set of overlapping transmission bundles: textual-critical, narrative, theological, institutional, and modern-critical.
```

The restriction:

```text
A simple layer table remains sufficient if the goal is only to list layers.
Hypergraph adds value only when modeling bundle overlap, competing instruction functions, and reuse of the same textual objects across regimes.
```

## Consequence for the Formalization Probe

The hypergraph probe can be upgraded from only a speculative formalization probe to a limited method candidate for Culture as Instructions + MEAT.

Suggested status:

```text
method_candidate / non-canon / case-supported / requires source discipline
```

Do not promote to canon yet.

## Next Step

Create a method note only if needed:

```text
03_CULTURE_AS_INSTRUCTIONS/METHODS/higher_order_instruction_network_method.md
```

The method must include strict entry conditions:

- use only when bundle overlap matters;
- use typed nodes;
- use temporal/directional hyperedges;
- keep source verification separate;
- reject if layer table explains the case more simply.
