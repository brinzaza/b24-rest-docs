# Отправление запроса на вступление в группу

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указаны типы параметров
- не указана обязательность параметров
- отсутствует ответ в случае ошибки
- нет примеров на др. языках

{% endnote %}

{% endif %}

{% note info "sonet_group.user.request" %}

{% include notitle [Скоуп sonet все](../_includes/scope-sonet-all.md) %}

{% endnote %}

## Описание

Метод отправляет запрос текущего пользователя на вступление в группу соцсети, при этом проверяются права на доступ текущего пользователя к группе. Если группа открыта для свободного вступления, пользователь сразу становится ее участником.

## Возвращает `true`, если запрос произошел успешно, или текст ошибки.

## Параметры

#|
|| **Параметр** | **Описание** ||
|| **GROUP_ID** | ID группы, в которую отправляется запрос. ||
|| **MESSAGE** | Текст запроса. ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %}

## Пример

```js
// Отправляем запрос на вступление в группу с ID=17
BX24.callMethod('sonet_group.user.request', {
    'GROUP_ID': 17,
    'MESSAGE': 'Request'
});
```
{% include [Сноска о примерах](../../../_includes/examples.md) %}

## Запрос:

```
https://mydomain.bitrix24.ru/rest/sonet_group.user.request.json?auth=52423d4a5f19f5f964f9b4e96a925cfa&GROUP_ID=17&MESSAGE=Request
```

## Ответ:

>200 OK

```json
{"result":true}
```