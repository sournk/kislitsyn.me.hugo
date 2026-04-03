---
title: 33. SMC Structure Trade
type: docs
prev: bots
next: 
sidebar:
  open: true
draft: false
publishDate: 2024-12-10
weight: 33
---
Testing the structure break trade hypothesis by SMC

* Created by Denis Kislitsyn | denis@kislitsyn.me | [kislitsyn.me](https://kislitsyn.me)
* Version: 1.00

## Что нового?
```
1.00: Первая версия
```

## Стратегия бота

1. Бот отслеживает структуру по правилам SMC/ICT на HTF.
2. После образования BOS или CHoCH бот ожидает отскока цены зону POI, определяемую уровнями Фибо.
3. Пока цена находится в POI бот на LFT ищет подтверждение разворота цены в сторону продолжения структуры одним из способов:
    - Гистограмма MACD пересекает сигнальную линию в нужном направлении и гистограмма находится в нужной части относительно нулевой линии.
    - RSI заходит в зону перекупленности/перепроданности и образует пик/впадину, что соответствует ожиданию разворота.
    - RSI заходит в зону перекупленности/перепроданности и образует пик/впадину самую высокую/глубокую за длительный период.
4. После получения подтверждения бот входит в сделку с SL на нижней границы структуры и TP на верхней границе.
5. Бот использует BE после прохождения 0.5 уровня Фибо.
6. Бот использует TSL после прохождения каждого следующего уровня Фибо.

![Bot Layout](UM001.%20Layout.png)

## Установка

1. **Обновите терминал MetaTrader 5 до последней версии:** `Help->Check For Updates->Latest Release Version`. 
    - Если советник или индикатор не запускается, то проверьте сообщения на вкладке `Journal`. Возможно вы не обновили терминал до нужной версии.
    - Иногда для тестирования советников рекомендуется обновить терминал до самой последней бета-версии: `Help->Check For Updates->Latest Beta Version`. На прошлых версиях советник может не запускаться, потому что скомпилирован на последней версии терминала. В этом случае вы увидите сообщения на вкладке `Journal` об этом.
2. **Скопируйте файл бота `*.ex5` в каталог данных** терминала `MQL5\Experts\`. Открыть каталог данных терминала `File->Open Data Folder`.
3. **Установите из MQL5 Market индикатор `Structure Blocks`: https://www.mql5.com/ru/market/product/115943
8. **Откройте график нужной пары**.
9. **Переместите советника из окна `Навигатор` на график**.
10. **Установите в настройках бота галочку `Allow Auto Trading`**.
11. **Включите режим автоторговли** в терминале, нажав кнопку `Algo Trading` на главной панели инструментов.


## Настройки бота

##### 1. SIGNAL (SIG)
- [x] `SIG_HTF`: SB Indicator TF for Structure Detect
- [x] `SIG_HTF_FF`: Entry Fibo zone level From
- [x] `SIG_HTF_FT`: Entry Fibo zone level To

- [x] `SIG_LTF`: SB Indicator TF for Structure Detect
- [x] `SIG_LTF_CMD`: Confirm Mode
- [x] `SIG_LTF_MACD_FEP`: MACD Fast EMA Period
- [x] `SIG_LTF_MACD_SEP`: MACD Slow EMA Period
- [x] `SIG_LTF_MACD_SP`: MACD Signal SMA Period

##### 2. FILTER IMPULSE PRICE ACTION (FIL)
- [x] `FIL_ENB`: Impulse Price Action Filter Enabled
- [x] `FIL_MFR`: Min Impulse Price Action Fibo Level
- [x] `FIL_SBD_MIN`: Min SB Depth allowed
- [x] `FIL_SBD_MAX`: Max SB Depth allowed

3. ENTRY (ENT)
- [x] `ENT_MMV`: Lot Size
- [x] `ENT_SL_ES`: SL Extra Shift, pnt

##### 5. MISCELLANEOUS (MS)
- [x] `MS_MGC`: Expert Adviser ID - Magic
- [x] `MS_EGP`: Expert Adviser Global Prefix
- [x] `MS_LOG_LL`: Log Level
- [x] `MS_LOG_FI`: Log Filter IN String (use `;` as sep)
- [x] `MS_LOG_FO`: Log Filter OUT String (use `;` as sep)
- [x] `MS_PHV`: Print Historical Event Data
- [x] `MS_COM_EN`: Comment Enable (turn off for fast testing)
- [x] `MS_COM_IS`: Comment Interval, Sec
- [x] `MS_COM_EW`: Comment Custom Window


