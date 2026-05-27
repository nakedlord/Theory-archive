# Theory Archive Source Registry

Status: active registry
Date: 2026-05-26
CSP event: `projects/syntax/events/2026-05-17-codex-knowledge-compilation-layer-v1.md`

## Purpose

This registry gives future agents stable source classes and IDs for theory,
evidence, idea-state, and canon-candidate updates.

It complements:

- `00_META/ACTIVE_IDEAS_INDEX.md`
- `00_META/MEMORY_SYSTEM_ARCHITECTURE.md`
- `00_META/MIGRATION_STATUS_RULES.md`
- `00_META/CANDIDATE_TO_CANON_CHECKLIST.md`

## Source Classes

| Source Class | Use For | Required Evidence |
|---|---|---|
| `chat_export` | Theory/SynTax/R Theory conversations that produced reusable ideas. | Chat/session ID, date, agent, summary, target module. |
| `idea_card` | Active idea-state files and their revisions. | Path, status, related modules, next test. |
| `external_reference` | Papers, articles, docs, books, or public sources used as evidence. | URL/citation, retrieval date, applicability note. |
| `repo_artifact` | Existing committed theory docs, patches, cases, or versions. | Repo, branch, path, commit hash if known. |
| `human_note` | User-provided durable theory clarification. | Date, author/context, confirmation status. |

## Source ID Format

Use stable, readable IDs:

```text
theory-YYYY-MM-DD-short-topic
rtheory-YYYY-MM-DD-short-topic
syntax-YYYY-MM-DD-short-topic
source-YYYY-MM-DD-short-topic
```

## Initial Registry

| Source ID | Source Class | Status | Target Area | Notes |
|---|---|---|---|---|
| `theory-active-ideas-index` | `idea_card` | active | `00_META/ACTIVE_IDEAS_INDEX.md` | Existing active idea re-entry map. |
| `theory-memory-system-architecture` | `repo_artifact` | active | `00_META/MEMORY_SYSTEM_ARCHITECTURE.md` | Existing memory architecture map. |
| `theory-migration-status-rules` | `repo_artifact` | active | `00_META/MIGRATION_STATUS_RULES.md` | Existing migration/canon status policy. |
| `source-2026-05-18-higher-order-instruction-networks` | `external_reference` + `human_note` | source_verified_for_representation_risk / hypothesis | `03_CULTURE_AS_INSTRUCTIONS/SOURCES/2026-05-18_higher_order_networks_source_note.md`; `03_CULTURE_AS_INSTRUCTIONS/SOURCES/2026-05-19_weighted_hypergraph_distance_verification.md`; `03_CULTURE_AS_INSTRUCTIONS/HYPOTHESES/2026-05-18_hypergraph_formalization_probe.md`; `03_CULTURE_AS_INSTRUCTIONS/CASES/2026-05-19_hypergraph_carrier_bundle_test.md` | User reframed higher-order / hypergraph network math as a formalization probe for Culture as Externalized Instructions. Underlying verified source: `Distances in weighted higher-order networks`, Communications Physics, 2026-03-26. Supports representation-risk claim only, not cultural canon. |
| `syntax-2026-05-23-ai-assisted-precognition` | `chat_export` + `human_note` | active_hypothesis / operator_candidate | `02_SYNTAX/SOURCES/2026-05-23_ai_assisted_precognition_source_note.md`; `02_SYNTAX/HYPOTHESES/2026-05-23_ai_assisted_precognition.md` | User formulated `опережающее мышление` / AI-assisted precognition after using AI to pre-process a transcript, extract transferable architecture, map it to their own systems, and write a CSP/Codex implementation plan. Non-canon; to be tested across multiple source types. |
| `source-2026-05-25-pmv-action-symbols` | `external_reference` | source_verified / evidence_note / non_canon_case_check | `01_R_THEORY/SOURCES/2026-05-25_pmv_action_symbols_nature_source.md`; `01_R_THEORY/EVIDENCE/2026-05-25_pmv_action_symbols_evidence_note.md`; `01_R_THEORY/CASES/2026-05-26_action_symbol_archaeology_check.md` | Nature 2026 PMv action-symbols paper used as non-canon evidence for action-first abstraction and artifact-as-operation interpretation. Follow-up archaeology case check supports the architecture in a limited sense: Lomekwi proto-operation, Oldowan action-symbol threshold candidate, Acheulean action grammar/R2+ candidate, ochre/burial symbolic carrier layer. Does not prove full R3, language origin, or PMv as a general abstract-thought center. |
| `culture-2026-05-25-myth-dynamic-instruction-network` | `chat_export` + `human_note` | active_hypothesis / non-canon | `03_CULTURE_AS_INSTRUCTIONS/SOURCES/2026-05-25_myth_dynamic_instruction_network_source_note.md`; `03_CULTURE_AS_INSTRUCTIONS/HYPOTHESES/2026-05-25_myth_as_dynamic_instruction_network.md` | User clarified mythologization as a dynamic external instruction network with temporary activation centers, agency compression, R1 mass-transmission compression, and R2/R3 infrastructure requirements. Non-canon; needs concrete textual/historical case test. |
| `culture-2026-05-26-mark-ending-hypergraph-test` | `external_reference` + `repo_artifact` | partial_source_verification / concrete_textual_stress_test / non-canon | `03_CULTURE_AS_INSTRUCTIONS/SOURCES/2026-05-26_mark_ending_textual_source_note.md`; `03_CULTURE_AS_INSTRUCTIONS/CASES/2026-05-26_mark_ending_hypergraph_test.md` | Concrete stress-test for hypergraph modeling on Mark 16:8 and the longer ending tradition. Uses only cautious textual premises; does not make historical, theological, or canon claims. |

## Rule

Every durable theory source should get a source ID before it updates a theory
page. If an idea is speculative, mark it as draft, hypothesis, evidence, or
candidate rather than canon.
