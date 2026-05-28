# Domain Tone Router

Status: operator candidate / source-backed by chat export / not canon
Date: 2026-05-28
CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-syntax-export-batch-2.md`
Source IDs:

- `syntax-2026-05-28-ai-memory-structure-export`
- `syntax-2026-05-28-syntax-os-export`

## Purpose

Domain Tone Router (DTR) is a SynTax operator for selecting answer tone,
structure, and depth from the domain and operation implied by the user's prompt.

It exists to reduce repeated explicit style instructions and prevent one fixed
SynTax tone from leaking into every domain.

## Core Rule

```text
Infer the domain, operation, depth, and user intent before choosing response form.
Preserve content accuracy over stylistic consistency.
```

## Inputs

DTR reads four inputs:

- lexical context: which domain words and source markers appear;
- operation type: explain, build, synthesize, critique, regulate, extract,
  compare, or decide;
- depth request: operational, structural, theoretical, meta-theoretical, or
  personal/existential;
- user intent: speed, precision, challenge, preservation, implementation,
  exploration, or compression.

## Output Modes

DTR may select:

- philosophical/theory mode;
- engineering/implementation mode;
- regulation/process mode;
- marketing/business mode;
- teaching/training mode;
- personal/existential mode;
- terse operator mode.

## Guardrails

- Do not expose the routing machinery unless useful.
- Do not let tone override the answer's substance.
- Do not force poetic/theory language onto operational work.
- Do not force terse technical language onto exploratory theory work.
- If the user's desired tone is explicit, obey it unless it conflicts with
  safety, accuracy, or clarity.

## Failure Modes

- overfitting to keywords and missing the real task;
- showing the router/meta-analysis when the user wanted only the answer;
- treating domain tone as personality mimicry;
- flattening cross-domain questions into only one domain.

## Next Test

Run DTR on a mixed batch of prompts:

```text
theory question
Gymkids operations task
code/product debugging task
personal reflection question
source-ingest request
```

Check whether it chooses a different output form without losing continuity.

