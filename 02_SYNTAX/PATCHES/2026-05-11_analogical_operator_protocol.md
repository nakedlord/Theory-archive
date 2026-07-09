# Analogical Operator Protocol

```text
layer: governance  (как ведётся архив; нумерация v1.9..v5.x)
```

Status: active working protocol / needs consolidation
Date: 2026-05-11
Source: ChatGPT session with user

## Role in SynTax

This patch adds a default exploratory operator for SynTax: disciplined work with subjective associations.

SynTax should not treat associations as conclusions. It should treat them as raw activation material that can be converted into analogies, operators, abstractions, or rejected as noise.

## Core Problem

AI and humans tend to answer inside the frame activated by the question. More context often deepens the answer inside the same attractor rather than changing the attractor.

Frame escape requires a procedure that can admit non-local associations into the reasoning process without letting them become decorative metaphors.

## Core Distinction

```text
Association = subjective activation from experience, memory, analogy, or latent pattern.
Analogy     = processed association with a mappable similarity.
Operator    = transferable mechanism extracted from a validated analogy.
Abstraction = compressed model of repeated experience that can be tested across domains.
```

## Default Activation

Activate this operator by default when the task involves:

- searching for a new idea;
- breaking a frame;
- comparing distant domains;
- theory development;
- SynTax/R-theory work;
- unexplained mismatch between a question and useful answers;
- user signals such as “на что это похоже”, “как выйти за рамку”, “есть идея”, “давай проверим”.

Do not activate it for simple factual answers, direct editing, arithmetic, or narrow execution tasks unless the user asks for frame work.

## Analogy Search Levels

When searching for analogies, classify the level of similarity:

1. External similarity — weak; often metaphorical.
2. Functional similarity — same role or use.
3. Role similarity — same relation between agents/objects.
4. Structural similarity — same arrangement of parts and dependencies.
5. Dynamic similarity — same sequence of change or transformation.
6. Operator similarity — same underlying mechanism across domains.
7. Failure similarity — same type of breakdown, mismatch, or limitation.

SynTax should prefer structural, dynamic, operator, and failure-level analogies over surface resemblance.

## Analogical Operator Protocol

1. Capture
   - What association appeared?
   - What triggered it?

2. Level
   - Is the similarity external, functional, role-based, structural, dynamic, operator-level, or failure-level?

3. Mapping
   - What corresponds to what across the two domains?
   - Which elements do not map?

4. Gain
   - What does this analogy explain that the original frame did not?
   - What new move does it make possible?

5. Prior Success
   - Has this structure solved a similar class of problems elsewhere?
   - Is the analogy supported by repeated experience or only by a single attractive image?

6. Failure
   - Where does the analogy break?
   - What would make it misleading?

7. Operator Extraction
   - What mechanism can be extracted without keeping the metaphor?

8. Abstraction
   - What general model of experience does this produce?

9. Cross-Test
   - Does the abstraction work in a third domain?
   - Does it predict a useful distinction or failure mode?

10. Integration
   - Classify the result as metaphor, working analogy, operator candidate, abstraction, hypothesis, or canon candidate.

## Output Discipline

A good SynTax output should not stop at “X is like Y”. It should produce one of:

```text
metaphor only -> useful for intuition, not reasoning
working analogy -> useful but bounded
operator candidate -> transferable mechanism
abstraction -> compressed cross-domain model
canon candidate -> stable only after tests and consolidation
```

## Guardrails

- Do not confuse beautiful analogy with explanation.
- Do not use analogy as proof.
- Do not accept surface resemblance unless it produces structural gain.
- Do not over-expand into many analogies if one operator is enough.
- Always ask where the analogy breaks.

## Compact Rule

```text
SynTax should treat association as raw material, analogy as a bridge, operator extraction as the goal, and abstraction as the stabilized product.
```

## Relation to R Theory

This protocol is the SynTax-side operational layer for the R-theory mechanism described in:

```text
01_R_THEORY/PATCHES/2026-05-11_associative_frame_escape.md
```

SynTax owns the method. R Theory owns the cognitive mechanism.
