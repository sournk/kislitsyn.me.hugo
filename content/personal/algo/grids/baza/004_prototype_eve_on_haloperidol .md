---
title: 05. Ева на галоперидоле
type: docs
prev: 
next: 
weight: 5
publishDate: 2023-10-10
---
Переписал алгоритм Евы на MQL5 с нуля. Сделал все настройки доступными для редактирования и очень гибкими. Аккуратно их изменяя можно из Евы даже почти Гермес сделать. Правда без SL пока и трейлинга. Настраивается практически все. Конечно можно отстрелить себе ногу, выставляя их бездумно, но для экспериментов без этого не обойтись.
1. **Максимальное количество ордеров в сетке**. Попробую ограничить Еву 15-ю или 16-ю ордерами и прогнать тесты. Сравнить как упадет прибыль в "тихие" месяцы по сравнению с оригиналом, и как в таком случае она выберется из всех месяцев, где требуются доливы на рекомендованных настройках.  
1. **Таймфрейм каждого ордера сетки**. Ева с 1-го по 10-ый контролит на M1, далее на M5. В галоперидольной Еве можно задать любой таймфрейм для каждого ордера. Планирую протестировать так, чтобы 15-ый ордер и далее брались на M15 или даже M30 и более, чтобы уменьшить скорость роста сетки.
2. **Настройки коэффициента лота следующего ордера сетки**. По умолчанию взял настройки из своих бэктестов, потому что на больших сетках коэффициенты ордеров после 16 в них 1.3, а не 1.65 как указано в таблицах группы AKKURANTO. Тоже планирую тестировать с разными вариантами, чтобы не так быстро сетки росли после 15-го ордера.
3. **Запрет открытия новых ордеров при просадке в USD и % от депозита**.

На нескольких месяцах уже прогнал свою Еву и сравнил с оригиналом. Прибыли и просадки очень близки друг у другу. Несколько больших сеток совпадают по лотности на 100%, а по цене с учетом погрешности на разные ТВХ. Все это говорит, о том что алгоритм очень близок к оригиналу. Хотя не все детали реализации Евы известны, а только основная логика сеточника с усреднением. Хорошо, что она простая и прямолинейная. Причем описана и реализована десятки раз.

Далее хочу тщательнее прогнать тесты новой Евы, чтобы убедиться, что все работает аналогично оригиналу. А далее буду экспериментировать с настройками, чтобы избежать сливов, пробуя разные варианты защиты от этого. Успокоить так сказать Еву, посадив на успокоительные.