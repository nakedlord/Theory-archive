# Theory Archive Source Registry

Status: active registry
Date: 2026-05-19
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

## Rule

Every durable theory source should get a source ID before it updates a theory
page. If an idea is speculative, mark it as draft, hypothesis, evidence, or
candidate rather than canon.
