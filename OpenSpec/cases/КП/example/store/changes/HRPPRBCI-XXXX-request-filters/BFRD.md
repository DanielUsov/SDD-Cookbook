# BFRD: фильтры в списке заявок (backend)

Единое описание фичи: [FRD.md](OpenSpec/cases/КП/example/store/changes/HRPPRBCI-XXXX-request-filters/FRD.md).

## Что меняется

Операция `GET /requests` принимает дополнительные необязательные параметры отбора. Полное описание: [OpenSpec/cases/КП/example/store/changes/HRPPRBCI-XXXX-request-filters/contracts/api.yaml](OpenSpec/cases/КП/example/store/changes/HRPPRBCI-XXXX-request-filters/contracts/api.yaml).

| Параметр | Тип | Правило |
|---|---|---|
| `status` | список значений статуса | можно передать несколько раз; значения объединяются по «или» |
| `createdFrom` | дата | нижняя граница даты создания, включительно |
| `createdTo` | дата | верхняя граница даты создания, включительно |
| `assigneeId` | идентификатор | заявки этого исполнителя |

## Правила

1. Если передано несколько разных параметров, заявка должна подходить под все (связка «и»).
2. Если параметров нет, поведение не меняется.
3. Сортировка и постраничная выдача остаются прежними.
4. Правила доступа к заявкам не меняются: пользователь видит только свои допустимые заявки, фильтры сужают этот набор.

## Ошибки

| Ситуация | Ответ |
|---|---|
| `createdFrom` позже `createdTo` | `400`, код `INVALID_PERIOD` |
| неизвестное значение в `status` | `400`, код `INVALID_STATUS` |

Ответ `400` содержит код ошибки и человекочитаемое сообщение.

## Данные

Для требования по времени ответа (см. FRD) добавляются индексы по полям фильтрации. Описание: [OpenSpec/cases/КП/example/store/changes/HRPPRBCI-XXXX-request-filters/contracts/data-model.yml](OpenSpec/cases/КП/example/store/changes/HRPPRBCI-XXXX-request-filters/contracts/data-model.yml). Выбор способа реализации и миграции остаётся за разработчиком.
