# Sync Log — SynTax

```text
layer: governance  (как ведётся архив; нумерация v1.9..v5.x)
```

## 2026-04-25

Создан проектный модуль SynTax.

Добавлено:

- `CANON.md`
- `STATUS.md`
- `WORKSPACE.md`

Создана папка патчей:

- `PATCHES/README.md`

Перенесена серия ключевых архитектурных патчей:

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

Промежуточный вывод: SynTax больше не хранится только как компактный канон. В GitHub появилась трассируемая история ключевых архитектурных изменений.

Следующий шаг: создать `00_META/CANDIDATE_TO_CANON_CHECKLIST.md` и связать его с Infrastructure Split, Progress Delta, Complexity Governance и Canon Aging.
