# Получение набора компаний, связанных с указанным контактом

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указан тип параметра
- отсутствуют примеры (на других языках)
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "crm.contact.company.items.get" %}

**Scope**: [`crm`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `crm.contact.company.items.get` возвращает набор компаний, связанных с указанным контактом.

#|
|| **Параметр** | **Описание** ||
|| **id**^*^ | Идентификатор контакта. ||
|#

{% include [Сноска о примерах](../../../../_includes/examples.md) %}

## Пример

```js
var id = prompt("Введите ID");
BX24.callMethod(
    "crm.contact.company.items.get",
    {
        id: id
    },
    function(result)
    {
        if(result.error())
            console.error(result.error());
        else
            console.dir(result.data());
    }
);
```

{% include [Сноска о примерах](../../../../_includes/examples.md) %}

## Возвращаемые данные

Результат возвращается в виде массива объектов, каждый из которых содержит следующие [поля](./crm-contact-company-fields.md):

#|
|| **Поле** | **Описание** ||
|| **COMPANY_ID** | Идентификатор компании ||
|| **SORT** | Индекс сортировки ||
|| **ROLE_ID** | Идентификатор роли (зарезервировано) ||
|| **IS_PRIMARY** | Флаг первичной компании ||
|#