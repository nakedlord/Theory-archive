# SynTax Open Gaps

Статус: active gap list
Дата: 2026-04-25

## Назначение

Этот файл фиксирует открытые пробелы миграции SynTax.

Пробел — это участок, который уже перенесён частично или известен из памяти, но ещё не закрыт структурно, источниково или статусно.

---

## 1. Canon gaps

### 1.1 Compact CANON.md не отражает всю архитектуру

Статус:

```text
needs review
```

Проблема:

`CANON.md` хранит компактное ядро, но не ясно, какие элементы из перенесённых full drafts должны быть active canon, а какие остаются migration drafts.

Нужно:

- создать `CANON_REVIEW.md`;
- не расширять `CANON.md` автоматически;
- отделить active infrastructure от historical/migration material.

---

## 2. Patch gaps

### 2.1 Нет PATCH_INDEX

Статус:

```text
missing file
```

Нужный файл:

```text
PATCHES/PATCH_INDEX.md
```

Нужно проиндексировать:

- v1.9 Infrastructure Split;
- v2.6 Context Arbitration;
- v2.8 E11 Context Lock-In;
- v3.0 Progress Delta;
- v3.3 Canon Aging;
- v3.5 Exploration Budget;
- v3.6 Module Independence;
- v3.7 Error Recurrence Counter;
- v4.3 Drift Detection;
- v4.6 Complexity Governance;
- v4.9 Operator Registry.

---

## 3. Source verification gaps

### 3.1 Нет сверки с исходным SynTax-чатом

Статус:

```text
needs source
```

Почти все full drafts перенесены из памяти.

Нужно сверить с исходными чатами или конспектами:

- SynTax Companion Architecture v1.0;
- Goal Module;
- runtime pipeline;
- validation layer;
- error architecture;
- patch line v1.9–v4.9.

---

## 4. Runtime gaps

### 4.1 Runtime pipeline перенесён, но не принят как canonical runtime spec

Статус:

```text
migration draft / needs review
```

Файл:

- `VERSIONS/runtime_pipeline_full.md`

Нужно решить:

- должен ли pipeline быть в `CANON.md`;
- какую короткую форму использовать;
- как связать pipeline с Migration Mode.

---

## 5. Validation gaps

### 5.1 Validation layer перенесён, но не стабилизирован как checklist

Статус:

```text
migration draft / needs process extraction
```

Файл:

- `VERSIONS/validation_layer_full.md`

Нужно возможно вынести практические checklist-файлы:

- migration validation checklist;
- canon update validation checklist;
- evidence validation checklist.

Пока не создавать без необходимости, чтобы не раздуть архитектуру.

---

## 6. Error architecture gaps

### 6.1 Early error classes восстановлены неполно

Статус:

```text
recovery draft / needs source
```

Файл:

- `VERSIONS/early_error_classes_archive.md`

Нужно:

- сверить с ранним SynTax-чатом;
- понять, какие error classes active;
- не дублируют ли они later mechanisms.

### 6.2 Нет единого Error Index

Статус:

```text
optional / not urgent
```

Можно создать позже, если error architecture станет активно использоваться.

---

## 7. Operator gaps

### 7.1 Operator Registry перенесён, но реестр конкретных операторов не создан

Статус:

```text
partial
```

Файл:

- `VERSIONS/operator_registry_full.md`

Не хватает:

- списка core operators;
- паспортов операторов;
- overlap map.

Решение:

Не создавать полный operator registry сейчас, пока идёт миграция. Это отдельный будущий pass.

---

## 8. Drift / complexity gaps

### 8.1 Drift Protocol перенесён, но нет реальных drift passports

Статус:

```text
migration draft / no cases yet
```

### 8.2 Complexity Passport перенесён, но не применяется как отдельный файл

Статус:

```text
migration draft / principle active
```

Решение:

Использовать как правило, но не плодить complexity passports без необходимости.

---

## 9. Portable / activation gaps

### 9.1 Portable Syntax.md не сверен с исходной версией

Статус:

```text
migration draft / needs verification
```

### 9.2 Activation prompt archived intentionally

Статус:

```text
archived / prompt not reproduced
```

Решение:

Не восстанавливать скрытый prompt без явной причины. Portable spec лучше скрытой фразы.

---

## 10. Goal Module gaps

### 10.1 Нет шаблонов Goal Card / Session Link как отдельных файлов

Статус:

```text
optional
```

Файл `GOAL_MODULE.md` уже содержит поля.

Можно создать templates позже, если понадобится практическое применение.

---

## 11. Highest priority gaps

Закрывать сейчас:

1. `CANON_REVIEW.md`
2. `PATCHES/PATCH_INDEX.md`
3. `MIGRATION_CLOSURE.md`

Не закрывать сейчас:

- полный реестр операторов;
- source verification по всем чатом;
- новые templates;
- новые protocols.

## Current SynTax migration status

```text
broad migration done / structural closure pending
```

---

## 12. Q-R3 route from R Theory export

CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-instruction-runtime-route-split.md`

Status:

```text
operator_candidate_created / non_canon
```

Artifact:

- `OPERATORS/q_r3_tension_preservation_operator_candidate.md`

Open:

- compare Q-R3 with existing operators before registry promotion;
- test answer suppression and question generation on a concrete theory case;
- decide whether Q-R3 remains a note, becomes a patch, or enters a later
  operator registry.
