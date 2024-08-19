# Просмотр полей для связи сделка-контакт

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- отсутствуют примеры (на других языках)
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "crm.deal.contact.fields" %}

**Scope**: [`crm`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `crm.deal.contact.fields` возвращает для связи сделка-контакт описание полей, используемых методами семейства `crm.deal.contact.*`, то есть [crm.deal.contact.items.get](./crm-deal-contact-items-get.md), [crm.deal.contact.items.set](./crm-deal-contact-items-set.md), [crm.deal.contact.add](./crm-deal-contact-add.md) и т.д.

Без параметров.

## Пример

```js
BX24.callMethod(
    "crm.deal.contact.fields",
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

## Возвращаемые поля

#|
|| **Поле** | **Описание** ||
|| **SORT**
[`integer`](../../../data-types.md) | Индекс сортировки (число). Определяет, в каком порядке привязанные контакты будут показаны в сделке. ||
|| **IS_PRIMARY**
[`char`](../../../data-types.md) | [Y/N] Является ли привязка основной. В сделке всегда есть основной контакт. Для него будет `IS_PRIMARY=Y`, для остальных `IS_PRIMARY=N`. ||
|| **CONTACT_ID**
[`integer`](../../../data-types.md) | Идентификатор контакта, привязанного к сделке (число). ||
|#
