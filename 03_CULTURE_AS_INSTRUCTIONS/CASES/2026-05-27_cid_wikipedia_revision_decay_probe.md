# CID Probe: Wikipedia Revision Decay

Дата: 2026-05-27

Статус: experiment probe / non-canon

Связанные узлы:

- `03_CULTURE_AS_INSTRUCTIONS/PATCHES/2026-04-26_cultural_instruction_decay.md`
- `03_CULTURE_AS_INSTRUCTIONS/CASES/2026-05-26_cid_parent_message_retention_case.md`
- `03_CULTURE_AS_INSTRUCTIONS/CANON.md`
- `04_MEAT/CANON.md`
- `01_R_THEORY/CANON.md`

---

## 1. Зачем этот probe

Wikipedia даёт готовую цифровую среду, где культурные инструкции и утверждения проходят через последовательные версии.

Каждая статья имеет историю правок. Каждая правка может:

- сохранить формулировку;
- изменить формулировку, но сохранить смысл;
- изменить смысл;
- удалить утверждение;
- стабилизировать утверждение через источник, нейтральную формулировку или институциональную норму Wikipedia.

Это позволяет проверить центральное предсказание CID:

```text
literal retention < semantic retention < operator retention
```

То есть буквальная форма должна распадаться быстрее, чем смысловая структура, а смысловая структура быстрее, чем глубинная инструкция различения.

---

## 2. Почему Wikipedia подходит

Wikipedia — удобный аналог культурной сети потому что:

1. правки имеют timestamp;
2. доступны предыдущие версии;
3. можно сравнивать текст через интервалы;
4. редакторы выступают как распределённые агенты отбора;
5. правила нейтральности, источников и значимости выступают как институциональная стабилизация;
6. спорные статьи дают ускоренную динамику мутаций и отбора формулировок.

MediaWiki хранит revision history: каждая правка создаёт новую запись ревизии со страницей, временем, пользователем/IP и summary. Это делает статью временным рядом, а не статичным текстом.

---

## 3. Что измеряем

Единица анализа — claim/operator cluster.

Не слово.
Не предложение.
Не абзац.

А утверждение или инструкция различения, которая может пережить смену формы.

Три слоя:

| Слой | Что считается сохранением |
|---|---|
| Literal retention | совпала или почти совпала фраза |
| Semantic retention | смысл утверждения сохранился при другой формулировке |
| Operator retention | сохранилась инструкция различения / выбора, даже если смысловая формулировка изменилась |

Пример:

```text
AI will replace jobs
automation may affect employment
AI changes labor demand
```

Literal retention: низкий.
Semantic retention: средний.
Operator retention: высокий.

Operator:

```text
AI = фактор перераспределения труда
```

---

## 4. Минимальный объект теста

Первый test set должен быть маленьким.

Кандидаты страниц:

| Статья | Почему подходит |
|---|---|
| `Artificial intelligence` | много устойчивых и спорных утверждений, быстрые изменения поля |
| `COVID-19 pandemic` | высокая частота правок, борьба за формулировки, институциональная стабилизация |
| `Parkour` | ближе к прикладному домену пользователя, но динамика может быть слабее |
| `Homeschooling` | спорная социальная тема, много norm/benefit claims |
| `Video game addiction` | пересечение науки, морали, родительских тревог |

Рекомендуемый первый объект:

```text
Artificial intelligence
```

Причина: высокая плотность тезисов, много правок, удобно проверять transformation of claims.

---

## 5. Минимальный протокол

### Шаг 1. Выбрать страницу

Например:

```text
Artificial intelligence
```

### Шаг 2. Взять ревизии по интервалам

Не все ревизии подряд, а snapshots:

```text
T0  = первая выбранная дата
T1  = +7 дней
T2  = +30 дней
T3  = +180 дней
T4  = +365 дней
```

Для динамичных тем можно брать:

```text
T0, +1 день, +7 дней, +30 дней, +90 дней
```

### Шаг 3. Выделить claim clusters

Пример кластеров для AI:

