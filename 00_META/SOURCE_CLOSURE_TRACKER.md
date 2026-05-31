# Theory Archive Source Closure Tracker

Status: active control surface / needs consolidation
Date: 2026-05-31
CSP project: `syntax`
CSP thread: `openai-export-routing`

## Purpose

This tracker is the closure layer for personal/theory source intake.

It exists because the archive already has:

- source-backed theory modules;
- source registry rows;
- an ingest log;
- a local OpenAI export note pool;
- older Google Drive/source audit notes.

But it did not yet have one page that answers:

```text
Which personal/theory chats and Drive/source families are known?
Which are already source-recorded?
Which are still pending, source-only, skipped, blocked, or routed elsewhere?
What does "done with chats and Drive" mean?
```

This file does not import chat content by itself and does not promote any idea
to canon.

## Closure Definition

A source family is closed only when every known item has one of these terminal
or controlled statuses:

- `source_recorded`: source has a row in `SOURCE_REGISTRY.md` and an ingest log
  or explicit target artifact.
- `partially_recorded`: source has some target artifacts, but there is still a
  defined review/import residue.
- `source_only`: keep as provenance, reading material, or historical context;
  no current target artifact.
- `skipped`: no durable value for Theory Archive after review.
- `routed_elsewhere`: belongs in another repo/project, for example `GYMKIDS`,
  `agent-playbook`, a product repo, or a future repository request.
- `blocked`: cannot close until source access, Drive inventory, original file,
  or human answer appears.
- `needs_triage`: known item, not yet critically reviewed enough.
- `candidate_import`: likely useful, but not yet converted into a source record
  and target artifact.

For closure, there should be no `needs_triage` rows left.

## Source Families

| Family | Location / Source | Count / Scope | Current Status | Next Action |
|---|---|---:|---|---|
| OpenAI export notes 2026-05-11 | `imports/openai-export/2026-05-11/notes/` | 68 note files | enumerated / mixed status | Process by clusters and close every row. |
| Existing source registry | `00_META/SOURCE_REGISTRY.md` | active registry | active | Reconcile rows below against registry before new imports. |
| Existing ingest log | `00_META/INGEST_LOG.md` | active log | active | Append only when source closure creates or changes durable artifacts. |
| Theory Drive / source audit | `00_META/COVERAGE_AUDIT_2026-04-25.md` and Drive references | partial, old audit | blocked / inventory missing | Create a Drive source ledger when a fresh inventory or connector pass is available. |
| GYMKiDs / applied work residue | theory chats and export rows that mention pedagogy, parkour, trainer methodology, business ops | cross-project | route through `gymkids-kb-fill` | Do not store applied GYMKiDs/Fly Zone work in Theory Archive unless it is an explicit theory case. |
| Agent/tool/product residue | memory tooling, GitHub memory, OpenClaw, personal apps, transcript setup | cross-project | route check required | Route durable agent-ops to `agent-playbook`; product code/docs to product repos. |

## Processing Rules

1. Treat ChatGPT output skeptically. Prefer user-authored claims, pasted source
   fragments, and clearly named source files over assistant-generated rewrites.
2. Do not canonize during source closure. Use `source_note`, `hypothesis`,
   `candidate_patch`, `case`, `evidence`, or `source_only`.
3. If a chat mixes theory, GYMKiDs, product, and agent operations, split by
   durable route instead of forcing it into one module.
4. If a source is only a generated image, design attempt, casual conversation,
   or utility search, mark it `source_only` or `skipped` unless it contains a
   reusable theory/operator delta.
5. For Drive, start metadata-first. Do not claim Drive closure until a fresh
   inventory or repeatable connector pass exists.

## OpenAI Export Notes Ledger

Initial status is a routing/closure status, not an import verdict. Rows marked
`candidate_import` still require a source note or explicit skip decision before
closure.

