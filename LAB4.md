# ЛАБОРАТОРНАЯ РАБОТА. СБОР, ОБРАБОТКА И ВИЗУАЛИЗАЦИЯ ТЕСТОВОГО НАБОРА ДАННЫХ.
Отчет по лабораторной работе #2 выполнил:
- Рыжанков Илья Александрович
- РИ-210943
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | # | 20 |
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

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_2.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_3.PNG)

Оператор OR работает исправно, в данном случае обучился за 6 эпох.

Обучение оператору AND:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_4.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_5.PNG)

Оператор AND работает исправно, в данном случае обучился также за 6 эпох.

Обучение оператору NAND:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_6.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_7.PNG)

Оператор NAND работает исправно, в данном случае обучился быстрее остальных за 4 эпохи.

Обучение оператору XOR:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/4-1_8.PNG)

Оператор XOR не обучается, неважно сколько эпох. Одиночный перцептрон не может решить нелинейные задачи, XOR - является такой.

## Задание 2
### -

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

