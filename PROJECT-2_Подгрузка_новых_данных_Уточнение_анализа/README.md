# Проект 2. Подгрузка новых данных. Уточнение анализа 

## Оглавление
[1. Описание проекта](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-0_Угадай_число/README.md#Описание-проекта)

[2. Какой кейс решаем?](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-0_Угадай_число/README.md#Какой-кейс-решаем)

[3. Краткая информация о данных](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-0_Угадай_число/README.md#Краткая-информация-о-данных)

[4. Этапы работы над проектом](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-0_Угадай_число/README.md#Выводы)

[5. Результат](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-0_Угадай_число/README.md#Результат)

[6. Выводы](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-0_Угадай_число/README.md#Выводы)

### 1. Описание проекта
Большинство крупных компаний хранят данные в реляционных базах, так как в таком виде они более структурированы и адаптированы для внешних систем, с помощью которых, как правило, данные в базу и заносятся. В системах с такими базами данных имеют значение именно отношения между сущностями. Если вам понадобилось, например, посчитать статистику по заказам, то здесь важны отношения: заказ, клиент, товар и т. д.

Реализация данного проекта подразумевает практику в этой области.

:arrow_up:[к оглавлению](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-0_Угадай_число/README.md#Оглавление)

### 2. Какой кейс решаем?
В ходе реализации проекта еобходимо будет познакомиться с данными реляционного датасета hh.ru, понять, с какими резюме мы имеем дело, собрать статистику для различных кадровых агентств и статистических центров.

**Условия задания:**

На основе данные по возрасту кандидатов, по городам с наиболее активным рынком труда изучим специфику найма (где какие вакансии более активны), а также узнаеем желаемые позиции для тех или иных кандидатов.

**Что практикуем:**
- SQL.

:arrow_up:[к оглавлению](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-0_Угадай_число/README.md#Оглавление)

### 3. Краткая информация о данных

На диаграмме мы видим четыре таблицы:

![изображение](https://user-images.githubusercontent.com/96936125/179499408-0f4958ad-9e08-4a9d-9aeb-3c6c25263efe.png)
 
CANDIDATE
Таблица хранит в себе общие данные по кандидатам: id, пол, возраст, желаемая должность, город, вид занятости, текущая должность, дата обновления записи и зарплата.

![изображение](https://user-images.githubusercontent.com/96936125/179499462-0fd9ea3b-526c-4495-a939-5a4899c64ef0.png)

CITY
city — таблица-справочник для наших кандидатов — хранит код города и его название.

![изображение](https://user-images.githubusercontent.com/96936125/179499493-ca2fb2a1-6d8b-47bc-8eab-196fb24e4719.png)

CANDIDATE_TIMETABLE_TYPE
Это дополнительная таблица. Она существует для организации связи многие-ко-многим, так как у нас есть много кандидатов и у них может быть несколько подходящих типов рабочего графика.

![изображение](https://user-images.githubusercontent.com/96936125/179499528-e45999e7-2238-4e2a-a536-957c116e26fa.png)

TIMETABLE_TYPE
Это таблица-справочник вариантов рабочего графика, подходящего кандидату.
 
![изображение](https://user-images.githubusercontent.com/96936125/179499553-d6f8ec85-33e3-4ac4-a3fc-d3e2390d14a2.png)

### 4. Этапы работы над проектом

1. знакомство с датасетом;
2. предварительный анализ данных;
3. анализ кандидатов;
4. глобальный анализ показателей.

### 5. Результат

Результатом анализа является Аналитическая справка с сформулированными выводами.

### 6. Выводы

Для анализа представлены данные по 44744 соискателям. Из них два кандидата указали возраст, выходящий за возрастные рамки “среднестатистического” работника: 100 лет (принято решение исключить эти данные из дальнейшего анализа) и 14 лет.
При дополнительном анализе было выявлено, что вероятнее всего и указанный возраст 14 лет является ошибкой, однако данные по этому кандидату исключены не были для соответствия полученных ответов.

Дальнейший анализ соискателей в разрезе возраста показал, что количество соискателей старше среднего возраста занятых в экономике России (в расчетах 40 лет) составляет всего 14% от общего числа соискателей, т.е. граждане России старше 40 лет по тем или иным причинам имеют более консервативный взгляд на смену места работы (устраивает место работы, нет веры в возможность смены места работы, …).
Еще меньшую долю составляют соискателей пенсионного возраста (0,2%), что является закономерным. В связи с тем, что соискатели пенсионного возраста обычно более лояльны и к условиям работы, и к работодателю, следует провести дополнительные исследования по желаемым профессиям таких соискателей с целью предоставления полученной выборки соответствующим заказчикам.

При анализе данных в разрезе городов был сделан вывод, что у Москвы значительный отрыв от остальных городов по числу соискателей, разместивших свои резюме (второе место за Санкт-Петербургом). В целом полученный вывод соответствует как картине рынка труда по России, так и демографическим показателям городов (число жителей) Однако по представленным данным нет возможности дать точную оценку полученному выводу, так как нет ясности о каком именно городе представлены данные (о том, где проживает соискатель, или о том, в каком городе он ищет работу). Для этого необходимо уточнение данных о городах в таблице candidate, и, вероятнее всего, разделение данных на два признака: “город проживания”, “город, в котором ищет работу”.
Анализ данных по желаемым профессиям было выявлено, что большое число желаемых профессий составляют профессии из IT-отрасли. Проанализировав данные по самым популярным IT-профессиям (разработчик, аналитик, программист) мы получили вывод, что основную масса соискателей на эти профессии составляют мужчины возрастом до 40 лет. 

Схожая картина и в Москве по соискателям, готовым к “проектной работе”: большинство желали бы продолжить или связать свою трудовую деятельность с IT-отраслью: программирование, аналитика, разработка, … 
