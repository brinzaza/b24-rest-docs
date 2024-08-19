# Отключение сотруднику признака наличия sip-aппарата

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- не указана обязательность параметров
- отсутствуют примеры
- отсутствует ответ в случае успеха
- отсутствует ответ в случае ошибки

{% endnote %}

{% endif %}

{% note info "voximplant.user.deactivatePhone" %}

{% include notitle [Скоуп telephony admin](../../_includes/scope-telephony-admin.md) %}

{% endnote %}

Метод `voximplant.user.deactivatePhone` отключает сотруднику признак наличия sip-aппарата. Метод проверяет наличие права на модификацию пользователя.

Метод доступен обладателю [права](https://helpdesk.bitrix24.ru/open/18177766/) `Настройки пользователя - Изменение` в соответствии с его значением этого права.

#|
|| **Параметр** / **Тип** | **Описание** ||
|| **USER_ID**^*^
[`int`](../../../data-types.md) | Идентификатор пользователя. ||
|#

{% include [Сноска о параметрах](../../../../_includes/required.md) %}