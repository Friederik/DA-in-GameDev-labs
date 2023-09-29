# ЛАБОРАТОРНАЯ РАБОТА. ПЕРЦЕПТРОН
Отчет по лабораторной работе #4 выполнил:
- Рыжанков Илья Александрович
- РИ-210943/РИ-310943
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | # | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Ознакомиться с принципом работы перцептрона и реализовать его в Unity.

## Задание 1
### В проекте Unity реализовать перцептрон, который умеет производить вычисления.

С помощью предоставленных файлов и видео привожу скриншоты выполненного задания.

На пустой GameObject добавляю представленный скрипт перцептрона и устанавливаю 8 эпох обучения, далее подставляю значения для каждого логического блока.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-2.PNG)

Обучение оператору OR:

Оператор OR работает исправно, в данном случае обучился за 6 эпох.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_2.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_3.PNG)

Обучение оператору AND:

Оператор AND работает исправно, в данном случае обучился также за 6 эпох.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_4.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_5.PNG)

Обучение оператору NAND:

Оператор NAND работает исправно, в данном случае обучился быстрее остальных за 4 эпохи.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_6.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_7.PNG)

Обучение оператору XOR:

Оператор XOR не обучается, неважно сколько эпох. Одиночный перцептрон не может решить нелинейные задачи, XOR - является такой.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_8.PNG)

## Задание 2
### Построить графики зависимости количества эпох от ошибки обучения. Указать от чего зависит необходимое количество эпох обучения.

На графиках ось X - количество эпох (EP), ось - Y - общее количество ошибок (TE)

График для оператора OR:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-3_1.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-3_2.PNG)

График для оператора AND:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-3_3.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-3_4.PNG)

График для оператора NAND:

Можно заметит, что обучается быстрее всех.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-3_5.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-3_6.PNG)

График для оператора XOR:

Не обучается, угадывает некоторые значения вначале, но дальше работает абсолютно неправильно

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-3_7.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-3_8.PNG)

Необходимое количество эпох обучений не является постоянным для конкретного оператора, меняется при каждом запуске перцептрона. Но оно стремится к какому-то конкретному числу в каждом случае. Для OR и AND примерно 6 эпох. Для NAND - 4 эпохи. Для XOR такого числа нет, так как не обучается вовсе. Значит, можно сделать вывод, что количество эпох зависит от конкретной задачи, от изначально заданных значений весов.

## Задание 3
### -

## Выводы

Абзац умных слов о том, что было сделано и что было узнано.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**

