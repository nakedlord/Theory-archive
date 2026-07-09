# SynTax Coverage

```text
layer: governance  (как ведётся архив; нумерация v1.9..v5.x)
```

Статус: migration coverage map
Дата: 2026-04-25

## Назначение

Этот файл показывает, что по SynTax уже перенесено в GitHub, что перенесено частично, что требует сверки с исходными чатами и что ещё остаётся открытым.

Главное правило:

```text
SynTax is infrastructure, not object theory
```

SynTax управляет миграцией, каноном, патчами, ошибками, целями и статусами, но не должен подменять содержание отдельных теорий.

---

## 1. Current module status

### Статус

```text
active infrastructure / migration mostly transferred
```

### Основные файлы

- `CANON.md`
- `STATUS.md`
- `WORKSPACE.md`
- `SYNC_LOG.md`
- `GOAL_MODULE.md`

### Что покрыто

- роль SynTax как инфраструктуры;
- Goal Module;
- patch history;
- runtime pipeline;
- validation;
- error architecture;
- operator registry;
- drift detection;
- complexity governance;
- portable syntax profile;
- activation prompt archive.

---

## 2. Canon and status files

### Уже перенесено

- `CANON.md`
- `STATUS.md`

### Статус

```text
active infrastructure / compact canon
```

### Проблема

`CANON.md` пока компактный и не отражает всей глубины перенесённых версий и патчей.

### Решение

Не расширять `CANON.md` автоматически. Сначала использовать `CANON_REVIEW.md`.

---

## 3. SynTax Companion Architecture

### Уже перенесено

- `VERSIONS/syntax_companion_architecture_v1.md`

### Статус

```text
migration draft / needs verification
```

### Что покрыто

- Pure Engine;
- Agent Shell;
- Autonomous Idea Pressure Loop;
- Idea Bank;
- You-Model + Style Policy;
- Status Protocol;
- SYNC Cycle;
- canon discipline;
- portable version idea.

### Что нужно

- сверить с исходным SynTax-чатом;
- решить, что должно быть active canon, а что historical architecture note.

---

## 4. Goal Module

### Уже перенесено

- `GOAL_MODULE.md`

### Статус

```text
active architecture component / migration draft needs verification
```

### Что покрыто

- Goal Module = Memory of Direction;
- G0/G1/G2/G3;
- Goal Card;
- Session Link;
- Goal State;
- статусы целей;
- правила значимых рабочих диалогов.

### Что нужно

- сверить с исходным чатом;
- возможно вынести Goal Card template отдельно.

---

## 5. Runtime / Validation / Error Architecture

### Уже перенесено

- `VERSIONS/runtime_pipeline_full.md`
- `VERSIONS/validation_layer_full.md`
- `VERSIONS/error_architecture_full.md`

### Статус

```text
migration drafts / needs verification
```

### Что покрыто

- input -> interpretation -> goal -> routing -> context arbitration -> operators -> validation -> response -> sync;
- level separation;
- grounding check;
- status check;
- context discipline;
- progress delta;
- complexity check;
- E11, false depth, premature synthesis, abstraction inflation, canon pollution, weak grounding, drift, ERC.

---

## 6. Operator / Drift / Complexity

### Уже перенесено

- `VERSIONS/operator_registry_full.md`
- `VERSIONS/drift_protocol_full.md`
- `VERSIONS/complexity_passport_full.md`

### Статус

```text
migration drafts / needs verification
```

### Что покрыто

- operator passport;
- operator statuses;
- overlap check;
- drift types;
- drift passport;
- severity levels;
- complexity cost/gain;
- complexity passport;
- rejection of costly ideas.

---

## 7. Portable and activation files

### Уже перенесено

- `VERSIONS/portable_syntax_md.md`
- `VERSIONS/activation_prompt_archive.md`

### Статусы

```text
portable_syntax_md -> migration draft / portable profile
activation_prompt_archive -> archived / prompt not reproduced
```

### Решение

Скрытый activation prompt не воспроизводить как активную инструкцию.

Portable Syntax должен быть понятным и аудируемым.

---

## 8. Patch history

### Уже перенесено

- `PATCHES/README.md`
- `PATCHES/v1.9_infrastructure_split.md`
- `PATCHES/v2.6_context_arbitration_step.md`
- `PATCHES/v2.8_error_E11_context_lock_in.md`
- `PATCHES/v3.0_progress_delta_check.md`
- `PATCHES/v3.3_canon_aging.md`
- `PATCHES/v3.5_exploration_budget.md`
- `PATCHES/v3.6_module_independence.md`
- `PATCHES/v3.7_error_recurrence_counter.md`
- `PATCHES/v4.3_drift_detection_protocol.md`
- `PATCHES/v4.6_complexity_governance_rule.md`
- `PATCHES/v4.9_operator_registry_protocol.md`

### Статус

```text
key patch line transferred / needs source verification
```

### Что нужно

- `PATCHES/PATCH_INDEX.md`;
- проверить, не пропущены ранние error classes и intermediate patches;
- сверить патчи с исходным SynTax-чатом.

---

## 9. Early error classes

### Уже перенесено

- `VERSIONS/early_error_classes_archive.md`

### Статус

```text
recovery draft / needs source verification
```

### Что покрыто

- Level Mixing;
- Premature Synthesis;
- False Depth;
- Abstraction Inflation;
- Weak Grounding;
- Theory Overreach;
- Canon Pollution;
- User-Mirroring Distortion;
- Response Bloat.

### Что нужно

- сверить с ранней Error Architecture;
- решить, какие классы active, а какие archived.

---

## 10. External meta files relevant to SynTax

### Уже есть в `00_META`

- `MIGRATION_MODE.md`
- `MIGRATION_STATUS_RULES.md`
- `CANDIDATE_TO_CANON_CHECKLIST.md`
- `IMPORT_BACKLOG.md`
- `FIELD_MAP.md`
- `COVERAGE_AUDIT_2026-04-25.md`
- `DEVELOPMENT_PLAN.md`

### Статус

```text
active process layer
```

### Важно

Эти файлы являются operational infrastructure для всего архива, а не только для SynTax.

---

## 11. Coverage summary

### Сильные зоны

- patch line v1.9–v4.9 перенесена;
- runtime pipeline перенесён;
- validation layer перенесён;
- error architecture перенесена;
- Goal Module перенесён;
- portable profile создан;
- migration/status discipline уже работает.

### Слабые зоны

- нет `PATCHES/PATCH_INDEX.md`;
- нет `OPEN_GAPS.md`;
- нет `CANON_REVIEW.md`;
- нет `MIGRATION_CLOSURE.md`;
- нет сверки с исходным SynTax-чатом;
- early error classes восстановлены не полностью;
- activation prompt не воспроизведён и намеренно archived.

## Current SynTax migration status

```text
broadly migrated / structurally not closed / source verification required
```
