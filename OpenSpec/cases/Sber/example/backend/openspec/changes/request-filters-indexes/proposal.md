---
jira-id: HRPPRBCI-XXXX
store-feature: HRPPRBCI-XXXX
store-version: HRPPRBCI-XXXX/v1
---

# request-filters-indexes: индексы для фильтрации заявок

Второй change фичи HRPPRBCI-XXXX. Работает в той же ветке `feature/HRPPRBCI-XXXX`, что и [request-filters-api](../request-filters-api/proposal.md): `jira-id` у обоих одинаковый.

## Что делаем

По дельте модели данных из Store (`contracts/data-model.yml`) создаём в схеме БД индексы по `status` и `createdAt`, а также по `assigneeId`. Миграцию и точный способ реализации выбирает разработчик под используемую СУБД.

## Границы

- Входит: миграция схемы и проверка времени ответа списка на большом объёме данных.
- Не входит: логика отбора (change `request-filters-api`).

## Критерий

Время ответа списка с фильтрами на объёме порядка миллиона заявок укладывается в целевое значение из FRD фичи.
