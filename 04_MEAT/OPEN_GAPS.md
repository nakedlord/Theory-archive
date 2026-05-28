# MEAT Open Gaps

## 2026-05-28 Update

CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-meat-pna-mccr-export-batch-3.md`
Source reference: `meat-2026-05-28-meat-pna-mccr-export`

MCCR source discovery is now complete. The gap is no longer `find the source`;
the remaining gap is review and classification.

Current MCCR status:

```text
source_found / recovery_draft / needs_review / not canon
```

Remaining questions:

- Should MCCR stay inside MEAT as a submodule?
- Should it become a cross-theory bridge between MEAT, PNA, R Theory, and
  artifact history?
- Does it need a separate module?
- Should it remain an archive node after source recovery?

Статус: active gap list
Дата: 2026-04-25

## Назначение

Этот файл фиксирует открытые пробелы миграции MEAT.

Пробел — это участок, который уже перенесён частично или известен из памяти, но ещё не закрыт структурно, источниково или статусно.

---

## 1. Canon gaps

### 1.1 CANON.md фиксирует v0.2, но не весь meat_full

Статус:

```text
needs review
```

Проблема:

`CANON.md` содержит базовую качественную модель и метрики, но `meat_full.md` шире: там есть синтез мемов, мутации, MEAT/EAT distinction, MCCR placeholder и связи с R/Culture.

Нужно:

- создать `CANON_REVIEW.md`;
- не расширять canon автоматически;
- оставить MEAT v0.2 качественной моделью до source/case verification.

---

## 2. MCCR gap

### 2.1 MCCR не восстановлен

Статус:

```text
recovery draft / needs source
```

Файл:

```text
VERSIONS/mccr_recovery_draft.md
```

Нужно:

- найти исходный чат MEAT/PNA/MCCR;
- восстановить расшифровку MCCR;
- решить, MCCR является частью MEAT, отдельным модулем или archive node.

До восстановления:

```text
do not use MCCR for conclusions
```

---

## 3. Case gaps

### 3.1 Нет CASE_INDEX

Статус:

```text
missing file
```

Нужный файл:

```text
CASES/CASE_INDEX.md
```

Должен покрыть:

- mythologized person;
- political slogan;
- meme synthesis;
- ritual;
- cultural archetype;
- concrete meme synthesis examples.

### 3.2 Concrete cases всё ещё типологические

Статус:

```text
migration drafts / need concrete source cases
```

Нужно:

- выбрать конкретный ритуал;
- выбрать конкретный архетип;
- выбрать конкретный политический лозунг;
- выбрать конкретный меметический синтез;
- проверить метрики на реальных материалах.

---

## 4. Metric gaps

### 4.1 Метрики качественные, не числовые

Статус:

```text
active qualitative metrics / not mathematical
```

Метрики:

- сила сцепления;
- частота совместной передачи;
- устойчивость комплекса;
- стоимость передачи;
- мутационная пластичность.

Нужно позже:

- определить шкалы weak / medium / strong;
- не делать числовую модель без данных;
- проверить на нескольких concrete cases.

---

## 5. Source verification gaps

### 5.1 Нет SOURCE_VERIFICATION_PLAN

Статус:

```text
optional but useful
```

Нужный будущий файл:

```text
SOURCE_VERIFICATION_PLAN.md
```

Группы источников:

- memetics;
- cultural transmission;
- social memory;
- ritual studies;
- political communication;
- archetype / narrative studies;
- network theory as analogy.

---

## 6. Cross-link gaps

### 6.1 Нет локального CROSS_LINKS.md

Статус:

```text
optional
```

Связи уже есть в `90_CROSS_LINKS`.

Но локальный файл может помочь позже:

- MEAT ↔ Culture;
- MEAT ↔ R Theory;
- MEAT ↔ EAT separation;
- MEAT ↔ PNA only if source exists;
- MEAT ↔ business/marketing as applied cases.

---

## 7. Conceptual distinction gaps

### 7.1 Мем / инструкция / понятие / символ

Статус:

```text
needs distinction map eventually
```

MEAT зависит от различия между:

- мем;
- инструкция;
- символ;
- понятие;
- ритуал;
- архетип;
- институт.

Часть различий относится к Culture and R Theory.

Не обязательно для migration closure, но важно для будущего развития.

---

## 8. Highest priority gaps

Закрывать сейчас:

1. `CANON_REVIEW.md`
2. `CASES/CASE_INDEX.md`
3. `MIGRATION_CLOSURE.md`

Не закрывать сейчас:

- числовую формализацию метрик;
- MCCR reconstruction without source;
- source cards;
- локальный cross-links file;
- distinction map.

## Current MEAT migration status

```text
broad migration done / structural closure pending / MCCR source missing
```