```text
AI automates labor
AI creates existential risk
AI imitates human intelligence
AI is used in healthcare
AI requires regulation
AI systems can be biased
```

### Шаг 4. Для каждого snapshot отметить состояние кластера

| Состояние | Значение |
|---|---|
| `0` | отсутствует |
| `1L` | literal сохранён |
| `1S` | смысл сохранён, форма изменилась |
| `1O` | оператор сохранён, смысловая формулировка изменилась |
| `M` | мутировал в другой оператор |
| `D` | удалён |

### Шаг 5. Посчитать retention

```text
literal_retention(t) = L(t) / L(T0)
semantic_retention(t) = S(t) / S(T0)
operator_retention(t) = O(t) / O(T0)
```

Главная проверка:

```text
operator_retention(t) > semantic_retention(t) > literal_retention(t)
```

---

## 6. Что будет сильным подтверждением CID

CID получает поддержку, если:

1. буквальные формулировки быстро исчезают;
2. claim-level смысл живёт дольше буквальной формы;
3. operator-level инструкция живёт дольше claim-level смысла;
4. одни операторы стабилизируются, другие исчезают;
5. стабилизированные операторы часто получают источник, более нейтральную формулировку или переходят в устойчивый раздел статьи;
6. спорные формулировки показывают высокий mutation rate до стабилизации.

---

## 7. Что ослабит CID

CID ослабляется, если:

1. literal, semantic и operator retention падают одинаково;
2. operator-level невозможно кодировать воспроизводимо;
3. устойчивость объясняется только редакторским revert-war, а не структурой инструкции;
4. выбранные операторы оказываются слишком произвольными;
5. изменение страницы отражает только внешние события, а не внутреннюю динамику стабилизации инструкции.

---

## 8. Минимальный data table

```text
page, cluster_id, operator_label, t, revision_id, literal_state, semantic_state, operator_state, notes
```

Пример:

| page | cluster | operator | t | literal | semantic | operator | notes |
|---|---|---|---|---|---|---|---|
| Artificial intelligence | labor | AI changes labor demand | T0 | 1 | 1 | 1 | initial phrase |
| Artificial intelligence | labor | AI changes labor demand | T1 | 0 | 1 | 1 | phrase rewritten |
| Artificial intelligence | labor | AI changes labor demand | T2 | 0 | 1 | 1 | source added |
| Artificial intelligence | labor | AI changes labor demand | T3 | 0 | 0 | 1 | moved into automation/economics framing |

---

## 9. Tools / data entry points

Possible entry points:

1. MediaWiki Action API for fetching revisions of a page.
2. Wikipedia XML dumps for larger revision histories.
3. Existing reliability/revision datasets, e.g. Wiki-Reliability.
4. WikiHist.html if HTML-rendered historical page content is needed rather than raw wikitext.

For first probe, API snapshots are enough.

For scale, dumps or existing datasets are better.

---

## 10. Source anchors

Known adjacent research/data:

- Wiki-Reliability: large-scale dataset of almost 1M English Wikipedia article revisions with full article text, revision metadata, and reliability-template labels.
- WikiHist.html: English Wikipedia full revision history rendered to HTML.
- Wikipedia inter-language knowledge propagation dataset: tracks propagation of Wikipedia concepts across 309 language editions and 33M articles.
- MediaWiki revision model: each edit creates a revision row with page id, editor/IP, timestamp, and edit summary.

---

## 11. Relation to CID

Wikipedia is not the same as parent-message retention.

Parent-message retention measures instruction survival in human memory and choice.

Wikipedia revision decay measures instruction survival in a public, edited textual artifact.

The bridge:

```text
human memory case -> instruction survives through recall
Wikipedia case -> instruction survives through public revision and editorial selection
```

Both test the same CID distinction:

```text
form can decay while operator survives
```

---

## 12. Next action

Build a tiny notebook or script:

```text
input: page title + date checkpoints + target claim clusters
output: table of literal/semantic/operator retention states
```

Do not automate operator detection first.

First pass should be manual-coded on a small sample to test whether the distinction is stable enough to automate later.
