# Удалить нумератор

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- отсутствуют примеры
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "documentgenerator.numerator.delete" %}

**Scope**: [`documentgenerator`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `documentgenerator.numerator.delete` удаляет нумератор.

{% note warning %}

Удалить можно только те нумераторы, которые были созданы через [documentgenerator.numerator.add()](./index.md).

{% endnote %}

#|
|| **Параметр** | **Описание** ||
|| **id**^*^ | ID нумератора. ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %} 

## Ответ в случае успеха

Ответ пустой.