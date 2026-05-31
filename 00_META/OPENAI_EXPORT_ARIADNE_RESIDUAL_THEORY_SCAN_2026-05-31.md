# OpenAI Export Ariadne Residual Theory Scan

Status: residual source audit / not canon / needs consolidation
Date: 2026-05-31
CSP project: `syntax`
CSP thread: `openai-export-routing`
CSP event: `projects/syntax/events/2026-05-31-codex-ariadne-openai-export-residual-theory-scan.md`
Source ID: `theory-2026-05-31-ariadne-openai-residual-theory-scan`
Source class: `chat_export_audit`

## Scope

This pass lets Ariadne inspect the raw local ChatGPT export after the previous
second-pass theory audit.

Source material:

- raw local export: `C:/Users/imnak/Downloads/OpenAI-export.zip`
- nested conversation shards: `conversations-000.json`, `conversations-001.json`,
  `conversations-002.json`
- whole-corpus manifest:
  `C:/Users/imnak/OneDrive/ChatGTP/OPENAI_EXPORT_INGEST/2026-05-28-inventory/conversation_manifest.jsonl`
- prior baseline:
  `00_META/OPENAI_EXPORT_SECOND_PASS_THEORY_AUDIT_2026-05-31.md`

No raw transcript text is committed here. This file records source IDs, routing
verdicts, extracted idea summaries, and non-import decisions.

## Method

1. Loaded all 260 raw conversations from the local export.
2. Compared conversation IDs and short IDs against the existing Theory Archive.
3. Scored remaining raw conversations by theory-like signals, with user-authored
   text weighted above assistant-generated summaries.
4. Manually reviewed the highest-scoring uncovered rows and route-mismatch rows.
5. Rejected false positives where the score came from generic words like
   `model`, `culture`, `meaning`, or `network` inside GYMKiDs, product-code,
   health, design, or utility chats.
6. Preserved only durable theory residues as source notes.

## Main Result

Ariadne did not overturn the previous raw second-pass audit. It found two
smaller residual sources worth preserving as non-canon provenance:

| Conversation ID | Title | Earlier status | Ariadne verdict | Artifact |
|---|---|---|---|---|
| `69328718-7ecc-832e-b310-016095f93ddd` | `Болтать по пути` | not source-recorded in Theory Archive | source note for language as an evaluation/framing layer rather than deterministic thought structure | `02_SYNTAX/SOURCES/2026-05-31_language_evaluation_layer_chat_export_source_note.md` |
| `67a79da2-eb9c-8013-b966-6abb8d975a07` | `Легенда о бессмертии` | not source-recorded in Theory Archive | source note for immortality/no-reproduction as a speculative social role and skill-drift model | `03_CULTURE_AS_INSTRUCTIONS/SOURCES/2026-05-31_immortality_skill_drift_chat_export_source_note.md` |

Both are source notes only. No canon page was changed and no external claim was
accepted as evidence.

## Interesting But Not Imported

These rows looked interesting during the scan but did not justify new Theory
Archive artifacts in this pass.

