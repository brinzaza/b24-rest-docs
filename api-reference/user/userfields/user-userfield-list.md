# Получение списка пользовательских полей

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- возможно, нужны параметры или поля и их типы
- не указана обязательность параметров
- отсутствуют примеры на др.языках
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки
 
{% endnote %}

{% endif %}

{% note info "user.userfield.list" %}

**Scope**: [`user.userfield`](../../scopes/permissions.md) | **Права на выполнение**: `администратор`

{% endnote %}

Метод позволяет получить список пользовательских полей. Доступен только пользователю с правами администратора. Доступны только фильтр и сортировка.

Фильтр доступен по ключам:

- **ID**
- **FIELD_NAME**
- **USER_TYPE_ID**
- **XML_ID**
- **SORT**
- **MULTIPLE**
- **MANDATORY**
- **SHOW_FILTER**
- **SHOW_IN_LIST**
- **EDIT_IN_LIST**
- **IS_SEARCHABLE**
- **LANG**

## Пример

```php
CRest::call(
    'user.userfield.list',
    [
        'order' => ['ID' => 'desc'],
        'filter' => ['ID' => 42],
    ]
);
```
{% include [Сноска о примерах](../../../_includes/examples.md) %}