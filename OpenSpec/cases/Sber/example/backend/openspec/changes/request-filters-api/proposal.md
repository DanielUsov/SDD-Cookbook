---
jira-id: HRPPRBCI-XXXX
store-feature: HRPPRBCI-XXXX
store-version: HRPPRBCI-XXXX/v1
---

# request-filters-api: параметры отбора в списке заявок

Первый из двух changes, на которые разработчик декомпозировал фичу Store HRPPRBCI-XXXX. Второй: [request-filters-indexes](../request-filters-indexes/proposal.md).

## Что делаем

Реализуем в backend параметры отбора `status`, `createdFrom`, `createdTo`, `assigneeId` для `GET /requests` по описанию из Store: [BFRD.md](../../../../store/changes/HRPPRBCI-XXXX-request-filters/BFRD.md) (в репозитории файл читается из `openspec/store/` на теге `HRPPRBCI-XXXX/v1`).

## Границы

- Входит: приём и валидация параметров, отбор в выборке, ошибки `INVALID_PERIOD` и `INVALID_STATUS`.
- Не входит: индексы и миграция (change `request-filters-indexes`).

## Почему отдельный change

Сужение контекста агента: логика запроса и работа со схемой данных реализуются поэтапно.
