---
jira-id: HRPPRBCI-YYYY
store-feature: HRPPRBCI-XXXX
store-version: HRPPRBCI-XXXX/v1
---

# request-filters-ui: панель фильтров в списке заявок

Frontend-часть фичи Store HRPPRBCI-XXXX.

| Поле | Значение |
|---|---|
| Jira | HRPPRBCI-YYYY: отдельная Jira-задача frontend, связанная с историей HRPPRBCI-XXXX |
| Ветка | `feature/HRPPRBCI-YYYY` |
| Фича Store | HRPPRBCI-XXXX (тег `HRPPRBCI-XXXX/v1`) |

Здесь `jira-id` отличается от `store-feature`: декомпозиция сделана на уровне Jira, у frontend своя задача. Для сравнения: у backend-changes `jira-id` совпадает с историей, потому что декомпозиция сделана разработчиком без отдельных задач.

## Что делаем

Реализуем панель фильтров над таблицей по описанию из Store: [FFRD.md](OpenSpec/cases/КП/example/store/changes/HRPPRBCI-XXXX-request-filters/FFRD.md) (в репозитории читается из `openspec/store/` на теге).

## Границы

- Входит: панель фильтров, синхронизация с адресной строкой, состояния экрана.
- Не входит: серверная логика отбора (backend).
