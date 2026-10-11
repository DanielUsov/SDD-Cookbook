# Модуль «Заявки» (requests): актуальное описание

> Master spec модуля. Состояние до фичи HRPPRBCI-XXXX: показывается как «было».

## Назначение

Пользователь работает со списком заявок и может открыть заявку для просмотра.

## Основной механизм

- Список заявок отдаётся постранично, новые заявки идут первыми.
- Заявка имеет статус: `NEW`, `IN_PROGRESS`, `DONE`, `REJECTED`.
- Пользователь видит только заявки, к которым у него есть доступ (правила доступа не меняются фичами этого модуля).

## Описание по частям

- Backend: [BFRD.md](OpenSpec/cases/КП/example/store/specs/requests/BFRD.md)
- Frontend: [FFRD.md](OpenSpec/cases/КП/example/store/specs/requests/FFRD.md)
- Контракты: [OpenSpec/cases/КП/example/store/specs/requests/contracts/api.yaml](OpenSpec/cases/КП/example/store/specs/requests/contracts/api.yaml), [OpenSpec/cases/КП/example/store/specs/requests/contracts/data-model.yml](OpenSpec/cases/КП/example/store/specs/requests/contracts/data-model.yml)
