# Возвращение элементов перечисления «Тип содержания»

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- отсутствует ответ в случае ошибки
- отсутствует ответ в случае успеха
- нет примеров на др. языках
  
{% endnote %}

{% endif %}

{% note info "crm.enum.contenttype" %}

**Scope**: [`crm`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

## Описание

```js
crm.enum.contenttype()
```

Возвращает элементы перечисления «Тип содержания».

## Параметры

Без параметров.

## Примеры

```javascript
BX24.callMethod(
    "crm.enum.contenttype",
    {},
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