| Conversation ID | Title | Verdict |
|---|---|---|
| `69f39478-3fdc-832f-981b-9b6bb5a930af` | `Persistent Memory for AI` | Operationally useful for agent memory / task graph evaluation, but it routes to `agent-playbook` or CSP/codex-ops method work rather than Theory Archive. It may inform Ariadne/CSP later, but is not a theory import here. |
| `688a4f3c-24f4-832b-9ede-d32b042ed225` | `Второй источник неопределенности` | Latour/source-theory lead only. Adjacent Latour rows are already recorded in the culture/religion closure. This row should be reopened only with a concrete Latour source-card task. |
| `2402fea3-e58d-43dd-b4c0-b018380495de` | `Virtual Assistant Helps Queries` | Information structural realism explanation was assistant-generated and source-like, not a user-developed theory artifact. Keep as reading/source lead only. |
| `67bcb9c1-cdd8-8013-94ea-fae9df6253b1` | `Основание Нобелевской премии` | Contains user conceptual pressure around fields, photons, probability, and quantum operators. Do not import as physics evidence; use external physics sources if entanglement or operator-boundary work resumes. |
| `692b2b10-98a8-832a-b934-180537fbf09b` | `Выбор книги в магазине` | Reading-navigation source: Hayek, Bekhterev, Lombroso, Lorenz. Useful for future reading choices, not a current theory artifact. |
| `67027097-ecf0-8013-9753-da6061fc9c6a` | `Санся и предпочтения` | Possible culture/comparative mythology source-only row about Chinese fantasy categories. Not enough for a durable theory artifact without a concrete case task. |
| `67154a1b-7bbc-8013-b561-23305ae2598d` | `Дунхуа Perfect World` | Fantasy cultivation taxonomy/source-only. Could become a case for symbolic progression systems, but not a theory import now. |
| `687dcdf3-89bc-8013-9607-fa962bcfc08f` | `Происхождение названия Химки` | Mixed local-history and film `Her` discussion. Interesting for the user's Ariadne naming motif, not a Theory Archive source artifact. |

## False Positives / Route-Outs

The scoring pass also surfaced several high-volume or keyword-heavy rows that
should not be imported into Theory Archive:

| Conversation ID | Title | Reason |
|---|---|---|
| `68679d80-0e9c-8013-a113-78691540ab9a` | `Методическое пособие по паркуру` | GYMKiDs/Fly Zone methodology route; not Theory Archive unless deliberately used as a theory case. |
| `69d4b787-6358-8332-aebb-a7364c74856a` | `Буклет для клиентов GYMKIDs` | GYMKiDs client/material route; theory-like words are layout/copy noise. |
| `69f5d445-0d20-832a-bc93-d67cb6eaffb8` | `Создание репозитория продолжение` | Product/CSP implementation trace; any durable agent-memory idea belongs in `agent-playbook` or CSP method evaluation. |
| `675c15c5-193c-8013-8cab-7bfc9802399b` | `Переработка текста` | GYMKiDs product copy / physical culture wording. Route to GYMKiDs if needed. |
| `697a1798-ae58-832c-b311-230b7b3744c0` | `Диалоговый тренажёр тренера` | Product implementation route. |
| `6891c0a1-afe4-8324-b447-a09805a5bdeb` | `Работа FLY ZONE регламенты` | GYMKiDs/Fly Zone regulations route. |
| `685e730e-5f78-8013-9c86-6c77dac05d57` | `Процент жира по фото` | Health/body-composition route; not theory. |
| `698f19c3-0be0-8390-b5e1-fd3e1c1187e3` | `Зачем дневник трейсера` | GYMKiDs/Fly Zone product/material route. |
| `6974cce0-ab04-832a-81bb-022e6e1cd641` | `Маркетинг-партнёр` | Business/marketing route. |

## Residual Risk

This pass reduces the chance of missing large theory residue, but it is not a
mathematical proof that no small phrase in 260 chats could later become useful.

Current residual risk:

- low for high-signal, source-recordable theory rows;
- medium for future case-specific rows that only become relevant after a new
  theory question appears;
- high for Google Drive/source-family material, because this scan covers the
  local OpenAI export only.

## Next Actions

1. Keep the previous raw second-pass audit as the main baseline.
2. Treat this file as a residual addendum, not as a replacement.
3. If developing SynTax operators, source-check the language evaluation layer
   against linguistic relativity, translation studies, bilingual cognition, and
   existing Domain Tone Router / Cognitive Ascent Architecture notes.
4. If developing Culture as Instructions, test the immortality/skill-drift row
   only as a speculative stress case for role turnover, generation replacement,
   and cultural transmission without reproduction.
5. Continue Drive/source-family closure separately; this scan does not close
   Drive.
