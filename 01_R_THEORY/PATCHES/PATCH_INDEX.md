# R Theory Patch Index

Статус: active patch index
Дата: 2026-04-25

## Назначение

Этот файл индексирует все патчи и patch-like modules внутри R-теории.

Цель — видеть:

- какие изменения уже приняты в канон;
- какие являются candidate;
- какие являются migration draft;
- какие требуют источниковой сверки;
- какие кейсы и evidence связаны с каждым патчем.

---

## 1. `2026-04-25_symbol_to_concept.md`

### Статус

```text
accepted into active canon v3.2
```

### Суть

Патч добавляет различение символа и понятия.

Ключевая формула:

```text
функция -> значимость -> символ -> переносимое различение -> понятие
```

Символ фиксирует значимость.

Понятие фиксирует переносимое различение.

Понятие можно читать как сжатую инструкцию различения.

### Связанные файлы

- `../CANON.md`
- `../VERSIONS/v3.2.md`
- `../CASES/ochre_symbol_to_concept.md`
- `../CASES/fire_symbol_to_concept.md`
- `../CASES/burial_symbol_to_concept.md`
- `../../90_CROSS_LINKS/R_THEORY__CULTURE_AS_INSTRUCTIONS__SYMBOL_TO_CONCEPT.md`

### Что проверено

- охра;
- огонь;
- погребение;
- связь с Culture as Instructions.

### Ограничения

Патч не доказывает, что любой символ является понятием.

Нужно различать:

```text
значимость != символ != понятие
```

---

## 2. `2026-04-25_shadows_of_R3.md`

### Статус

```text
candidate
```

### Суть

Тени R3 — формы стабилизации поведения в зоне неопределённости, где прозрачная причинная модель недоступна.

Рабочая формула:

```text
неопределённость -> невозможность вывести причину -> повторяемое действие -> символическая стабилизация -> тень R3
```

### Связанные файлы

- `../CASES/shadows_of_R3_burial_case.md`
- `../CASES/shadows_of_R3_taboo_luck_case.md`
- `../ARCHAEOLOGY/death_symbolism.md`
- `../CASES/burial_symbol_to_concept.md`

### Что проверено

- погребение;
- табу / ритуалы удачи;
- смерть как зона неопределённости.

### Что ещё нужно проверить

- охра как тень R3;
- ранние магические действия;
- детские ритуализированные действия при тревоге;
- конкретные археологические кейсы.

### Решение на сейчас

```text
keep as candidate
```

Не переносить в canon до checklist и дополнительных проверок.

---

## 3. `q_r3_system.md`

### Статус

```text
migration draft / needs verification
```

### Суть

Q-R3 — question-driven recursive thinking system.

Главная функция: удерживать проблемное напряжение вопросами и не закрывать его преждевременным ответом.

Ключевые модули:

- Tension Buffer;
- Question Generator;
- Bad Question Filter;
- Answer Suppression Gate;
- Meta-Question Graph.

Метрики:

- QSI;
- RDR;
- TPC.

Типы вопросов:

- REFINE;
- SHIFT;
- META-SHIFT.

### Связанные файлы

- `../../02_SYNTAX/VERSIONS/runtime_pipeline_full.md`
- `../../02_SYNTAX/VERSIONS/validation_layer_full.md`
- `../../02_SYNTAX/VERSIONS/error_architecture_full.md`

### Что нужно

- сверить с исходным Q-R3 v1.0;
- решить, Q-R3 является частью R Theory или SynTax auxiliary module;
- не переносить в `CANON.md` до сверки.

### Решение на сейчас

```text
keep as migration draft / needs verification
```

---

## 4. `recursive_choice_decoherence.md`

### Статус

```text
migration draft / needs verification
```

### Суть

Модель описывает стабилизацию выбора внутри ΔT через конкурирующие операторы.

Декогеренция используется как формальная аналогия, а не как утверждение о квантовой природе мозга.

Рабочая формула:

```text
альтернативы -> конкурирующие операторы -> усиление одного пути -> стабилизация решения
```

### Связанные файлы

- `../VERSIONS/v3.1_full.md`
- `../../05_PNA/VERSIONS/pna_full.md`
- `../../05_PNA/VERSIONS/r3_modes_pna.md`

### Что нужно

- сверить с исходным чатом;
- отделить модель выбора от физической аналогии;
- решить, нужна ли отдельная версия или оставить как patch-like migration module.

### Решение на сейчас

```text
keep as migration draft / needs verification
```

---

## 5. Общая карта статусов

| Файл | Статус | Canon? | Нужно действие |
|---|---|---:|---|
| `2026-04-25_symbol_to_concept.md` | accepted into v3.2 | yes | source/case enrichment later |
| `2026-04-25_shadows_of_R3.md` | candidate | no | more cases + checklist |
| `q_r3_system.md` | migration draft | no | source verification |
| `recursive_choice_decoherence.md` | migration draft | no | source verification / analogy separation |

---

## 6. Следующие действия по патчам

1. Не менять `CANON.md`.
2. Создать `VERSION_COMPARISON_v3.1_v3.2.md`.
3. Создать `CASES/CASE_INDEX.md`.
4. Для `shadows_of_R3` пройти candidate checklist позже.
5. Для Q-R3 и decoherence найти исходные чаты или конспекты.

## Текущий статус patch block

```text
indexed / not closed / source verification required
```

---

## 7. `2026-05-28_r3_modes_instruction_runtime_candidate_patch.md`

CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-rtheory-export-batch-4.md`

### Status

```text
candidate_patch / source-backed by chat export / not canon
```

### Source IDs

- `rtheory-2026-05-28-recursive-choice-symbolic-rupture-export`
- `rtheory-2026-05-28-r3-1-3-export`
- `rtheory-2026-05-28-rtheory-structuration-export`

### Summary

The patch preserves the R3.1/R3.2/R3.3 operating-mode split, the motivational
field correction, instruction runtime, Q-R3 and recursive-choice/decoherence
source anchors, and the boundary that R4 is not accepted as a default next
operator.

### Related files

- `../SOURCES/2026-05-28_recursive_choice_symbolic_rupture_chat_export_source_note.md`
- `../SOURCES/2026-05-28_r3_1_3_chat_export_source_note.md`
- `../SOURCES/2026-05-28_rtheory_structuration_chat_export_source_note.md`
- `../../90_CROSS_LINKS/2026-05-28_rtheory_instruction_runtime_cross_links.md`

### Current decision

```text
keep as candidate patch; do not update CANON.md before review
```

### Review update 2026-05-28

Review file:

- `2026-05-28_r3_modes_instruction_runtime_review.md`

Review decision:

```text
split before canon movement
R3 modes -> canon-review candidate / not canon
instruction runtime -> cross-route split required
Q-R3 -> auxiliary SynTax/R Theory cross-link
decoherence -> formal analogy only
R4 -> guardrail candidate, not new default operator
```
