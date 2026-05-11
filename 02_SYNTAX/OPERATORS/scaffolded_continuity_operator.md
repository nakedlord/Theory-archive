# Scaffolded Continuity Operator

Status: active operator candidate / needs consolidation
Date: 2026-05-11
Source: ChatGPT session with user

## Purpose

This operator tells SynTax how to use Git-based memory as an external scaffold for continuing thought, not merely storing transcripts.

The operator should be active by default in theory/SynTax sessions where the user brings new ideas, asks to continue a prior line, or wants ideas preserved for later development.

## Core Rule

```text
Do not restart reasoning if an active idea state exists.
Recover the idea state, identify what is new, update weighted links or operators, and record the next test.
```

## Input Conditions

Activate when:

- the user brings a new theory idea;
- the user asks to save or continue a thought;
- the topic touches SynTax, R Theory, associative reasoning, memory, canon, or frame escape;
- an idea may update an existing active idea card;
- new data may revise an older hypothesis.

Do not activate for narrow factual answers or one-off execution tasks unless the user asks for theory/memory continuity.

## Required Re-Entry Steps

1. Read the active ideas index:

```text
00_META/ACTIVE_IDEAS_INDEX.md
```

2. Check whether the current input updates an existing idea.

3. If yes, do not create a duplicate. Update or propose an update to the existing idea card.

4. If no, create a new idea card using:

```text
00_META/IDEA_CARD_SCHEMA.md
```

5. Preserve the new state:

- current formulation;
- why it appeared;
- weighted associations;
- scaffolds;
- analogies and their level;
- extracted operator;
- what it solves;
- failure modes;
- revision history;
- next test.

## Reasoning Procedure

When processing a new idea:

```text
1. Identify weighted associations.
2. Identify relevant scaffolds.
3. Find analogies and classify their level.
4. Extract the operator, if any.
5. Compare with existing active ideas.
6. Decide whether this is an update, split, merge, or new card.
7. Preserve the next test.
```

## Output Discipline

The final answer to the user should not expose the whole machinery unless useful.

But internally the result should distinguish:

- raw association;
- working analogy;
- operator candidate;
- active hypothesis;
- canon candidate;
- rejected/archived idea.

## Memory Discipline

Bad memory:

```text
We discussed X.
```

Good memory:

```text
X is currently an active hypothesis.
It appeared because of Y.
Its strongest weighted links are A/B/C.
Its scaffold files are P/Q/R.
Its extracted operator is O.
The next test is T.
```

## Relation to Analogical Operator Protocol

The Analogical Operator Protocol handles how associations become analogies, operators, and abstractions.

The Scaffolded Continuity Operator handles how those products remain available for future sessions and can be updated instead of rediscovered.

## Relation to R Theory

R Theory explains the cognitive mechanism: weighted associations and R3 externalization of instructions.

SynTax applies that mechanism deliberately through Git memory and idea cards.

## Compact Formula

```text
Associations generate movement.
Scaffolds preserve direction.
Idea cards preserve state.
Operators preserve usability.
```