| Note File | Title | Primary Route | Status | Next Action |
|---|---|---|---|---|
| `00-canon-6943f980-3f.md` | 00_CANON | `02_SYNTAX/` | `source_recorded` | Covered by SynTax module files and `02_SYNTAX/SOURCES/2026-05-31_syntax_memory_dialogue_source_closure.md`; no canon promotion. |
| `01-errorlog-6943f9da-6d.md` | 01_ERRORLOG | `02_SYNTAX/` | `source_recorded` | Early error-hygiene provenance recorded in the 2026-05-31 SynTax closure note. |
| `02-cases-6943fa34-d4.md` | 02_CASES | `02_SYNTAX/` | `source_recorded` | Early case-format provenance recorded in the 2026-05-31 SynTax closure note. |
| `ai-инструменты-для-личного-знания-и-syntax-os-69f16123-7f.md` | AI tools for personal knowledge and SynTax OS | `02_SYNTAX/` + `agent-playbook` | `partially_recorded` | PKM critique and agent/tooling split recorded in the 2026-05-31 SynTax closure note; route product/process residue outside Theory Archive. |
| `ec-os-v-2-0-693d68bc-91.md` | EC-OS v.2.0 | `02_SYNTAX/` | `partially_recorded` | EC-OS preserved as predecessor/provenance in the 2026-05-31 SynTax closure note; not promoted to standalone canon. |
| `how-are-you-67437789-55.md` | How are you | none / personal | `needs_triage` | Review for durable idea delta; otherwise mark skipped. |
| `m5-theory-6910571f-8d.md` | M5 Theory | `06_BOUNDARY_SATURATION/` | `source_recorded` | Use existing M5 source note and verification plan; no further import unless new residue is found. |
| `meat-pna-mccr-693da148-49.md` | MEAT, PNA, MCCR | `04_MEAT/` + `05_PNA/` | `source_recorded` | Next work is MCCR review/classification, not source discovery. |
| `r-theory-3-1-canon-69e4b2dc-86.md` | R-theory 3.1 Canon | `01_R_THEORY/` | `source_recorded` | Old v3.1/v3.3 provenance recorded in `01_R_THEORY/SOURCES/2026-05-31_rtheory_thought_archaeology_source_closure.md`; no canon rewrite. |
| `r-теория-и-структурация-69c581fa-03.md` | R-theory and structuration | `01_R_THEORY/` + `90_CROSS_LINKS/` | `source_recorded` | Existing R Theory structuration source note and instruction-runtime split remain authoritative; checked in cluster 2 closure. |
| `r3-1-3-694a3e41-03.md` | R3.1-3 | `01_R_THEORY/` | `source_recorded` | R3 compact canon is accepted; cluster 2 closure confirms remaining residue is route-specific, not more R3 extraction. |
| `syntax-cognitive-model-69359fed-3f.md` | Syntax cognitive model | `02_SYNTAX/` | `partially_recorded` | Statistical/cognitive framing recorded as provenance in the 2026-05-31 SynTax closure note; no new operator yet. |
| `syntax-os-693479d0-f1.md` | Syntax OS | `02_SYNTAX/` | `source_recorded` | Existing Syntax OS source note covers main route; residue checked in the 2026-05-31 closure pass. |
| `syntax-sync-лог-6943fa8f-b6.md` | SynTax sync log | `02_SYNTAX/` | `source_recorded` | Append-only sync provenance recorded in the 2026-05-31 SynTax closure note. |
| `агентность-иисуса-христа-69d5429f-ad.md` | Agency of Jesus Christ | `03_CULTURE_AS_INSTRUCTIONS/` + `07_SOTERIOLOGICAL_RITUAL_ACCUMULATION/` | `candidate_import` | Review as culture/religion case source; separate theological claim from instruction-network model. |
| `активировать-syntax-69eaf9d5-49.md` | Activate SynTax | `03_CULTURE_AS_INSTRUCTIONS/` + `07_SOTERIOLOGICAL_RITUAL_ACCUMULATION/` | `candidate_import` | Title is misleading for SynTax closure; process with the culture/religion cluster because the digest is about Jesus agency and New Testament analysis. |
| `активировка-синтакс-режима-69e12d63-f9.md` | SynTax mode activation | `02_SYNTAX/` + `agent-playbook` | `partially_recorded` | SynTax activation and agent-harness split recorded in the 2026-05-31 closure note; do not reconstruct hidden prompts. |
| `анализ-творчества-691ff022-99.md` | Creativity analysis | `02_SYNTAX/` + possible culture/case | `needs_triage` | Decide whether it contains an operator/case or only casual analysis. |
| `архетип-и-достижения-пользователя-69417ea3-81.md` | User archetype and achievements | `02_SYNTAX/` / personal profile | `needs_triage` | Use only if it updates identity/continuity operators; otherwise source-only. |
| `архитектура-syntax-69ad0e69-8d.md` | SynTax architecture | `02_SYNTAX/` | `partially_recorded` | Validation Layer is covered; Execution Trace residue remains review-only in the 2026-05-31 SynTax closure note. |
| `аудит-памяти-chatgpt-69fecf0b-f9.md` | ChatGPT memory audit | `agent-playbook` + CSP provenance | `routed_elsewhere` | Mainly GitHub/CSP tool-call and memory-audit process provenance; no theory import in this pass. |
| `болталка-2-0-692604cd-83.md` | Boltalka 2.0 | `02_SYNTAX/` | `source_only` | Broad early self-analysis/provenance; no clean missing SynTax delta from the digest after closure review. |
| `болталка-3-0-идеи-6933051b-95.md` | Boltalka 3.0 ideas | `02_SYNTAX/` | `source_recorded` | Existing source note covers main route; check only for residue. |
| `болталка-3-1-693484aa-b5.md` | Boltalka 3.1 | `02_SYNTAX/` | `source_recorded` | Existing source note covers main route; process cross-route queue if needed. |
| `болталка-6943fe5d-54.md` | Boltalka | `02_SYNTAX/` | `needs_triage` | Review for distinct idea/operator delta. |
| `болталка-и-поиск-инфы-6891c1ad-50.md` | Boltalka and information search | `02_SYNTAX/` + source workflow | `needs_triage` | Decide whether it belongs to SynTax, agent-playbook, or source-only. |
| `взаимодействие-памяти-и-гаджетов-69eef777-3d.md` | Memory and gadgets interaction | `02_SYNTAX/` + memory architecture | `source_only` | Digest appears noisy/misrouted; keep as provenance unless a raw-transcript pass finds a durable memory-architecture delta. |
| `википедия-68aa1003-0b.md` | Wikipedia | source/reference | `needs_triage` | Mark source-only unless it contributed a concrete theory case or external-reference route. |
| `выбор-подержанного-авто-680cc303-72.md` | Used car choice | outside Theory Archive | `source_only` | No theory import unless a surprising operator is found. |
| `гиперболизация-человеческих-инстинктов-687ca471-69.md` | Hyperbolization of human instincts | `09_REPRODUCTIVE_STRATEGY/` + culture | `candidate_import` | Check against reproductive-strategy module and avoid folk-biological overclaims. |
| `госпожа-бовари-epub-67627fe9-28.md` | Madame Bovary epub | reading/source | `needs_triage` | Use only as literature/culture case if a theory claim was made. |
| `жизнь-как-набор-инструкций-694943ff-4b.md` | Life as a set of instructions | `03_CULTURE_AS_INSTRUCTIONS/` + `01_R_THEORY/` | `candidate_import` | Likely high-value culture/R Theory bridge; process early. |
| `занудная-болталка-6943dd99-de.md` | Tedious Boltalka | `02_SYNTAX/` | `needs_triage` | Review for distinct source value; likely source-only if repetitive. |
| `использование-github-в-памяти-69fcd5ad-ba.md` | Using GitHub in memory | `agent-playbook` + CSP provenance | `routed_elsewhere` | Mainly operational GitHub/CSP memory workflow; no raw tool-call import into Theory Archive. |
| `история-артефактов-до-верхнего-палеолита-693c17f5-60.md` | Artifact history before Upper Paleolithic | `01_R_THEORY/` | `partially_recorded` | Existing archaeology source cards/comparison table cover the safer route; keep only source leads or raw-transcript residue, no duplicate claims. |
| `как-измерить-период-полураспада-идей-69ed62d8-45.md` | How to measure idea half-life | `03_CULTURE_AS_INSTRUCTIONS/` | `candidate_import` | Candidate for Cultural Instruction Decay empirical/measurement route. |
| `кинонавигатор-68f50d7e-0d.md` | Movie navigator | outside Theory Archive / product idea | `source_only` | Route outside only if revived as product; otherwise skip. |
| `книга-койре-обзор-693b19c7-fd.md` | Koyre book review | culture / history of science source | `candidate_import` | Review as external-reading source/case, not canon by itself. |
| `книги-и-философия-6891965a-57.md` | Books and philosophy | reading/source | `needs_triage` | Extract only concrete reading routes or theory cases. |
| `мастер-родословной-в-аниме-66fb8bad-0b.md` | Lineage master in anime | culture/case candidate | `needs_triage` | Use only if it tests a culture/transmission model. |
| `математика-для-чайников-6921f3da-39.md` | Math for beginners | personal learning/source | `source_only` | No theory import by default. |
| `методика-обучения-паркуру-67f91a0d-6a.md` | Parkour teaching methodology | `GYMKIDS` route | `routed_elsewhere` | Route to `gymkids-kb-fill` unless explicitly used as theory/pedagogy case. |
| `новости-и-обновления-6725b41f-8d.md` | News and updates | none / temporal | `source_only` | Do not import unless tied to a durable source route. |
| `о-чем-ты-подумал-6955483e-e2.md` | What did you think about | `02_SYNTAX/` | `needs_triage` | Review for self-reflection/operator delta. |
| `обсуждение-книги-латура-688a4700-14.md` | Latour book discussion | `03_CULTURE_AS_INSTRUCTIONS/` + source theory | `candidate_import` | Review as culture/instruction-network external source case. |
| `объективность-и-субъектность-69fce53f-ed.md` | Objectivity and subjectivity | `08_KANT_NVC_PREDICATION_HYGIENE/` + `02_SYNTAX/` | `candidate_import` | Compare with Kant/NVC predication hygiene before new artifact. |
| `онтология-мысли-692f3d2b-4d.md` | Ontology of thought | `03_CULTURE_AS_INSTRUCTIONS/` + source cases | `candidate_import` | Title is misleading for R/PNA closure; process with culture/religion because the digest is about Ka, Maat, and Egyptian conceptual structure. |
| `ответ-на-вопросик-6943a96f-ef.md` | Answer to a small question | unknown | `needs_triage` | Review title/content; likely source-only unless theory delta exists. |
| `переворот-интуиции-69961ffb-28.md` | Intuition reversal | `01_R_THEORY/` + `02_SYNTAX/` | `partially_recorded` | Operation-type exhaustion / explanation-limit motif recorded in cluster 2 closure; no formal operator imported. |
| `попытки-вывести-r4-провалено-693ea03b-a3.md` | Attempts to derive R4 failed | `01_R_THEORY/` | `source_recorded` | Recorded as negative/boundary source for R4; keep the existing R3-mode guardrail and do not introduce R4 by default. |
| `приветик-игорь-69a8786d-7b.md` | Hi Igor | personal/mixed | `needs_triage` | Review for durable content; otherwise skipped. |
| `приложения-для-себя-69fecb94-ad.md` | Apps for myself | product / agent-ops | `routed_elsewhere` | Route to product/agent-playbook only if revived. |
| `разговор-о-мыслях-688afac4-81.md` | Conversation about thoughts | `03_CULTURE_AS_INSTRUCTIONS/` + reading/source theory | `candidate_import` | Rerouted from R/PNA closure; digest points to Latour/Dawkins/source-theory material. |
| `роза-мира-андреева-69f58504-37.md` | Andreev's Rose of the World | `03_CULTURE_AS_INSTRUCTIONS/` + `07_SOTERIOLOGICAL_RITUAL_ACCUMULATION/` | `candidate_import` | Review as religious/culture source case; separate literary/theological claims. |
| `создание-изображения-системы-694258ce-c5.md` | System image generation | visual/source-only | `source_only` | Do not import generated image attempts as theory evidence; keep only if diagram architecture mattered. |
| `создание-репозитория-теорий-69ecf671-a4.md` | Theory repository creation | `00_META/` | `source_recorded` | Repository migration provenance recorded in the 2026-05-31 SynTax closure note; existing meta/migration files remain authoritative. |
| `создание-чата-для-транскрипции-68aed8cb-fd.md` | Creating a chat for transcription | `agent-playbook` / workflow | `routed_elsewhere` | Route only if reusable agent workflow exists. |
| `структурирование-памяти-ии-6939385d-95.md` | Structuring AI memory | `02_SYNTAX/` | `source_recorded` | Existing AI memory structure source note covers main route; check residue later. |
| `теория-без-воды-69e13654-f3.md` | Theory without fluff | `02_SYNTAX/` + output/interface residue | `partially_recorded` | Cluster 2 closure records it as format/output-constraint residue, not R-core; avoid canon overwrite. |
| `теория-рекурсивного-выбора-и-символического-разрыва-69233882-c0.md` | Recursive Choice and Symbolic Rupture Theory | `01_R_THEORY/` | `source_recorded` | Existing source note covers main route; cluster 2 closure preserves decoherence as analogy/provenance, not physics evidence. |
| `тест-новой-модели-69a9d35b-2c.md` | New model test | `02_SYNTAX/` / model testing | `needs_triage` | Review for operator/test result; otherwise source-only. |
| `удиви-меня-6962b2f5-5e.md` | Surprise me | unknown | `needs_triage` | Review for durable theory delta; otherwise skipped. |
| `цели-в-архитектуре-диалогов-69ac79a9-bf.md` | Goals in dialogue architecture | `02_SYNTAX/` + `03_CULTURE_AS_INSTRUCTIONS/` | `partially_recorded` | Goal Module provenance recorded; ritual/religion residue routed to the culture/religion cluster. |
| `что-почитать-6936c01c-d0.md` | What to read? | reading/source | `needs_triage` | Extract external-source queue only if tied to active theory gaps. |
| `что-такое-openclaw-69fc16c7-8f.md` | What is OpenClaw | agent/product route | `routed_elsewhere` | Route outside Theory Archive unless it became SynTax operator evidence. |
| `что-такое-кяриз-693bc422-9a.md` | What is kyariz | factual/reference | `source_only` | No theory import by default. |
| `что-такое-стресс-69446ec8-4f.md` | What is stress | `01_R_THEORY/` + `05_PNA/` | `source_recorded` | Covered by `01_R_THEORY/EVIDENCE/stress_metabolic_mismatch.md` and cluster 2 closure; future work is evidence/source verification, not chat import. |
| `что-я-умею-67dbe92c-63.md` | What I can do | personal/profile | `needs_triage` | Use only if it changes active identity/continuity operators; otherwise skipped. |

