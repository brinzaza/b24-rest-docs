# Записи таймлайна

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% note info "Права" %}

**Scope**: [`rpa`](../../../scopes/permissions.md) | **Кто может выполнять метод**: `любой пользователь`

{% endnote %}

Набор методов для работы с записями таймлайна.

#|
|| **Метод** | **Описание** ||
|| [rpa.timeline.listForItem](./rpa-timeline-list-for-item.md) | Метод возвращает массив записей таймлайна для элемента с идентификатором itemId процесса с идентификатором itemId, отсортированные по убыванию даты создания (сверху самые новые). ||
|| [rpa.timeline.updateIsFixed](./rpa-timeline-update-is-fixed.md) | Метод обновляет флаг прикрепления записи. ||
|| [rpa.timeline.add](./rpa-timeline-add.md) | Метод создаст новую запись таймлайна у элемента с идентификатором itemId процесса с идентификатором typeId. ||
|| [rpa.timeline.update](./rpa-timeline-update.md) | Метод обновит запись таймлайна с идентификатором id. ||
|| [rpa.timeline.delete](./rpa-timeline-delete.md) | Метод удалит запись таймлайна с идентификатором id. ||
|#