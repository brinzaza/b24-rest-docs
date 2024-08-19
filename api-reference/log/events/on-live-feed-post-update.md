# На редактирование сообщения в Ленте новостей

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- какие данные передаются в событие
- не прописаны ссылки на ещё не созданные страницы
- отсутствуют примеры

{% endnote %}

{% endif %}

{% note info "OnLiveFeedPostUpdate" %}

**Scope**: [`log`](../../scopes/permissions.md)og | **Права на выполнение**: `любой пользователь`

{% endnote %}

Событие `OnLiveFeedPostUpdate` вызывается после изменения поста в Ленте новостей. Прокси к событию [OnAfterSocNetLogUpdate](.).

#|
|| **Поле** | **Описание** ||
|| **ID** | Идентификатор измененного сообщения ||
|#
{% include [Сноска о параметрах](../../_includes/required.md) %}