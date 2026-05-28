# Theory Archive Source Registry

Status: active registry
Date: 2026-05-27
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
| `syntax-2026-05-28-syntax-os-export` | `chat_export` | source_note / operator_provenance | `02_SYNTAX/SOURCES/2026-05-28_syntax_os_chat_export_source_note.md`; `02_SYNTAX/OPERATORS/domain_tone_router.md`; `02_SYNTAX/OPERATORS/cognitive_ascent_architecture.md` | ChatGPT export source for architecture-independent SynTax OS, external-backup activation, cross-model identity stability, and self-referential Error-Layer stress tests. |
| `syntax-2026-05-28-boltalka-3-0-ideas-export` | `chat_export` | source_note / operator_provenance | `02_SYNTAX/SOURCES/2026-05-28_boltalka_3_0_ideas_chat_export_source_note.md`; `02_SYNTAX/OPERATORS/cognitive_ascent_architecture.md` | ChatGPT export source for autonomous SynTax idea tree, EC-OS, statistical meaning-distribution framing, CAA, and MET/EAT/Event-first integration tests. |
| `syntax-2026-05-28-boltalka-3-1-export` | `chat_export` | source_note / cross_route_queue | `02_SYNTAX/SOURCES/2026-05-28_boltalka_3_1_chat_export_source_note.md` | ChatGPT export source for own-thought buffer, PNA-like consciousness flashes, Heraclitus/process ontology node, long-context tests, and action-to-meaning transition routing leads. |
| `syntax-2026-05-28-ai-memory-structure-export` | `chat_export` | source_note / operator_provenance | `02_SYNTAX/SOURCES/2026-05-28_ai_memory_structure_chat_export_source_note.md`; `02_SYNTAX/OPERATORS/domain_tone_router.md`; `02_SYNTAX/OPERATORS/cognitive_ascent_architecture.md` | ChatGPT export source for memory as operational configuration, active idea buffer, Domain Tone Router, Cognitive Ascent Architecture, L0 constraints, and S-layer role. |
| `source-2026-05-25-pmv-action-symbols` | `external_reference` | source_verified / evidence_note / non_canon_case_check | `01_R_THEORY/SOURCES/2026-05-25_pmv_action_symbols_nature_source.md`; `01_R_THEORY/EVIDENCE/2026-05-25_pmv_action_symbols_evidence_note.md`; `01_R_THEORY/CASES/2026-05-26_action_symbol_archaeology_check.md` | Nature 2026 PMv action-symbols paper used as non-canon evidence for action-first abstraction and artifact-as-operation interpretation. Follow-up archaeology case check supports the architecture in a limited sense: Lomekwi proto-operation, Oldowan action-symbol threshold candidate, Acheulean action grammar/R2+ candidate, ochre/burial symbolic carrier layer. Does not prove full R3, language origin, or PMv as a general abstract-thought center. |
| `rtheory-2026-05-26-action-symbol-archaeology-check` | `repo_artifact` | non_canon_case_check / archaeology_probe | `01_R_THEORY/CASES/2026-05-26_action_symbol_archaeology_check.md` | Unique source ID for the archaeology case-check artifact derived from `source-2026-05-25-pmv-action-symbols`; added to remove duplicate source_id lint while preserving the PMv source anchor. |
| `rtheory-2026-05-27-lomekwi-proto-operation` | `external_reference` | source_verified_for_proto_operation | `01_R_THEORY/SOURCES/2026-05-27_lomekwi_proto_operation_source_card.md` | Harmand et al. 2015 Nature source card for Lomekwi 3. Supports Lomekwi as proto-operation / R1+ to R2- lower bound, not an established action-symbol grammar. |
| `rtheory-2026-05-27-oldowan-action-symbol-threshold` | `external_reference` | source_verified_for_action_symbol_threshold | `01_R_THEORY/SOURCES/2026-05-27_oldowan_action_symbol_threshold_source_card.md` | Science 2023 Nyayanga and Nature Communications 2025 Namorotukunan source card. Supports Oldowan as action-symbol threshold candidate: portable sharp-edge production category with partial recombination. |
| `rtheory-2026-05-27-acheulean-action-grammar` | `external_reference` | source_verified_for_action_grammar | `01_R_THEORY/SOURCES/2026-05-27_acheulean_action_grammar_source_card.md` | Lepre et al. 2011 Nature source card for Kokiselei 4 / early Acheulian. Supports Acheulean as action grammar / R2+ candidate, not R3 or symbolic meaning by itself. |
| `rtheory-2026-05-27-symbolic-carrier-ochre-burial` | `external_reference` | source_verified_for_symbolic_carrier_layer | `01_R_THEORY/SOURCES/2026-05-27_symbolic_carrier_ochre_burial_source_card.md` | Blombos Nature 2018 and Panga ya Saidi Nature 2021 source card. Supports ochre/graphic marks and burial as symbolic carrier layer, distinct from action-symbol origin. |
| `rtheory-2026-05-27-action-first-abstraction-readiness-check` | `repo_artifact` | keep_as_candidate_patch / not_ready_for_canon | `01_R_THEORY/PATCHES/2026-05-27_action_first_abstraction_readiness_check.md` | Canon-readiness check for the action-first abstraction chain. Result: not ready for canon because dedicated candidate patch and cross-link are missing; ready to become a candidate patch. |
| `rtheory-2026-05-27-action-first-abstraction-candidate-patch` | `repo_artifact` | candidate_patch / non-canon | `01_R_THEORY/PATCHES/2026-05-27_action_first_abstraction_candidate_patch.md` | Candidate patch adding a lower operation/action abstraction layer beneath the existing function/significance/symbol/concept layer. Does not update canon. |
| `crosslink-2026-05-27-action-first-abstraction` | `repo_artifact` | candidate_support / non-canon | `90_CROSS_LINKS/2026-05-27_action_first_abstraction_cross_links.md` | Cross-link note connecting action-first abstraction to R Theory, Culture as Externalized Instructions, PNA/action representation, archaeology, and symbol-to-concept path. |
| `rtheory-2026-05-27-action-first-abstraction-readiness-rerun` | `repo_artifact` | ready_for_canon_review_with_blockers | `01_R_THEORY/PATCHES/2026-05-27_action_first_abstraction_readiness_rerun.md` | Rerun of canon checklist after candidate patch and cross-link. Result: ready for canon review with blockers; comparison table and non-archaeological test remain required before acceptance. |
| `rtheory-2026-05-27-action-symbol-archaeology-comparison-table` | `repo_artifact` | candidate_support / blocker_closed | `01_R_THEORY/CASES/2026-05-27_action_symbol_archaeology_comparison_table.md` | Comparison table separating morphology, operational sequence, portability/category, grammar, transmission, and significance across Lomekwi, Oldowan, Acheulean, ochre/graphic marks, and burial-like contexts. |
| `rtheory-2026-05-27-child-motor-learning-action-abstraction-case` | `repo_artifact` | candidate_support / blocker_closed | `01_R_THEORY/CASES/2026-05-27_child_motor_learning_action_abstraction_case.md` | Non-archaeological case-anchor using child action learning / imitation to test whether action can be abstracted from concrete movement before language-level symbolism. |
| `culture-2026-05-25-myth-dynamic-instruction-network` | `chat_export` + `human_note` | active_hypothesis / non-canon | `03_CULTURE_AS_INSTRUCTIONS/SOURCES/2026-05-25_myth_dynamic_instruction_network_source_note.md`; `03_CULTURE_AS_INSTRUCTIONS/HYPOTHESES/2026-05-25_myth_as_dynamic_instruction_network.md` | User clarified mythologization as a dynamic external instruction network with temporary activation centers, agency compression, R1 mass-transmission compression, and R2/R3 infrastructure requirements. Non-canon; needs concrete textual/historical case test. |
| `culture-2026-05-26-mark-ending-hypergraph-test` | `external_reference` + `repo_artifact` | partial_source_verification / concrete_textual_stress_test / non-canon | `03_CULTURE_AS_INSTRUCTIONS/SOURCES/2026-05-26_mark_ending_textual_source_note.md`; `03_CULTURE_AS_INSTRUCTIONS/CASES/2026-05-26_mark_ending_hypergraph_test.md` | Concrete stress-test for hypergraph modeling on Mark 16:8 and the longer ending tradition. Uses only cautious textual premises; does not make historical, theological, or canon claims. |
| `theory-2026-05-26-soteriological-ritual-accumulation` | `chat_export` + `human_note` | active_hypothesis / non-canon | `07_SOTERIOLOGICAL_RITUAL_ACCUMULATION/SOURCES/2026-05-26_soteriological_ritual_accumulation_source_note.md`; `07_SOTERIOLOGICAL_RITUAL_ACCUMULATION/HYPOTHESES/2026-05-26_soteriological_ritual_accumulation.md` | User formulated a mechanism where salvation-oriented faith under opaque causality accumulates rituals, icons, saints, prayers, and helper practices because each may be a possible channel of help or salvation. Non-canon; needs comparative source-backed testing. |
| `theory-2026-05-28-m5-chat-export` | `chat_export` | needs_source | `06_BOUNDARY_SATURATION/SOURCES/2026-05-28_m5_chat_export_source_note.md` | ChatGPT M5 Theory export source; provenance for Boundary Saturation/M5 migration draft, not external physics evidence. |

## Rule

Every durable theory source should get a source ID before it updates a theory
page. If an idea is speculative, mark it as draft, hypothesis, evidence, or
candidate rather than canon.
