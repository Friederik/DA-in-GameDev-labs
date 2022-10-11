# ЛАБОРАТОРНАЯ РАБОТА. СБОР, ОБРАБОТКА И ВИЗУАЛИЗАЦИЯ ТЕСТОВОГО НАБОРА ДАННЫХ.
Отчет по лабораторной работе #2 выполнил:
- Рыжанков Илья Александрович
- РИ-210943
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

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
Ознакомиться с основными операторами языка Python на примере реализации линейной регрессии.

## Задание 1
### Реализовать совместную работу и передачу данных в связке Python - Google-Sheets – Unity.

С помощью предоставленных файлов и видео привожу скриншоты выполненного задания

- В облачном сервисе google console подключить API для работы с google
sheets и google drive.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/111.PNG)

- Реализовать запись данных из скрипта на python в google-таблицу.
- Ссылка на таблицу https://docs.google.com/spreadsheets/d/1KHek-z6fytXRC-yw9gpJICnswzhvAuW64lxq4sPL5Cs/edit#gid=0

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/222.PNG)

- Создать новый проект на Unity, который будет получать данные из google-
таблицы, в которую были записаны данные в предыдущем пункте.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/333-1.PNG)

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/333-2.PNG)

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/333-3.PNG)

- Написать функционал на Unity, в котором будет воспризводиться аудио-
файл в зависимости от значения данных из таблицы.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/444.PNG)

## Задание 2
### Реализовать запись в Google-таблицу набора данных, полученных с помощью линейной регрессии из лабораторной работы № 1

- Скриншот таблицы:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/333-3.PNG)

- Ссылка на таблицу: https://docs.google.com/spreadsheets/d/1Uugw6_RrE4lGzw0dfHbWo2cmO1DOUuHJcA3lz9v2yGs/edit#gid=0

- Код:

```py

import numpy as np
import gspread
gc = gspread.service_account(filename='lab2-365217-74eeef80a64e.json')
sh = gc.open("Lab2Sheets")

x = [3, 21, 22, 34, 54, 34, 55, 67, 89, 99]
x = np.array(x)
y = [2, 22, 24, 65, 79, 82, 55, 130, 150, 199]
y = np.array(y)


def model(a, b, x):
    return a*x + b


def loss_function(a, b, x, y):
    num = len(x)
    prediction = model(a, b, x)
    return (0.5/num) * (np.square(prediction-y)).sum()


def optimize(a, b, x, y):
    num = len(x)
    prediction = model(a, b, x)
    da = (1.0/num) * ((prediction -y)*x).sum()
    db = (1.0/num) * ((prediction -y).sum())
    a = a - Lr*da
    b = b - Lr*db
    return a, b


def iterate(a, b, x, y, times):
    for i in range(times):
        a, b = optimize(a, b, x, y)
    return a, b


a = np.random.rand(1)
b = np.random.rand(1)
Lr = 0.000001
counter = 30

while counter <= 45:
    counter += 1
    a, b = iterate(a, b, x, y, counter)
    loss = loss_function(a, b, x, y)
    sh.sheet1.update(('A' + str(counter-30)), str(counter-30))
    sh.sheet1.update(('B' + str(counter-30)), str(a))
    sh.sheet1.update(('C' + str(counter-30)), str(b))
    sh.sheet1.update(('D' + str(counter-30)), str(int(loss)))
    print(a, b, loss)

```

## Задание 3
### Самостоятельно разработать сценарий воспроизведения звукового сопровождения в Unity в зависимости от изменения считанных данных в задании 2

- В зависимости от погрешности воспроизводится определенный аудио-файл.

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/666.PNG)

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/777.PNG)

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

