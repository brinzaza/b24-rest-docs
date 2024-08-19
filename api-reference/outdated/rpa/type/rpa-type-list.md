# Получение массива процессов с их полями

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- не указана обязательность параметров
- отсутствуют примеры
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "rpa.type.list" %}

**Scope**: [`rpa`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `rpa.type.list` вернёт массив процессов с их полями.

#|
|| **Параметр** | **Описание** ||
|| **select** | Массив полей для вывода. По умолчанию выводятся все. ||
|| **order** |  Список для сортировки, где ключ - поле, а значение - ASC или DESC. ||
|| **filter** | Список для фильтрации. ||
|| **start** | Сдвиг для постраничной навигации. ||
|#

## Ответ в случае успеха

> 200 OK

```json
{
    "types": [
        {},
        {}
    ]
}
```