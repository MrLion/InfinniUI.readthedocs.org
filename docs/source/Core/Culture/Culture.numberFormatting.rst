Culture.numberFormatting
========================

Ниже приведены настройки форматирования для числовых значений.
Интерпретация большинства перечисленных форматов зависит от текущей
культуры
(`GlobalContext <../GlobalContext/>`__. `Culture.numberFormatInfo <Culture.numberFormatInfo.html>`__).

Предопределенные форматы
------------------------

Предопределенные форматы представляют числовые значения с использованием
часто используемых шаблонов. Предопределенный формат числового значения
записывается в виде "Axx", где "A" - обозначение предопределенного
формата из таблице ниже, "xx" - необязательное целочисленное значение,
определяющее точность представления числового значения (количество
знаков в дробной части). Значение точности "xx" может находиться в
диапазоне от 0 до 99. Если точность не определена, используются
соответствующие настройки представления числовых значений текущей
культуры -
`GlobalContext <../GlobalContext/>`__. `Culture.numberFormatInfo <Culture.numberFormatInfo.html>`__.

.. list-table::
   :header-rows: 1

   * - Формат
     - Наименование
     - Описание
     - Пример
   * -  
     - *Числовые значения*
     -  
     -  
   * - ``n`` or ``N``
     - Представления числового значения.
     - Формат использует настройки представления числовых значений текущей культуры `GlobalContext <../GlobalContext/>`__. `Culture.NumberFormatInfo.Number <Culture.numberFormatInfo.html>`__.
     - ru-RU, "n", 123.4567: "123,46", ru-RU, "n3", 123.4567: "123,457", en-US, "n", 123.4567: "123.46", en-US, "n3", 123.4567: "123.457"
   * -  
     - *Значения процентов*
     -  
     -  
   * - ``p``
     - Представление значения процентов с преобразованием.
     - Перед представлением значение процентов умножается на 100. Например, значение "0.15" будет представлено, как "15 %". Формат использует настройки представления значений процентов текущей культуры `GlobalContext <../GlobalContext/>`__. `Culture.numberFormatInfo.Percent <Culture.numberFormatInfo.html>`__.
     - ru-RU, "p", 123.4567: "12 345,67%", ru-RU, "p3", 123.4567: "12 345,670%", en-US, "p", 123.4567: "12,345.67 %", en-US, "p3", 123.4567: "12,345.670 %"
   * - ``P``
     - Представление значения процентов без преобразования.
     - Перед представлением значение процентов не умножается на 100. Например, значение "0.15" будет представлено, как есть - "0.15 %". Формат использует настройки представления значений процентов текущей культуры `GlobalContext <../GlobalContext/>`__. `Culture.numberFormatInfo.Percent <Culture.numberFormatInfo.html>`__.
     - ru-RU, "P", 123.4567: "123,46%", ru-RU, "P3", 123.4567: "123,457%", en-US, "P", 123.4567: "123.46 %", en-US, "P3", 123.4567: "123.457 %"
   * -  
     - *Значения денежных единиц*
     -  
     - \_
   * - ``c`` or ``C``
     - Представление значения денежной единицы.
     - Формат использует настройки представления представления денежных единиц текущей культуры `GlobalContext <../GlobalContext/>`__. `Culture.numberFormatInfo.Currency <Culture.numberFormatInfo.html>`__.
     - ru-RU, "c", 123.4567: "123,46р.", ru-RU, "c3", 123.4567: "123,457р.", en-US, "c", 123.4567: "$123.46", en-US, "c3", 123.4567: "$123.457"


Элементы пользовательского формата
----------------------------------

Пользователь может определять собственные строки форматирования,
используя ниже перечисленные элементы.

.. list-table::
   :header-rows: 1

   * - Элемент
     - Описание
   * - ``%``
     - Должен заменяться на `GlobalContext <../GlobalContext/>`__. `Culture.numberFormatInfo.percentSymbol <Culture.numberFormatInfo.html>`__.
   * - ``$``
     - Должен заменяться на `GlobalContext <../GlobalContext/>`__. `Culture.NumberFormatInfo.CurrencySymbol <Culture.numberFormatInfo.html>`__.
   * - Иные символы
     - Вставляются, как есть, без изменения, если не совпадают с предопределенными форматами (см. выше).


Example
-------

.. list-table::
   :header-rows: 1

   * - Формат
     - Форматируемое значение
     - Результат форматирования (en-US)
   * - *Числовые значения*
     -  
     -  
   * - ``n``
     - 1234.567
     - 1,234.57
   * - ``n``
     - -1234.567
     - -1,234.57
   * - ``n0``
     - 1234.567
     - 1,235
   * - ``n0``
     - -1234.567
     - -1,235
   * - ``n1``
     - 1234.567
     - 1,234.6
   * - ``n1``
     - -1234.567
     - -1,234.6
   * - ``n2``
     - 1234.567
     - 1,234.57
   * - ``n2``
     - -1234.567
     - -1,234.57
   * - ``n3``
     - 1234.567
     - 1,234.567
   * - ``n3``
     - -1234.567
     - -1,234.567
   * - ``n4``
     - 1234.567
     - 1,234.5670
   * - ``n4``
     - -1234.567
     - -1,234.5670
   * - ``n5``
     - 1234.567
     - 1,234.56700
   * - ``n5``
     - -1234.567
     - -1,234.56700
   * - *Значения процентов*
     -  
     -  
   * - ``p``
     - 1234.56789
     - 123,456.79 %
   * - ``p``
     - -1234.56789
     - -123,456.79 %
   * - ``p0``
     - 1234.56789
     - 123,457 %
   * - ``p0``
     - -1234.56789
     - -123,457 %
   * - ``p1``
     - 1234.56789
     - 123,456.8 %
   * - ``p1``
     - -1234.56789
     - -123,456.8 %
   * - ``p2``
     - 1234.56789
     - 123,456.79 %
   * - ``p2``
     - -1234.56789
     - -123,456.79 %
   * - ``p3``
     - 1234.56789
     - 123,456.789 %
   * - ``p3``
     - -1234.56789
     - -123,456.789 %
   * - ``p4``
     - 1234.56789
     - 123,456.7890 %
   * - ``p4``
     - -1234.56789
     - -123,456.7890 %
   * - ``p5``
     - 1234.56789
     - 123,456.78900 %
   * - ``p5``
     - -1234.56789
     - -123,456.78900 %
   * - *Значения денежных единиц*
     -  
     -  
   * - ``c``
     - 1234.567
     - $1,234.57
   * - ``c``
     - -1234.567
     - ($1,234.57)
   * - ``c0``
     - 1234.567
     - $1,235
   * - ``c0``
     - -1234.567
     - ($1,235)
   * - ``c1``
     - 1234.567
     - $1,234.6
   * - ``c1``
     - -1234.567
     - ($1,234.6)
   * - ``c2``
     - 1234.567
     - $1,234.57
   * - ``c2``
     - -1234.567
     - ($1,234.57)
   * - ``c3``
     - 1234.567
     - $1,234.567
   * - ``c3``
     - -1234.567
     - ($1,234.567)
   * - ``c4``
     - 1234.567
     - $1,234.5670
   * - ``c4``
     - -1234.567
     - ($1,234.5670)
   * - ``c5``
     - 1234.567
     - $1,234.56700
   * - ``c5``
     - -1234.567
     - ($1,234.56700)

