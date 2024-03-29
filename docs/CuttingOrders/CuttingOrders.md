# Обрезка заказов

Для правильного планирования отгрузок с учетом остатков производства используется АРМ **"Обрезка заказов"**. АРМ отвечает за обрезку **Заказов клиентов** и **Заказов на перемещение** по текущим остаткам и расходам на дату отгрузки.

> Остаток рассчитывается: Остатки на складах на дату + **Заявки на производство** от *Даты остатков* до *Даты заявки* + Приходы на склад от *Даты остатков* до *Даты заявки*.

> Расходом считаются заказы с подтвержденным количеством номенклатуры с датой отгрузки в промежуток от *Даты остатков* до *Даты заявки*.

АРМ **"Обрезка заказов"** расположен в разделе **"Заказы"** в подсистеме **"Обработка заказов клиентов"**.

[![1][1]][1]

Обрезка заказов происходит по [**Настройкам обрезки заказов**](../CuttingOrders/CuttingOrdersSetting.md). При выборе настройки автоматически заполнится дата отгрузки. После заполнения даты отгрузки, нужно обновить табличную часть, чтобы данные из **Заказов клиентов** и **Заказов на перемещение** загрузились в табличную часть.

[![2][2]][2]

Верхняя табличная часть отвечает за обрезку заказов.

[![3][3]][3]

При обновлении табличная часть заполнится элементами:

- Номенклатура – только те наименования номенклатуры, что указаны в заказах на конкретную дату отгрузки, или те, по которым существуют остатки
- Характеристика – соответствующие характеристики номенклатур из заказов
- Единицы измерения
- Всего:

    - Остаток – количество номенклатуры, которая осталась на складе и будет произведена в промежуток времени, указанный в [**Настройке обрезки заказов**](../CuttingOrders/CuttingOrdersSetting.md), за вычетом планируемых отгрузок
    - Расход – количество номенклатуры, отгруженное в промежуток между *Датой работы* и *Датой заявки*
    - Заказано – суммарное количество номенклатуры в заказе на этапе первого порядка
    - Подтверждено – суммарное количество номенклатуры, которое пользователь подтвердил для отгрузки
    - Отклонение – разница между этапом *Заказано* и *Подтверждено*

- Заказы клиентов и Заказы на перемещение:

    - Точка доставки – подтягивается из **Заказа клиента**
    - Номер заказа
    - Этапы документов – подтягиваются из справочника **"Этапы документов"** по соответствующему виду документа. Заказано – первый порядок, Подтверждено – второй порядок

> **Заявки на производство** передаются в колонку **Остатки** в промежуток между *Датой работы* и *Датой заявки*. **Заказы на перемещение** на определенную дату доставки попадают в АРМ в промежутке от *Даты работы* до *Даты отгрузки*.  Даты указываются в [**Настройке обрезки заказов**](../CuttingOrders/CuttingOrdersSetting.md). 

Табличная часть **Остатки** для выделенной номенклатуры детально показывает остатки по датам выпуска и процентам остаточного срока годности.

[![4][4]][4]

Объяснение элементов табличной части **Остатки**:

- Дата выпуска – дата, в которую заказ был изготовлен. Заполняется по оставшейся номенклатуре на складе, либо по **Заявкам на производство**. Берется из партий номенклатуры и из даты выпуска, указанной в  **Заявке на производство**.
- Остаток – количество номенклатуры, которое выпущено или планируется выпустить в соответствующую дату выпуска
- Расход – количество номенклатуры, отгруженное в промежуток межу *Датой работы* и *Датой заявки* в разрезе дат выпуска
- Заказано – общее количество номенклатуры, содержащейся в заказе на дату отгрузки.
- Подтверждено – количество номенклатуры, которое подходит по %ОСГ(проценту остаточного срока годности) для контрагента по всем заказам
- Заказ клиента и заказ на перемещение:

    - Точка доставки
    - Номер заказа и %ОСГ. Процент остаточного срока годности указывается по каждому контрагенту при его создании. У заказов на перемещение нет %ОСГ.
    - Заказано – количество номенклатуры из конкретного заказа клиента, ставится в ячейку вне допустимого срока годности
    - Подтверждено – количество номенклатуры, который подтвердил пользователь, в разрезе даты выпуска и %ОСГ

Для того, чтобы обрезать заказы по текущим остаткам, предусмотрены соответствующие кнопки.

[![5][5]][5]

При нажатии на кнопку **Заказано->Подтверждено**, номенклатуры по текущим остаткам переносятся из *Заказано* в *Подтверждено*. Например, потребность в *Заказе клиента* равна 300 шт., остаток на складе 200 шт.. После анализа на соответствие % ОСГ продукции для покупателя, **Заказ клиента** обрезается до 200 шт.. При совпадении количества в *Заказано* и *Подтверждено* пара ячеек подсвечивается зеленым, если количества не совпадают, число в *Подтверждено* выделяется жирным шрифтом и колонка **Отклонение** заполняется разницей.

[![6][6]][6]

По кнопке **Подтвердить** всем заказам присваивается этап *Подтверждено* и состояние документа меняется на *"Состояние Подтверждено Заказа клиента"* из [**Настройки обрезки заказов**](../CuttingOrders/CuttingOrdersSetting.md). Вследствие обрезки заказа в АРМе, у **Заказа клиента** изменится этап на *Подтверждено*, состояние на *Проверки успешны*. Заполнится количество подтвержденной номенклатуры, выставится дата выпуска продукции и причина расхождения.

[![7][7]][7]

По кнопке **Сохранить** все заказы сохраняются с подтвержденным количеством. Этап документа поменяется на *Подтверждено*, добавятся строки с подтвержденным количеством номенклатуры для отгрузки, проставится дата выпуска и причина расхождения.

[![8][8]][8]

При необходимости выбрать другие настройки обрезки заказов, предусмотрена возможность внести изменения по гиперссылке **Настройки**. При этом в [**Настройке обрезки заказов**](../CuttingOrders/CuttingOrdersSetting.md) данные не изменятся.

[![9][9]][9]

[1]: CuttingOrders.assets/1.png
[2]: CuttingOrders.assets/2.png
[3]: CuttingOrders.assets/3.png
[4]: CuttingOrders.assets/4.png
[5]: CuttingOrders.assets/5.png
[6]: CuttingOrders.assets/6.png
[7]: CuttingOrders.assets/7.png
[8]: CuttingOrders.assets/8.png
[9]: CuttingOrders.assets/9.png
