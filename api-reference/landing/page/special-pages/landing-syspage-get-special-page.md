# Получение адреса специальной страницы сайта

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- отсутствуют параметры или поля
- не указаны типы параметров
- не указана обязательность параметров
- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "landing.syspage.getSpecialPage" %}

**Scope**: [`landing`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `landing.syspage.getSpecialPage` возвращает адрес специальной страницы сайта. В примере показано как получить ссылку на страницу персонального раздела сайта.

```js
BX24.callMethod(
    'landing.syspage.getSpecialPage',
    {
        siteId: 1391,// ИД сайта
        type: 'personal',// тип специальной страницы
        additional: {// необязательный массив доп. параметров, которые будут добавлены к URL
            SECTION: 'private'
        }
    },
    function(result)
    {
        if(result.error())
        {
            console.error(result.error());
        }
        else
        {
            console.info(result.data());
        }
    }
);
```

{% include [Сноска о примерах](../../../../_includes/examples.md) %}