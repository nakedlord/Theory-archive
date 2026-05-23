# Source Note: AI-Assisted Precognition / Опережающее мышление

Status: source note / human-note-backed chat insight
Date: 2026-05-23
Source ID: `syntax-2026-05-23-ai-assisted-precognition`
Source class: `chat_export` + `human_note`
Target module: `02_SYNTAX`
Related modules: `01_R_THEORY`, `03_CULTURE_AS_INSTRUCTIONS`, `00_META`

## Source Context

The idea appeared during a ChatGPT session after the user shared a transcript of the YouTube video `I was laid off by Atlassian` and used the assistant to extract reusable architectural principles from the transcript instead of watching the video linearly.

The sequence was:

```text
noticed potentially valuable source
  -> obtained transcript
  -> asked AI to extract useful ideas
  -> mapped ideas to user's own systems
  -> created an implementation plan
  -> wrote a CSP handoff for Codex
```

The user then generalized the process: they increasingly do not read long articles linearly when a source merely looks potentially interesting. Instead, they send the source to an AI and ask what it says, what is interesting for them, what concepts are inside, what can be applied, and whether it deserves deeper attention.

The user named this mode `опережающее мышление`; the English analogue that emerged was `precognition`, later clarified as non-mystical `AI-assisted precognition`.

## Core Source Claim

AI enables a new information-processing order:

```text
old order:
attention -> consumption -> understanding -> relevance judgment -> application

new order:
source signal -> AI probe -> value map -> selective attention -> transfer/application
```

The model is not about paranormal foresight. It is about preliminary understanding before full human consumption of a source.

## Working Definition

`AI-assisted precognition` / `опережающее мышление` is an AI-supported mode in which a person uses a model as a scout before investing deep attention. The source is first probed for meaning, density, transferable operators, relevance to the person's systems, and possible actions; only after that does the person decide whether to enter the source deeply.

## Important Distinction

This is not ordinary summarization.

```text
Summary asks: what does the source say?
Precognition asks: what can this source do for my system?
```

The relevant output is not only a summary but a value map, operator extraction, transfer hypothesis, and implementation path.

## Relation To The Atlassian Transcript Case

In the Atlassian transcript case, the user did not need Atlassian's code, internal infrastructure, or private implementation. The useful extraction was architectural:

- self-service broker;
- async provisioning pipeline;
- control plane;
- centralized edge layer;
- sidecars;
- maintenance/on-call discipline;
- churn as a signal of future complexity.

These were mapped into the user's own ecosystem as:

- Knowledge Broker;
- Agent Control Plane;
- AI Edge;
- Domain Sidecars;
- Promotion Gates;
- Churn Detector;
- Agent On-Call Runbook.

## Confidence And Boundaries

Confidence: medium-high as a descriptive cognitive/workflow model.

Current limitation: this source note is based on one chat session and the user's self-observation. It should be treated as an active hypothesis/operator candidate, not canon.

## Next Use

Use this source note as provenance for the idea card:

```text
02_SYNTAX/HYPOTHESES/2026-05-23_ai_assisted_precognition.md
```
