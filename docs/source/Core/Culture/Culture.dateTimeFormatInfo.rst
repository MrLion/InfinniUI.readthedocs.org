Culture.dateTimeFormatInfo
==========================

Сведения о формате представления даты и времени.

Описание настроек форматирования для даты и времени приведено в разделе
`DateTimeFormatting <Culture.dateTimeFormatting.html>`__.

Properties
----------

monthNames
~~~~~~~~~~

Тип: ``Array.<String>``

Список наименований месяцев.

.. code:: json

    ["Январь", "Февраль", "Март", "Апрель", "Май", "Июнь", "Июль", "Август", "Сентябрь", "Октябрь", "Ноябрь", "Декабрь"]

abbreviatedMonthNames
~~~~~~~~~~~~~~~~~~~~~

Тип: ``Array.<String>``

Список сокращенных наименований месяцев.

.. code:: json

    ["янв", "фев", "мар", "апр", "май", "июн", "июл", "авг", "сен", "окт", "ноя", "дек"]

dayNames
~~~~~~~~

Тип: ``Array.<String>``

Список наименований дней недели.

.. code:: json

    ["воскресенье", "понедельник", "вторник", "среда", "четверг", "пятница", "суббота"]

abbreviatedDayNames
~~~~~~~~~~~~~~~~~~~

Тип: ``Array.<String>``

Список сокращенных наименований дней недели.

.. code:: json

    ["Вс", "Пн", "Вт", "Ср", "Чт", "Пт", "Сб"]

dateSeparator
~~~~~~~~~~~~~

Тип: ``String``

Разделитель компонентов даты (год, месяц, день)

.. code:: json

    "."

timeSeparator
~~~~~~~~~~~~~

Тип: ``String``

Разделитель компонентов времени (час, минута, секунда).

.. code:: json

    ":"

amDesignator
~~~~~~~~~~~~

Тип: ``String``

Указатель часов до полудня (АМ — "ante meridiem").

.. code:: json

    "AM"

pmDesignator
~~~~~~~~~~~~

Тип: ``String``

Указатель часов после полудня (PМ — "post meridiem").

.. code:: json

    "PM"

firstDayOfWeek
~~~~~~~~~~~~~~

Тип: ``Integer``

Первый день недели.

.. code:: json

    1
