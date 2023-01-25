# SQL_database_of_site

   В базе данных (БД) Novosibirsk_n1.sql я постарался воспроизвести базу данных сайта https://novosibirsk.n1.ru/ (к сожалению позже этот сайт купил ЦИАН и переделал). У меня не было возможности
использовать API компании 2GIS, используемое на сайте, поэтому я заменил схемы из этого API на схемы, расположенные в таблице apartments_maps и упростил привязку объектов к метро таблицами metro и переходной таблицей apartments_metro.
   Из-за большого объема БД сайта https://novosibirsk.n1.ru/ и сжатых сроков сдачи проекта, я обошелся только одним типом недвижимости - 
квартирами. Но в мой проект можно легко добавить другие типы недвижимости созданием соответствующих таблиц недвижимости по аналогичной схеме, как и с квартирами. Также для ускорения я не стал указывать филиалы пользователей, т.к. это добавило бы очень много работы. Телефон каждому пользователю был добавлен в одном экземпляре.
   БД в файле novosibirsk_n1.sql содержит следующие таблицы (которые содержат):
   
   - realty: Тип недвижимости (квартиры, участки и т.д.)
   - rooms: Количество комнат в квартире, студии и т.д.
   - district: Районы г. Новосибирска
   - metro: Станции метро в Новосибирске
   - microdistrict: Микрорайоны г. Новосибирска
   - streets: улицы г. Новосибирска
   - bathroom_unit: Тип санузла
   - material: Материалы стен зданий
   - hometype: Типы домов (Малоэтажка, Хрущевка и т.д.)
   - layout: Планировки квартир
   - type_apartment: Типы квартир (Индивидуальной планировки, гостинка и т.д.)
   - type_owner: Типы пользователей сайта
   - owner: Пользователи сайта
   - apartments:Квартиры в БД
   - apartments_metro: Промежуточная таблица между квартирами и станциями метро
   - apartments_maps: Схемы квартир
   - apartments_photos: Фото квартир
   - messages: Сообщения между пользователями через мессенджер сайта
   - logs: Журнал находящихся в БД квартир
   - residential_complex: Жилые комплексы
   - apartments_residential_complex: Промежуточная таблица между жилыми комплексами и квартирами

   Схема используемых таблиц находится в файле DIAGRAMM_NSK_N1.png.
   
   В файле Views_nsk_n1.sql я создал 4 представления.

   В файле Procedurs_nsk_n1.sql я создал 2 процедуры.

   В файле Triggers_nsk_n1.sql я создал 3 триггера.
   
   В файле Select_nsk_n1.sql я создал 3 поиска.