# R Theory Open Gaps

Статус: active gap list
Дата: 2026-04-25

## Назначение

Этот файл фиксирует открытые пробелы миграции R-теории.

Пробел — это не новая задача развития, а участок, который уже был в наработках или логически необходим для закрытия миграции, но ещё не приведён в порядок.

---

## 1. Canon gaps

### 1.1 CANON.md слишком короткий относительно v3.1_full

Статус:

```text
needs review
```

Проблема:

`CANON.md` фиксирует v3.2, но не ясно, какие элементы из `v3.1_full.md` должны быть активным каноном, а какие остаются историческим/migration layer.

Нужно:

- создать `CANON_REVIEW.md`;
- сравнить `CANON.md`, `v3.1_full.md`, `v3.2.md`;
- решить, что оставить в коротком каноне.

---

## 2. Version gaps

### 2.1 Нет сравнения v3.1 и v3.2

Статус:

```text
missing file
```

Нужный файл:

```text
VERSIONS/VERSION_COMPARISON_v3.1_v3.2.md
```

Вопросы:

- что добавило v3.2;
- что осталось из v3.1;
- что стало archive/migration;
- что требует источника.

---

## 3. Patch gaps

### 3.1 Нет PATCH_INDEX

Статус:

```text
missing file
```

Нужный файл:

```text
PATCHES/PATCH_INDEX.md
```

Патчи:

- symbol_to_concept;
- shadows_of_R3;
- q_r3_system;
- recursive_choice_decoherence.

### 3.2 shadows_of_R3 ещё не принят в canon

Статус:

```text
candidate
```

Нужно:

- проверить на checklist;
- связать с кейсами;
- решить keep candidate / canon update / more cases.

### 3.3 Q-R3 требует сверки

Статус:

```text
migration draft / needs verification
```

Нужен исходный Q-R3 v1.0 или конспект.

### 3.4 Recursive choice/decoherence требует сверки

Статус:

```text
migration draft / needs verification
```

Нужно сверить с исходным чатом и отделить R-теорию от физической аналогии.

---

## 4. Archaeology gaps

### 4.1 Нет ARCHAEOLOGY_INDEX

Статус:

```text
missing file
```

Нужный файл:

```text
ARCHAEOLOGY/ARCHAEOLOGY_INDEX.md
```

### 4.2 Нет source verification plan по археологии

Статус:

```text
missing file
```

Нужный файл:

```text
ARCHAEOLOGY/SOURCE_VERIFICATION_PLAN.md
```

### 4.3 Большинство археологических файлов требует источников

Статус:

```text
needs source verification
```

Особенно:

- Lomekwi;
- Oldowan;
- Acheulean;
- late Acheulean;
- fire/camp/childhood;
- migration/cold pressure;
- death symbolism;
- sapiens/neanderthals;
- brain size steps.

### 4.4 Brain size steps — speculative

Статус:

```text
speculative migration draft
```

Нужно проверить данные и тайминг.

### 4.5 Sapiens / Neanderthals — needs source

Статус:

```text
hypothesis / needs source verification
```

Нужно не сводить различие только к сетям.

---

## 5. Evidence gaps

### 5.1 Нет EVIDENCE_INDEX

Статус:

```text
missing file
```

Нужный файл:

```text
EVIDENCE/EVIDENCE_INDEX.md
```

### 5.2 Нет SOURCE_STATUS

Статус:

```text
missing file
```

Нужный файл:

```text
EVIDENCE/SOURCE_STATUS.md
```

### 5.3 Evidence claims требуют маркировки

Нужно разделить:

- supported;
- contested;
- plausible;
- speculative;
- needs source.

---

## 6. Case gaps

### 6.1 Нет CASE_INDEX

Статус:

```text
missing file
```

Нужный файл:

```text
CASES/CASE_INDEX.md
```

### 6.2 Кейсы пока типологические

Статус:

```text
partial
```

Нужно добавить source verification или конкретные археологические привязки.

### 6.3 Нужны дополнительные кейсы для shadows_of_R3

Возможные:

- охра;
- ранняя магическая практика;
- табу;
- погребение с предметами;
- детские ритуализированные действия при тревоге.

---

## 7. Source gaps

### 7.1 Нет общего SOURCE_VERIFICATION_PLAN

Статус:

```text
missing file
```

Нужный файл:

```text
SOURCE_VERIFICATION_PLAN.md
```

### 7.2 Нет списка источников по группам

Нужны группы:

- archaeology;
- cognitive development;
- stress/metabolism;
- cultural transmission;
- demography;
- sapiens/neanderthals;
- brain size evolution;
- fire/camp;
- burial/ochre.

---

## 8. Cross-link gaps

### 8.1 Нет R-local cross-links file

Статус:

```text
missing file
```

Нужный файл:

```text
CROSS_LINKS.md
```

### 8.2 Нужно ограничить границы R Theory

R Theory связана с PNA, MEAT, Culture, SynTax.

Но не всё соседнее должно попадать в R Theory.

Особенно:

```text
Boundary Saturation should remain separate
```

---

## 9. Migration closure gaps

### 9.1 Нет MIGRATION_CLOSURE

Статус:

```text
missing file
```

Нужный файл:

```text
MIGRATION_CLOSURE.md
```

Создавать только после:

- coverage;
- open gaps;
- canon review;
- patch index;
- archaeology index;
- evidence index;
- case index;
- source verification plan.

