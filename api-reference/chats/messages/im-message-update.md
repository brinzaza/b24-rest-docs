# Изменить отправленное сообщение

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- нужны правки под стандарт написания
- не указаны типы параметров
- отсутствуют примеры
- не прописаны ссылки на несозданные ещё страницы

{% endnote %}

{% endif %}

{% note info "im.message.update" %}

**Scope**: [`im`](../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Метод `im.message.update` отправляет изменения сообщения чат-бота.

#|
|| **Параметр** | **Пример** | **Описание** | **Ревизия** ||
|| **MESSAGE_ID^*^**
[`unknown`](../../data-types.md) | `1` | Идентификатор сообщения | 18 ||
|| **MESSAGE**
[`unknown`](../../data-types.md) | `Текст сообщения` | Текст сообщения. Если передать пустое значение, то сообщение будет удалено | 18 ||
|| **ATTACH**
[`unknown`](../../data-types.md) | | Вложение | 18 ||
|| **URL_PREVIEW**
[`unknown`](../../data-types.md) | `Y` | Преобразовывать ссылки в rich-ссылки | 18 ||
|| **KEYBOARD**
[`unknown`](../../data-types.md) | | Клавиатура | 18 ||
|| **MENU**
[`unknown`](../../data-types.md) | | Контекстное меню | 18 ||
|#

{% include [Сноска о параметрах](../../../_includes/required.md) %}

## Примеры

{% include [Пояснение о restCommand](../_includes/rest-command.md) %}

```php
$result = restCommand('
    im.message.update',
    Array(
        'MESSAGE_ID' => 1,
        'MESSAGE' => 'Текст сообщения',
        'ATTACH' => '',
        'URL_PREVIEW' => 'Y',
        'KEYBOARD' => '',
        'MENU' => '',
    ),
    $_REQUEST[
        "auth"
    ]
);
```

{% include [Сноска о примерах](../../../_includes/examples.md) %}

## Ответ в случае успеха

```json
{
    "result": true
}
```

**Результат выполнения**: `true` или ошибка.

## Ответ в случае ошибки

```json
{
    "error": "MESSAGE_ID_ERROR",
    "error_description": "Не передан идентификатор сообщения"
}
```

### Описание ключей

- `error` – код возникшей ошибки
- `error_description` – краткое описание возникшей ошибки

### Возможные коды ошибок

#|
|| **Код** | **Описание** ||
|| **MESSAGE_ID_ERROR** | Не передан идентификатор сообщения ||
|| **CANT_EDIT_MESSAGE** | У вас нет доступа к этому сообщению или время на его модификацию истекло (после публикации прошло более 3-х суток) ||
|| **ATTACH_ERROR** | Весь переданный объект вложения не прошел валидацию ||
|| **ATTACH_OVERSIZE** | Превышен максимально допустимый размер вложения (30 Кб) ||
|| **KEYBOARD_ERROR** | Весь переданный объект клавиатуры не прошел валидацию ||
|| **KEYBOARD_OVERSIZE** | Превышен максимально допустимый размер клавиатуры (30 Кб) ||
|| **MENU_ERROR** | Весь переданный объект меню не прошел валидацию ||
|| **MENU_OVERSIZE** | Превышен максимально допустимый размер меню (30 Кб) ||
|#

## Ссылки по теме:

- [Как работать с набираемыми клавиатурами](.)
- [Как работать с вложениями](.)
- [Форматирование сообщений](.)