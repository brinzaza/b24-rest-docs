# Удаление привязки дела

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- нужны правки под стандарт написания
- не указана обязательность параметров
- отсутствуют примеры
- отсутствует ответ в случае ошибки
- не прописаны ссылки на несозданные ещё страницы (справочник доступных типов)

{% endnote %}

{% endif %}

{% note info "crm.activity.binding.list" %}

**Scope**: [`crm`](../../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `crm.activity.binding.list` получает список привязок.

Метод вернет массив, элементами которого будут массивы, содержащие:
- `entityTypeId` - идентификатор типа элемента ([Справочник доступных типов](.));
- `entityId` - идентификатор элемента.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **activityId**
[`number`](../../../../data-types.md) | идентификатор дела ||
|| **START** | Порядковый номер элемента списка, начиная с которого необходимо возвращать следующие элементы при вызове текущего метода. Подробности в статье [{#T}](../../../../how-to-call-rest-api/list-methods-pecularities.md) ||
|#

## Примеры

```http
crm.activity.binding.list?activityId=1
```

{% include [Сноска о примерах](../../../../../_includes/examples.md) %}

## Ответ в случае успеха

> 200 OK
```json
{
    "result": [
        {
            "entityTypeId": 1,
            "entityId": 123
        },
        {
            "entityTypeId": 2,
            "entityId": 456
        },
        {
            "entityTypeId": 3,
            "entityId": 789
        }
    ]
}
```