# SynTax Patch Index

Статус: active patch index
Дата: 2026-04-25

## Назначение

Этот файл индексирует ключевые SynTax-патчи, перенесённые в GitHub.

Цель — видеть:

- что добавил каждый патч;
- какой дефект закрывал;
- активен ли патч;
- какие файлы связаны с патчем;
- что требует сверки с исходным SynTax-чатом.

---

## 1. v1.9 — Infrastructure Split

### Файл

- `v1.9_infrastructure_split.md`

### Статус

```text
active architecture patch / needs source verification
```

### Суть

Разделение инфраструктуры на:

- Memory Infrastructure;
- Evolution Infrastructure.

### Что закрывает

Риск попадания рабочих мутаций прямо в канон.

### Связанные файлы

- `../../00_META/MIGRATION_STATUS_RULES.md`
- `../../00_META/MIGRATION_MODE.md`

---

## 2. v2.6 — Context Arbitration Step

### Файл

- `v2.6_context_arbitration_step.md`

### Статус

```text
active architecture patch / needs source verification
```

### Суть

Вводит стадию выбора между context modules перед интерпретацией.

### Что закрывает

Silent steering и преждевременное подключение любимой рамки.

---

## 3. v2.8 — Error E11 Context Lock-In

### Файл

- `v2.8_error_E11_context_lock_in.md`

### Статус

```text
active error patch / needs source verification
```

### Суть

Фиксирует ошибку преждевременной фиксации на одной рамке.

### Что закрывает

Догматизацию через context module.

---

## 4. v3.0 — Progress Delta Check

### Файл

- `v3.0_progress_delta_check.md`

### Статус

```text
active response-layer patch
```

### Суть

Ответ должен давать реальное изменение понимания, а не просто выглядеть сложным.

### Что закрывает

False Depth.

---

## 5. v3.3 — Canon Aging

### Файл

- `v3.3_canon_aging.md`

### Статус

```text
active memory-infrastructure patch
```

### Суть

Вводит статусы:

- Active Canon;
- Archived Canon;
- Deprecated Canon.

### Что закрывает

Накопление устаревших конструкций в активном каноне.

---

## 6. v3.5 — Exploration Budget

### Файл

- `v3.5_exploration_budget.md`

### Статус

```text
active runtime patch
```

### Суть

Ограничивает бесконечное расширение анализа.

### Что закрывает

Cognitive drift и чрезмерную эксплорацию.

---

## 7. v3.6 — Module Independence

### Файл

- `v3.6_module_independence.md`

### Статус

```text
active core-architecture patch
```

### Суть

Core Thinking Architecture должна работать без любого конкретного context module.

### Что закрывает

Скрытую зависимость ядра от любимой теории.

---

## 8. v3.7 — Error Recurrence Counter

### Файл

- `v3.7_error_recurrence_counter.md`

### Статус

```text
active error-architecture patch
```

### Суть

Отслеживает повторение ошибок и переводит recurrent failure в patch pressure.

### Что закрывает

Трактовку системных ошибок как набора локальных случаев.

---

## 9. v4.3 — Drift Detection Protocol

### Файл

- `v4.3_drift_detection_protocol.md`

### Статус

```text
active audit patch
```

### Суть

Выявляет медленное отклонение поведения SynTax от канона.

### Что закрывает

Невидимую эрозию качества.

---

## 10. v4.6 — Complexity Governance Rule

### Файл

- `v4.6_complexity_governance_rule.md`

### Статус

```text
active architecture-governance patch
```

### Суть

Новая сложность допустима только при приросте различающей силы.

### Что закрывает

Architecture bloat.

---

## 11. v4.9 — Operator Registry Protocol

### Файл

- `v4.9_operator_registry_protocol.md`

### Статус

```text
active operator-layer patch
```

### Суть

Вводит управляемый каталог операторов и operator passports.

### Что закрывает

Operator explosion и неявное дублирование операторов.

---

## 12. v5.2 — Genius Axis Disambiguation (Gᴀ / Gᴛ)

### Файл

- `v5.2_genius_axis_disambiguation.md`

### Статус

```text
active evaluation patch / source: chat recovery 2025-11-21 / non-canon
```

### Суть

Вводит две независимые оси оценки идеи:
- **Gᴀ** — genius-impact: резонанс, удар, красота, продуктивность как толчок
- **Gᴛ** — genius-truth: строгость, фальсифицируемость, объяснительная сила

Оси ортогональны. Ответ на «это гениально?» обязан разворачиваться по обеим.

### Что закрывает

Потерю измерения при одноосевой оценке идеи.

---

## 12. Patch-line summary

| Patch | Status | Function |
|---|---|---|
| v1.9 | active | split memory/evolution infrastructure |
| v2.6 | active | context arbitration |
| v2.8 | active | E11 context lock-in |
| v3.0 | active | progress delta |
| v3.3 | active | canon aging |
| v3.5 | active | exploration budget |
| v3.6 | active | module independence |
| v3.7 | active | error recurrence |
| v4.3 | active | drift detection |
| v4.6 | active | complexity governance |
| v4.9 | active | operator registry |
| v5.2 | active / non-canon | genius axis disambiguation (Gᴀ / Gᴛ) |

---

## 13. What remains open

- сверить патчи с исходным SynTax-чатом;
- проверить, не пропущены ранние патчи до v1.9;
- проверить, не пропущены intermediate versions;
- не создавать новые патчи до source verification или явной необходимости.

## Current patch block status

```text
indexed / active patch line transferred / source verification required
```
