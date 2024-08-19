# Сущность Шаблон представления

{% note warning "Мы еще обновляем эту страницу" %}

Тут может не хватать некоторых данных — дополним в ближайшее время

{% endnote %}

{% if build == 'dev' %}

{% note alert "TO-DO _не выгружается на prod_" %}

- нужны правки под стандарт написания

{% endnote %}

{% endif %}

Сущность описывает шаблоны представления страницы (с шапкой, подвалом, сайдбаром).

Шаблоны представления описывают представления конкретного сайта или страницы о том, как выглядит их разметка:

- С шапкой и подвалом
- С сайдбаром
- Их вариации

Привязка к странице сильнее, чем привязка к сайту (если и сайт и страница данного сайта привязаны к разным шаблонам, то вывод будет происходить по сетке шаблона страницы). Каждая область такого шаблона есть отдельная страница (с набором блоков и прочими аналогичными характеристиками).

На данный момент в системе предустановлено несколько шаблонов представления и расширять их у стороннего разработчика нет возможности.

Вот данный список:

#|
|| **Внешний код (XML_ID)** | **Название** ||
|| **empty** | Пустой ||
|| **sidebar_left** | С сайдбаром слева ||
|| **sidebar_right** | С сайдбаром справа ||
|| **header_footer** | С шапкой и подвалом ||
|| **without_left** | Без левого сайдбара ||
|| **without_right** | Без правого сайдбара ||
|#

Обратите внимание, здесь не указываются идентификаторы шаблонов, вместе с тем при передаче [сайту](../site/base-fields.md) или [странице](../page/index.md) нужно указать именно идентификатор. Чтобы получить непосредственно идентификатор, воспользуйтесь методом [landing.template.getlist](./landing-template-get-list.md). Вы получите список идентификаторов в разрезе именно вашего портала.