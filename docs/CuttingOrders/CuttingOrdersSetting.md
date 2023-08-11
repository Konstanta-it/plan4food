# Настройки обрезки заказов

Обрезка заказов происходит по **Настройкам обрезки заказов**, которые заполняются в разделе **"Заказы"** в подсистеме **"Сервис" - "Настройки исполнения заказов"**.

[![1][1]][1]

[![2][2]][2]

В **Настройках обрезки заказов** заполняется:

- Наименование
- Дата отгрузки – элемент справочника **"Варианты начала периода"**, заполняется для определения заказов по дате отгрузки, с которыми работаем

[![3][3]][3]

- Дата работы – элемент справочника **"Варианты начала периода"**, заполняется для получения остатков от указанной даты до *Даты заявки*.
- Дата заявки – элемент справочника **"Варианты начала периода"**, это дата конца периода, из которого подтягиваются остатки. Остатки будут подтягиваться в промежутке между *Датой работы* и *Датой заявки*.
- Причина расхождения – элемент справочника **"Причины корректировок документов"**, заполняется для указания причины расхождения количества в заказах с этапом *Подтверждено*
- Игнорировать %ОСГ – настройка, которая позволяет вручную корректировать количество подтвержденной номенклатуры, несмотря на %ОСГ.
- Товарные категории – отбор товарных категорий для обрезки
- Склады отгрузки
- Этап заказа клиента для чтения – в АРМ подтягиваются данные из заказов, у которых установлен указанный этап
- Этап заказа клиента для записи – при подтверждении обрезки в АРМе, заказу устанавливается указанный этап
- Состояние *"Подтверждено"* Заказа клиента – какое состояние примет **Заказ клиента**, после перевода на этап для записи
- Этап заказа на перемещение для чтения – в АРМ подтягиваются данные из **Заказа на перемещение**, у которых установлен указанный этап
- Этап заказа на перемещение для записи – при подтверждении обрезки в АРМе, **Заказу на перемещение** устанавливается указанный этап
- Состояние *"Подтверждено"* Заказа на перемещение – какое состояние примет **Заказ на перемещение**, после перевода на этап для записи
- Сценарий заявки – **Заявки на производство** отбираются по указанному сценарию
- Этап для чтения "Заявка на производство" – Данные подгружаются в АРМ из **Заявки на производство**, у которой установлен указанный этап
- Описание
- Автор

[![4][4]][4]

[1]: CuttingOrdersSetting.assets/1.png
[2]: CuttingOrdersSetting.assets/2.png
[3]: CuttingOrdersSetting.assets/3.png
[4]: CuttingOrdersSetting.assets/4.png