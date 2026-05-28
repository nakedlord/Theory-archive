# Boundary Saturation Open Gaps

Статус: active gap list
Дата: 2026-04-25

## Назначение

Этот файл фиксирует открытые пробелы миграции Boundary Saturation.

Boundary Saturation остаётся speculative formal model. Пробелы здесь особенно важны, потому что физические утверждения требуют более строгой проверки, чем культурные или архитектурные модели.

---

## 1. Physical status gap

### 1.1 Модель не является установленной физикой

Статус:

```text
speculative formal model
```

Проблема:

Boundary Saturation легко звучит как новая теория чёрных дыр, хотя сейчас это только интерпретационный и формальный черновик.

Решение:

```text
do not claim replacement of GR or proof of new black hole physics
```

---

## 2. Dimension gaps

### 2.1 `C_b` and `I_dot` not physically defined

Статус:

```text
open formal gap
```

Файл:

- `FORMAL_MODEL/dimension_check_Cb_Idot.md`

Проблема:

Условие:

```text
I_dot >= C_b
```

не имеет физического смысла, пока не определены размерности.

Нужно определить, что течёт через границу:

- энергия;
- информация;
- корреляции;
- entropy rate;
- causal influence.

---

## 3. Compactness relation gap

### 3.1 Boundary load не выведен из compactness

Статус:

```text
open formal gap
```

Есть физический anchor:

```text
chi = 2GE / (c^4 R)
```

Но нет вывода, связывающего `C_b`, `I_dot`, `lambda`, `rho_Z` с `chi`.

---

## 4. Redshift-like gap

### 4.1 Redshift-like degradation is only analogy

Статус:

```text
speculative analogy
```

Файл:

- `FORMAL_MODEL/redshift_like_boundary_degradation.md`

Нельзя утверждать:

```text
Boundary Saturation derives gravitational redshift
```

Нужно проверить, можно ли связать `g(lambda)` с известным redshift factor.

---

## 5. Page-like gap

### 5.1 Page-like behavior is only candidate motif

Статус:

```text
candidate motif / not formalized
```

Файл:

- `FORMAL_MODEL/page_like_behavior.md`

Нельзя утверждать:

- Page curve;
- unitary evaporation;
- Hawking radiation mechanism;
- information recovery.

Нужно определить, что такое accessible correlation и как она меняется.

---

## 6. M5 old intuition gaps

### 6.1 Hot dense ball intuition is not current model

Статус:

```text
archived intuition inside migration draft
```

Файл:

- `VERSIONS/m5_black_hole_full_notes.md`

Проблема:

Старая интуиция “чёрная дыра как горячий плотный шар” сохранена, но не является текущей аккуратной формулировкой.

Текущая безопасная формулировка:

```text
black-hole-like regime as boundary-dominated accessibility near compactness threshold
```

---

## 7. Evaporation gap

### 7.1 Evaporation through universe expansion remains speculative intuition

Статус:

```text
speculative intuition / not integrated
```

Нельзя использовать как explanation of Hawking evaporation.

Нужно:

- formal relation;
- comparison with Hawking radiation;
- dimensional check;
- source verification.

---

## 8. Source verification gap

### 8.1 Нет SOURCE_VERIFICATION_PLAN

Статус:

```text
missing file / optional but important
```

Нужный будущий файл:

```text
SOURCE_VERIFICATION_PLAN.md
```

Группы источников:

- black hole compactness;
- Schwarzschild radius;
- holographic principle;
- black hole thermodynamics;
- Page curve;
- information paradox;
- gravitational redshift;
- scrambling.

---

## 9. Canon gap

### 9.1 CANON.md должен оставаться осторожным

Статус:

```text
needs review
```

Нужно создать:

```text
CANON_REVIEW.md
```

Цель:

- отделить active speculative core;
- old M5 intuitions;
- formal drafts;
- analogy files;
- non-predictions.

---

## 10. Highest priority gaps

Закрывать сейчас:

1. `CANON_REVIEW.md`
2. `MIGRATION_CLOSURE.md`

Можно не закрывать сейчас:

- full source verification;
- real formal derivation;
- `SOURCE_VERIFICATION_PLAN.md`;
- mathematical model;
- Page-like formalization.

## Current Boundary migration status

```text
broad migration done / speculative model hygiene good / physical verification open
```

---

## 2026-05-28 Source Provenance Update

Status: structural source gap partially addressed / external verification still open
CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-m5-export-source-provenance.md`

Added:

- `SOURCES/2026-05-28_m5_chat_export_source_note.md`
- `SOURCE_VERIFICATION_PLAN.md`

This resolves the missing-file part of the source verification gap. It does not
resolve the physics verification gap. The M5 chat export is now registered as
provenance for old intuitions and migration history, not as external evidence.
