# R Theory Canon Review

Статус: canon review draft
Дата: 2026-04-25

## Назначение

Этот файл проверяет, что сейчас действительно является каноном R-теории, а что является migration draft, candidate patch, case или evidence.

Файл не обновляет `CANON.md`.

---

## 1. Current active canon

Текущий активный канон:

```text
R Theory v3.2
```

Файлы:

- `CANON.md`
- `VERSIONS/v3.2.md`

---

## 2. Ядро active canon

В активном каноне находятся:

### R0

Реакция без окна выбора.

### R1

Единичная инструкция и выбор действия по ближайшему результату.

### R2

Цепочка действий и симуляция возможной траектории.

### R3

Анализ ошибки второго порядка и изменение правила генерации поведения.

### ΔT

Окно выбора, удержания альтернатив и стабилизации решения.

---

## 3. Каноническое различение v3.2

Главное добавление v3.2:

```text
символ фиксирует значимость
понятие фиксирует переносимое различение
понятие = сжатая инструкция различения
```

Лестница:

```text
функция -> значимость -> символ -> переносимое различение -> понятие
```

Статус:

```text
active canon
```

Основание:

- `PATCHES/2026-04-25_symbol_to_concept.md`;
- кейсы охры, огня, погребения;
- cross-link с Culture as Instructions.

---

## 4. v3.1_full status

Файл:

```text
VERSIONS/v3.1_full.md
```

Статус:

```text
migration draft / needs verification
```

Содержит важные элементы:

- сон;
- воображение;
- рефлексия;
- осознанность;
- R3 modes;
- дисциплина;
- аффект;
- археологический слой;
- культура как инструкции.

Часть этих элементов уже используется как рабочий канон в памяти, но в GitHub должна оставаться migration draft до сверки.

---

## 5. Что не нужно автоматически переносить в CANON.md

Не переносить автоматически:

- все детали археологии;
- все PNA-связки;
- все SynTax-механизмы;
- все MEAT-связки;
- все speculative claims;
- подробные evidence-файлы;
- Q-R3 целиком;
- decoherence model целиком.

CANON.md должен быть коротким и стабильным.

---

## 6. Candidate material

### shadows_of_R3

Файл:

```text
PATCHES/2026-04-25_shadows_of_R3.md
```

Статус:

```text
candidate
```

Суть:

ритуал или символ может быть способом стабилизации поведения в зоне неопределённости, где прозрачная причинная модель недоступна.

Пока не переносить в canon.

Нужно:

- пройти candidate -> canon checklist;
- проверить на дополнительных кейсах;
- уточнить ограничения.

---

## 7. Migration draft material

### Q-R3

Файл:

```text
PATCHES/q_r3_system.md
```

Статус:

```text
migration draft / needs verification
```

Не переносить в canon без сверки.

### Recursive choice with decoherence

Файл:

```text
PATCHES/recursive_choice_decoherence.md
```

Статус:

```text
migration draft / needs verification
```

Не переносить в canon без отделения:

- R-уровень;
- модель выбора;
- формальная аналогия с открытыми системами.

---

## 8. Archaeology status

Весь блок `ARCHAEOLOGY/` сейчас имеет статус:

```text
migration draft / needs source verification
```

Археология важна для R-теории, но не должна автоматически превращаться в canon.

Правило:

```text
археологический маркер поддерживает гипотезу, но не доказывает R-уровень напрямую
```

---

## 9. Evidence status

Блок `EVIDENCE/` имеет статус:

```text
evidence layer / needs source verification
```

Evidence может усиливать или ослаблять R-теорию, но не равен канону.

---

## 10. Что стоит добавить в CANON.md позже

Возможные будущие короткие добавления после проверки:

### 10.1 R as outsourced learning

Формулировка:

```text
R-уровни — уровни вынесенного из реальности обучения
```

Статус:

```text
likely canon, but review needed
```

### 10.2 Sleep / imagination / reflection

Можно добавить только кратко:

```text
сон, воображение и рефлексия — разные режимы обучения без немедленной реальной ошибки
```

Статус:

```text
candidate for canon compression
```

### 10.3 R3 modes

Можно добавить как компактное различение:

```text
R3-A online control, R3-B local error analysis, R3-C offline retrospective rewrite
```

Статус:

```text
needs verification
```

---

## 11. Что должно остаться вне CANON.md

Оставить вне canon:

- детальные археологические спекуляции;
- brain size steps как speculative;
- PNA как нейрокогнитивный механизм;
- MEAT как отдельную теорию;
- Boundary Saturation;
- бизнес-кейсы;
- полные тексты Q-R3;
- подробные evidence reviews.

---

## 12. Рекомендация

Пока не обновлять `CANON.md`.

Сначала создать:

- `PATCHES/PATCH_INDEX.md`;
- `VERSIONS/VERSION_COMPARISON_v3.1_v3.2.md`;
- `EVIDENCE/EVIDENCE_INDEX.md`;
- `SOURCE_VERIFICATION_PLAN.md`.

После этого можно сделать точечный canon update, если будет ясно, что именно стабильно.

---

## 13. Current decision

```text
CANON.md remains unchanged
R Theory v3.2 remains active canon
v3.1_full remains migration draft
shadows_of_R3 remains candidate
Q-R3 remains migration draft
recursive_choice_decoherence remains migration draft
archaeology remains migration draft / source verification required
```

---

## 14. Review update 2026-05-28: R3 modes and instruction runtime

CSP event: `projects/syntax/events/2026-05-28-codex-theory-archive-r3-modes-review.md`

Review artifact:

- `PATCHES/2026-05-28_r3_modes_instruction_runtime_review.md`

Decision:

```text
CANON.md remains unchanged
R3 modes are elevated to canon-review candidate, not canon
instruction runtime requires route split before promotion
```

The strongest future canon-compression candidate is the reading of R levels as
learning displacement: R0 reacts, R1 pays through action/result feedback, R2
moves error into internal trajectory simulation, and R3 rewrites the rule that
generated behavior.

R3.1/R3.2/R3.3 can be reviewed as a compact operating-mode distinction:

```text
online control / local error repair / offline retrospective rule rewrite
```

Do not move the full instruction-runtime packet into R Theory canon. Split it
between R Theory, Culture as Instructions, SynTax operators, PNA source checks,
and GYMKiDs applied methodology where appropriate.
