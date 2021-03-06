# Проект 1. Анализ вакансий из HeadHunter

## Оглавление
[1. Описание проекта](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Описание-проекта)

[2. Какой кейс решаем?](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Какой-кейс-решаем)

[3. Краткая информация о данных](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Краткая-информация-о-данных)

[4. Этапы работы над проектом](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Выводы)

[5. Результат](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Результат)

[6. Выводы](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Выводы)

### 1. Описание проекта
В нашем распоряжении будет база резюме, выгруженная с сайта поиска вакансий hh.ru (ссылка: https://drive.google.com/file/d/1Kb78mAWYKcYlellTGhIjPI-bCcKbGuTn/view?usp=sharing), анализ которой необходимо провести с ипользованием инструментов Python.

:arrow_up:[к оглавлению](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Оглавление)

### 2. Какой кейс решаем?

Проблематика: часть соискателей не указывает желаемую заработную плату, когда составляет своё резюме.

Решаемая в данном проекте задача:  преобразование, исследование и очистка данных для последующего построения модели, которая бы автоматически определяла примерный уровень заработной платы, подходящей пользователю, исходя из информации, которую он указал о себе.

**Что практикуем**

Применение методов работы с данными библиотки Pandas.

:arrow_up:[к оглавлению](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Оглавление)

### 3. Краткая информация о данных

Датасет предстлвляет собой csv-файл с таблицей, сосотоящей из 12 столбцов и 44743 строки. 
Столбцы в таблице:

 1.  Пол, возраст;                    
 2.  ЗП;                              
 3.  Ищет работу на должность:;        
 4.  Город, переезд, командировки;     
 5.  Занятость;                        
 6.  График;                           
 7.  Опыт работы;                      
 8.  Последнее/нынешнее место работы;  
 9.  Последняя/нынешняя должность;     
 10. Образование и ВУЗ;                
 11. Обновление резюме;                
 12. Авто.           

:arrow_up:[к оглавлению](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Оглавление)

### 4. Этапы работы над проектом

Проект состоит из четырёх частей:

1. базовый анализ структуры данных;
2. преобразование данных;
3. разведывательный анализ;
4. очистка данных.

В каждой части необходимо решить ряд практических задач. Решения необходимо выполнить в jupyter-ноутбуке.

:arrow_up:[к оглавлению](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Оглавление)

### 5. Результат

В результате был получен датасет, пригодные для последующего построения модели, которая бы автоматически определяла примерный уровень заработной платы, подходящей пользователю, исходя из информации, которую он указал о себе.

:arrow_up:[к оглавлению](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Оглавление)

### 6. Выводы

1. готовность к переезду и командировкам сильно повышает уровень заработной платы. Вероятно это связано с тем, что командируемые - это, как правило, люди занимающие высокие должности;
2. для категорий "среднее специальное" и "среднее" образование медианная заработная плата слабо растет с увеличением возраста, в отличие от высшего образования и неоконченного высшего;
3. наблюдается прямая зависимость опыта работы от возраста. Точки лежащие на прямой и находящиеся выше нее - аномальные значения опыта работы, равного или превышающего возраст соискателя.

:arrow_up:[к оглавлению](https://github.com/IShinkarev/sf_data_sience/tree/main/PROJECT-1_Анализ_вакансий_из_HeadHunter/README.md#Оглавление)
