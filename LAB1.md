# ЛАБОРАТОРНАЯ РАБОТА. КОНСТРУКЦИЯ ЯЗЫКА PYTHON НА ПРИМЕРЕ РЕАЛИЗАЦИИ ЛИНЕЙНОЙ РЕГРЕССИИ.
Отчет по лабораторной работе #1 выполнил:
- Рыжанков Илья Александрович
- РИ-210943/РИ-310943
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
### Написать программы Hello World на Python и Unity.

- Для Python в отчете привести скриншоты с демонстрацией сохранения
документа google.colab на свой диск с запуском программы, выводящей
сообщение Hello World.

![Image alt](https://github.com/Friederik/labs/blob/main/11.PNG)

![Image alt](https://github.com/Friederik/labs/blob/main/22.PNG)

- Для Unity в отчете привести скришноты вывода сообщения Hello
World в консоль.

![Image alt](https://github.com/Friederik/labs/blob/main/33.PNG)

## Задание 2
### В разделе «ход работы» пошагово выполнить каждый пункт с описанием и примером реализации задачи по теме лабораторной работы

1. Произвести подготовку данных для работы с алгоритмом линейной регрессии. 10 видов данных были установлены случайным образом, и данные находились в линейной зависимости. Данные преобразуются в формат массива, чтобы их можно было вычислить напрямую при использовании умножения и сложения.

- Скриншот:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/2-1.PNG)

2. Определите связанные функции. Функция модели: определяет модель линейной регрессии wx+b. Функция потерь: функция потерь среднеквадратичной ошибки. Функция оптимизации: градиентного спуска для нахождения частных производных w и b.

- Скриншот:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/2-2.PNG)

3. Начать итерацию

  Шаг 1. Инициализация и модель итеративной оптимизации:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/2-3_1.PNG)

  Шаг 2. На второй итерации отображаются значения параметров, значения потерь и эффекты визуализации после итерации:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/2-3_2.PNG)

  Шаг 3. Третья итерация показывает значения параметров, значения потерь ивизуализацию после итерации:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/2-3_3.PNG)

  Шаг 4. На четвертой итерации отображаются значения параметров, значения потерь и эффекты визуализации:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/2-3_4.PNG)

  Шаг 5. Пятая итерация показывает значение параметра, значение потерь и эффект визуализации после итерации:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/2-3_5.PNG)

  Шаг 6. 10000-я итерация, показывающая значения параметров, потери и визуализацию после итерации:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/2-3_6.PNG)

## Задание 3
### Изучить код на Python и ответить на вопросы

- Должна ли величина loss стремиться к нулю при изменении исходных данных? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ.

Ответ: При изменении исходных данных (массивов x и y) величина loss будет менятся. При большем разбросе точек  величина loss будет стремится к бесконечности, а при меньшем разбросе (точки стремятся к образованию прямой или уже образуют ее) величина loss будет стремится к нулю.

Изначальные данные:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-1_1.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-1_2.PNG)

Увеличенный разброс точек:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-2_1.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-2_2.PNG)

Точки образуют прямую (геометрическая прогрессия):

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-3_1.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-3_2.PNG)

- Какова роль параметра Lr? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ. В качестве эксперимента можете изменить значение параметра.

Ответ: Это параметр, который определяет размер шага для каждой итерации. Если брать шаг слишком большой, то не получится найти искомый минимум, мы будем постоянно перескакивать искомое минимальное значение. А при слишком малом значении понадобится слишком много итераций.

Изначальное значение Lr:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-4_1.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-4_2.PNG)

Слишком большое значение Lr:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-4_3.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-4_4.PNG)

Слишком малое значение Lr:

![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-4_5.PNG)
![Image alt](https://github.com/Friederik/DA-in-GameDev-labs/blob/main/3-4_6.PNG)

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