## Cluster Queue

Process in clusters rather than one chat at a time:

1. `SynTax / memory / dialogue architecture`: 00_CANON, ERRORLOG, CASES,
   Syntax architecture, activation, GitHub memory, memory/gadgets, dialogue
   goals, AI memory.
2. `R Theory / thought / archaeology`: R3/R4 residue, intuition reversal,
   thought ontology, artifact history, stress.
3. `Culture / religion / source cases`: life as instructions, Jesus agency,
   Latour, Koyre, Rose of the World, idea half-life.
4. `MEAT / PNA / reproductive strategy`: instincts hyperbolization, thought
   conversation, MCCR review, PNA residues.
5. `Route-out / source-only cleanup`: used car, movie navigator, personal apps,
   transcription chat, OpenClaw, generated images, casual chats.
6. `Theory Drive inventory`: wait for fresh Drive inventory/connector pass, then
   create a metadata-first Drive ledger.

## Current Next Action

Cluster 1 has a digest-level closure note:

- `02_SYNTAX/SOURCES/2026-05-31_syntax_memory_dialogue_source_closure.md`

Cluster 2 now also has a digest-level closure note:

- `01_R_THEORY/SOURCES/2026-05-31_rtheory_thought_archaeology_source_closure.md`

Continue with cluster 3 (`Culture / religion / source cases`) unless a fresh
Drive inventory becomes available first.

Before changing canon or module pages, check each row against:

- `SOURCE_REGISTRY.md`;
- `INGEST_LOG.md`;
- `ACTIVE_IDEAS_INDEX.md`;
- module `OPEN_GAPS.md`;
- module `MIGRATION_CLOSURE.md`.
