# Culture as Externalized Instructions Open Gaps

Статус: active gap list
Дата: 2026-04-25

## Назначение

Этот файл фиксирует открытые пробелы миграции Culture as Externalized Instructions.

Пробел — это участок, который уже перенесён частично или известен из памяти, но ещё не закрыт структурно, источниково или статусно.

---

## 1. Canon gaps

### 1.1 CANON.md компактный и не отражает весь instruction_network_full

Статус:

```text
needs review
```

Проблема:

`CANON.md` фиксирует v1.1, но полный migration draft шире: там есть сеть инструкций, веса передачи, неудобные детали, носители, мифологизация и историческая личность.

Нужно:

- создать `CANON_REVIEW.md`;
- не расширять canon автоматически;
- решить, какие короткие формулы оставить active canon.

---

## 2. Case gaps

### 2.1 Нет CASE_INDEX

Статус:

```text
missing file
```

Нужный файл:

```text
CASES/CASE_INDEX.md
```

Индекс должен покрыть:

- historical person;
- religious founder;
- New Testament;
- Mark Gospel;
- Passion narrative;
- contradictions / instruction layers;
- historical rollback;
- inconvenient details;
- text / ritual / institution carriers;
- institution formation.

### 2.2 New Testament cases требуют textual verification

Статус:

```text
migration drafts / needs textual verification
```

Нужно:

- не использовать как исторический вывод;
- отделять исторического Иисуса, текстовый образ, богословский слой, мифологический узел и инструктивную функцию;
- создать detailed episode index, если продолжать.

### 2.3 Нет detailed Mark episode reads

Статус:

```text
not transferred / optional until source pass
```

Нужный будущий файл:

```text
CASES/detailed_mark_episode_index.md
```

---

## 3. Source verification gaps

### 3.1 Нет SOURCE_VERIFICATION_PLAN

Статус:

```text
missing file
```

Нужный файл:

```text
SOURCE_VERIFICATION_PLAN.md
```

Группы источников:

- myth theory;
- cultural transmission;
- ritual studies;
- memory and oral tradition;
- New Testament textual studies;
- historical Jesus studies;
- institution formation;
- anthropology of taboo and ritual.

### 3.2 Нет textual source cards

Статус:

```text
missing / future pass
```

Возможные будущие файлы:

```text
SOURCES/mark_gospel_sources.md
SOURCES/new_testament_textual_sources.md
SOURCES/ritual_institution_sources.md
```

---

## 4. Layer separation gaps

### 4.1 Исторический / текстовый / богословский / инструктивный слой

Статус:

```text
needs explicit discipline
```

Нужно всегда различать:

- исторический агент;
- текстовый образ;
- богословскую интерпретацию;
- мифологизированный культурный узел;
- инструктивную функцию текста;
- институциональную функцию.

Без этого New Testament case может стать слишком сильным и нечистым.

---

## 5. Patch gaps

### 5.1 Нет PATCH_INDEX

Статус:

```text
optional / useful
```

Сейчас есть один главный патч:

```text
PATCHES/2026-04-25_mythologization_as_instruction_network.md
```

Он уже принят в v1.1.

Можно создать patch index позже или включить в migration closure.

---

## 6. Cross-link gaps

### 6.1 Нет локального CROSS_LINKS.md

Статус:

```text
optional / useful
```

Связи уже есть в `90_CROSS_LINKS`, но для закрытия модуля можно создать:

```text
CROSS_LINKS.md
```

Нужно отразить:

- Culture ↔ R Theory;
- Culture ↔ MEAT;
- Culture ↔ SynTax;
- Culture ↔ business/pedagogy only as applied cases;
- Culture ↔ New Testament as textual case.

---

## 7. Remaining conceptual gaps

### 7.1 Инструкция / мем / понятие / символ

Статус:

```text
needs distinction map
```

Нужно позже явно различить:

- инструкция;
- мем;
- понятие;
- символ;
- ритуал;
- институт.

Не обязательно для migration closure, но важно для развития.

### 7.2 Вес передачи

Статус:

```text
conceptual but not formalized
```

Есть идея веса передачи, но нет отдельной метрики внутри Culture module.

Часть этой задачи связана с MEAT.

---

## 8. Highest priority gaps

Закрывать сейчас:

1. `CANON_REVIEW.md`
2. `CASES/CASE_INDEX.md`
3. `SOURCE_VERIFICATION_PLAN.md`
4. `MIGRATION_CLOSURE.md`

Можно пропустить сейчас:

- detailed Mark episode reads;
- textual source cards;
- patch index;
- local cross-links;
- distinction map instruction/meme/symbol/concept.

## Current Culture migration status

```text
broad migration done / structural closure pending / textual verification required
```

---

## 9. Instruction packet runtime route

CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-instruction-runtime-route-split.md`

Status:

```text
candidate_patch_created / non_canon
```

Artifact:

- `PATCHES/2026-05-28_instruction_packet_runtime_candidate.md`

Open:

- test instruction packet/runtime on a concrete Culture case;
- compare against meme/symbol/concept/ritual distinction maps;
- add external sources before canon review.
