## ADDED Requirements

### Requirement: Фильтрация списка заявок

Сервис SHALL возвращать только заявки, подходящие под все переданные фильтры: `status` (значения по «или»), `createdFrom`, `createdTo`, `assigneeId`.

#### Scenario: Один статус
- **WHEN** клиент передаёт `status=NEW`
- **THEN** в ответе только заявки со статусом `NEW`

#### Scenario: Комбинация фильтров
- **WHEN** клиент передаёт `status=NEW` и `assigneeId`
- **THEN** в ответе только заявки со статусом `NEW` этого исполнителя

#### Scenario: Неверный период
- **WHEN** `createdFrom` позже `createdTo`
- **THEN** сервис возвращает `400` с кодом `INVALID_PERIOD`

#### Scenario: Неизвестный статус
- **WHEN** в `status` передано неизвестное значение
- **THEN** сервис возвращает `400` с кодом `INVALID_STATUS`