---

## 10. Highest priority gaps

Закрывать в таком порядке:

1. `CANON_REVIEW.md`
2. `PATCHES/PATCH_INDEX.md`
3. `ARCHAEOLOGY/ARCHAEOLOGY_INDEX.md`
4. `EVIDENCE/EVIDENCE_INDEX.md`
5. `CASES/CASE_INDEX.md`
6. `SOURCE_VERIFICATION_PLAN.md`
7. `MIGRATION_CLOSURE.md`

## Текущий статус

```text
R Theory migration: broad transfer done, structural closure not done
```

---

## 11. Chat Export Batch 2026-05-28 Gaps

CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-rtheory-export-batch-4.md`

### 11.1 R3 modes now have source anchors

Status:

```text
source_found / candidate_patch / needs_review
```

Source notes:

- `SOURCES/2026-05-28_recursive_choice_symbolic_rupture_chat_export_source_note.md`
- `SOURCES/2026-05-28_r3_1_3_chat_export_source_note.md`

Needed:

- decide whether R3.1/R3.2/R3.3 become canon, version material, or remain a
  candidate patch;
- compare against `VERSIONS/v3.1_full.md` and `VERSIONS/v3.2.md`;
- decide whether the motivational field belongs in R Theory, PNA, or a
  cross-link.

### 11.2 Q-R3 and decoherence source gaps are narrowed, not closed

Status:

```text
source_anchor_found / still needs review
```

The export batch anchors `PATCHES/q_r3_system.md` and
`PATCHES/recursive_choice_decoherence.md`, but does not complete canon review.

### 11.3 Instruction runtime needs routing decision

Status:

```text
candidate / cross-route
```

Instruction runtime touches R Theory, Culture as Externalized Instructions,
SynTax operator architecture, and applied GYMKiDs/Fly Zone methodology. Future
work must choose the owning module before expanding it.

### 11.4 Review gate result

Status:

```text
review_completed / compact_r3_later_accepted / route_split_started
```

Review file:

- `PATCHES/2026-05-28_r3_modes_instruction_runtime_review.md`

Closed or narrowed:

- R3.1/R3.2/R3.3 are no longer unreviewed source leads; compact R3-A/B/C later
  entered canon.
- Q-R3 and recursive-choice/decoherence are source-anchored but still outside
  canon.
- R4 has a guardrail candidate: do not treat it as a default next R operator.

Still needed:

- optional external cognitive/source checks for R3 modes;
- human canon review for compact R3 is complete;
- separate route artifacts for instruction runtime, Q-R3, PNA motivational
  field, and GYMKiDs applied methodology.

### 11.5 R3 internal closure

Status:

```text
accepted_into_canon / compact_r3_modes
```

Closure packet:

- `PATCHES/2026-05-28_r3_modes_canon_compression_packet.md`

Closed:

- R3 core candidate is separated from instruction runtime.
- R3 modes have exact compact canon wording.
- R4 is excluded from the default R ladder.
- Q-R3 and decoherence remain outside R core canon.

Still open:

- optional external source cards for predictive control, error monitoring,
  cognitive control, retrospective reasoning, and mental simulation.
- separate route artifacts for instruction runtime, Q-R3, PNA motivational
  field, and GYMKiDs applied methodology.

### 11.6 R3 compact canon accepted

CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-r3-canon-acceptance.md`

Status:

```text
closed_for_r3_core / accepted_into_canon
```

Closed:

- compact R3 canon wording accepted;
- `CANON.md` updated;
- `VERSIONS/v3.3.md` created.

Still open outside R core:

- external cognitive source cards are useful but no longer block compact canon;
- instruction runtime now has route-specific artifacts, but they are non-canon;
- Q-R3 and motivational field have route artifacts but need tests/sources;
- decoherence remains a formal analogy only;
- GYMKiDs methodology remains a downstream KB import, not done in this pass.

### 11.7 Instruction runtime route split

CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-instruction-runtime-route-split.md`

Status:

```text
route_split_started / R_core_closed / non_canon_artifacts
```

Created:

- `PATCHES/2026-05-28_instruction_runtime_route_split.md`
- `../03_CULTURE_AS_INSTRUCTIONS/PATCHES/2026-05-28_instruction_packet_runtime_candidate.md`
- `../02_SYNTAX/OPERATORS/q_r3_tension_preservation_operator_candidate.md`
- `../05_PNA/HYPOTHESES/2026-05-28_motivational_field_r3_bridge.md`

Still open:

- Culture candidate needs concrete cases and external sources;
- Q-R3 needs operator tests against existing SynTax operators;
- motivational field needs PNA source verification;
- GYMKiDs / Fly Zone applied trainer methodology needs a separate KB import if
  pursued.

### 11.8 R2 future choice vs R3 irreversibility source note

CSP event: `projects/syntax/events/2026-05-31-codex-openai-export-second-pass-theory-audit.md`

Status:

```text
source_note_created / boundary_distinction / non_canon
```

Artifact:

- `SOURCES/2026-05-31_r2_future_choice_r3_irreversibility_source_note.md`

Open:

- compare the distinction against current R3-A/B/C canon;
- test cases where future simulation remains R2 because it only selects a local
  trajectory;
- test cases where irreversible choice rewrites the rule-space and may count as
  R3;
- avoid treating regret, responsibility, or existential language as sufficient
  proof of R3.
