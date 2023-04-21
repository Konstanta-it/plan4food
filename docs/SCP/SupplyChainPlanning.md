# Планирование цепочек поставок

Для настройки АРМа **"Планирование цепочек поставок"** заполняется [**"Сценарий планирования цепочек поставок"**](SupplyChainPlanningScenarios.md), автоматически заполнятся период планирования.

Далее заполняется вкладка **"Потребности"**, для этого выбирается один из вариантов заполнения:

- Заполнить все потребности за период
- Заполнить потребности по сценарию – выбирается сценарий планирования потребностей в отгрузке

    [![1][1]][1]

- Заполнить потребности по документу – выбирается план потребностей

    [![2][2]][2]

- Заполнить потребностями склада – выбирается склад

    [![3][3]][3]

- Заполнить потребности по нескольким сценариям – выбираются несколько сценариев планирования потребностей в отгрузке

    [![4][4]][4]

- Заполнить по заказам
- Открыть АРМ [**"Планирования потребностей"**](NeedsPlanning.md) – планирование потребностей осуществляется в АРМе **"Планирование потребностей"**, результаты передаются в АРМ **"Планирование цепочек поставок"**

    [![5][5]][5]

После выбора варианта заполнения надо нажать кнопку **"Заполнить"** для заполнения потребностей:

[![6][6]][6]

Далее на вкладке **"Движения"** обновляется таблица:

[![7][7]][7]

Необеспеченные строки выделяются красным цветом. Для обеспечения потребностей нажимаем кнопку **"Обеспечить"** или **"Обеспечить автоматически"**. 

При нажатии кнопки **"Обеспечить автоматически"** обеспечение осуществляется автоматически по назначенным схемам.

[![8][8]][8]

Схемы обеспечения определяются автоматически на основании установленных приоритетов, при необходимости их можно менять вручную, нажав на кнопку **"Обеспечить"**.

В нижней части открывшейся формы обеспечения справа определяются потребности. При выборе схемы обеспечения с типом **"Производство"** там отображается сырье, которое требуется для производства. На следующей итерации обеспечения будет обеспечиваться сырье.

[![9][9]][9]

Далее выбирается период и уровень обеспечения:

- Только потребности
- До минимального запаса
- До рекомендуемого запаса
- До максимального запаса

Затем нажимаем одну из кнопок:

- **"Текущий"** - план заполнится на текущую дату выпуска рекомендациями по обеспечению
- **"Весь"** - план заполнится на все даты выпуска

При подборе объема обеспечения учитывается кратность партии из ресурсной спецификации.

[![10][10]][10]

После заполнения плана обеспечения передаем результат в АРМ **"Планирование цепочек поставок"**, для этого нажимаем кнопку **"Передать результат"**.

Обеспечивать можно столько раз сколько потребуется. После обеспечения на вкладке **"План"** можно создать документы:

- **"Заказ на перемещение"** – создается для типа обеспечения перемещение
- **"Заявка на закупку"** – создается для типа обеспечения закупка
- **"Заявка на производство"** – создается для типа обеспечения производство

[![11][11]][11]

В результате работы АРМа планируется перемещение, закупка и производство готовой продукции и сырья.

[1]: SupplyChainPlanning.assets/1.png
[2]: SupplyChainPlanning.assets/2.png
[3]: SupplyChainPlanning.assets/3.png
[4]: SupplyChainPlanning.assets/4.png
[5]: SupplyChainPlanning.assets/5.png
[6]: SupplyChainPlanning.assets/6.png
[7]: SupplyChainPlanning.assets/7.png
[8]: SupplyChainPlanning.assets/8.png
[9]: SupplyChainPlanning.assets/9.png
[10]: SupplyChainPlanning.assets/10.png
[11]: SupplyChainPlanning.assets/11.png