
# Ballistic.py

Ballistic.py -- скрипт для решения задачи внешней баллистики с учетом влияния воздушных условий

Требования
---

Для запуска данного скрипта требуется установленный ```python 3``` со следующими библиотеками:
* numpy
* scipy

Запуск
---

Команда для запуска скрипта со всеми параметрами по умолчанию. В качестве параметров по умолчанию взяты значения, указанные в "данных для отладки" текста Задания; таким образом, достаточно переопределить лишь те параметры, значение для которых отличается от таковых.

    $ ./ballistic.py
    
Пример команды для запуска скрипта с явным заданием всех возможных параметров. Смысл каждого из них разъяснен в разделе [Описание аргументов командной строки](#variables)

    $ ./ballistic.py --mass 1707 --height 495 --velocity 42 -F F_data.csv -W Wind_data.csv

<a name='variables'></a>
Описание аргументов командной строки
---

|**Аргумент**|**Описание**                                   |**Значение по умолчанию**|
|:----------:|:---------------------------------------------:|:-----------------------:|
|MASS        |Масса груза                                    |100                      |
|HEIGHT      |Высота сброса груза                            |1000                     |
|VELOCITY    |Начальная скорость груза                       |250                      |
|F           |Путь к файлу с данными об аэродинамической силе|F.csv                    |
|W           |Путь к файлу с данными о поле ветра            |Wind.csv                 |

Результат работы
---

В случае успешного выполнения скрипта в директории с исполняемым файлом появится текстовый файл ```Ballistic.csv``` с расчетными данными в виде таблицы со следующими столбцами:
* время
* координата X
* координата Y
* координата Z
* проекция скорости на координату X
* проекция скорости на координату Y
* проекция скорости на координату Z
