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
CLOSED 2026-07-07 — файл существует (PATCHES/PATCH_INDEX.md), индексирует v1.9..v5.3.
Пробел оставался в списке после закрытия: наблюдаемый случай слепоты модуля к собственному состоянию.
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

Все три структурных пробела закрыты (CANON_REVIEW, PATCH_INDEX, MIGRATION_CLOSURE существуют).

Текущий приоритет сместился на эпистемические — см. раздел 11b:

1. Внешний якорь runtime (11b.1) — critical
2. Governance/runtime drift detection (11b.2)
3. Теория «защита vs генерация» (11b.3)

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

## 11b. Эпистемические пробелы (добавлено 2026-07-07, патч v5.3)

Ранее OPEN_GAPS содержал 11 разделов, **все структурные** (нет файла, нет индекса, нет сверки). Ни одного о том, где архитектура даёт ложные результаты. У R-Theory есть `ARCHAEOLOGY/archaeology_falsification_map`; у SynTax не было error log СЕБЯ.

### 11b.1 Внешний якорь runtime отсутствует

Статус:

```text
open / critical
```

Симуляционная эмпирика (`ERROR_LOG.md`, 24/70/72 прогона) прогонялась агентом **внутри** SynTax. Это не внешний якорь. Настоящий якорь — задачи, чей исход определяется вне протокола: код прошёл тесты; рекомендация сработала в GYMKiDs; предсказание подтвердилось литературой.

Без якоря runtime неотличим от самосогласованной догмы.

### 11b.2 Governance/runtime рассинхрон не детектируется

Статус:

```text
open
```

Патч v5.2 (Gᴀ/Gᴛ) active с 2026-06-16, но отсутствует в `RUNTIME_SPEC.md`. Агент, работающий по runtime, оценивает идеи одной осью. `v4.3 Drift Detection Protocol` мониторит канон, но не runtime, и дрейф не поймал.

Нужно: расширить drift detection на runtime-слой.

### 11b.3 Защита систематически душит генерацию

Статус:

```text
observed / needs theory
```

Из `ERROR_LOG.md`: M1, M4, M6, L2 — все четыре пришлось выключить или ослабить именно на Design/Расходящихся. Это не частные баги, а причина сдвига v4.0→v5.0.

Обобщение (кандидат в теорию протоколов): механизм, полезный на Critique, вероятно вреден на Design. Часть защит требует **инверсии по знаку** (M7), а не выключения. Бинарное вкл/выкл — недостаточная модель управления механизмом.

### 11b.4 Рефлексивность как риск самооправдания

Статус:

```text
open
```

Патч v5.3 признаёт SynTax рефлексивной теорией. Риск: «рефлексивность» станет щитом, отражающим любую критику как «суждение изнутри рамки». Защита: механизмы остаются под Gᴛ, фальсифицируемы поштучно; ядро — под Gᴀ через progress delta (v3.0).

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
