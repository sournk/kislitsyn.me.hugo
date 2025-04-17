---
title: 51. FridayGoldRush-MT5-Bot
type: docs
prev: bots
next: 
sidebar:
  open: true
draft: false
publishDate: 2025-02-07
weight: 51
---

Торговый советник **Friday Gold Rush** для MetaTrader 5 реализует очень простую эффективную стратегию, которую использует Andre Stagge.

* Created by Denis Kislitsyn | denis@kislitsyn.me | [kislitsyn.me](https://kislitsyn.me/personal/algo)
* Version: 1.00
* Free download [MQL5 Market](https://www.mql5.com/en/market/product/131729)

## Что нового?
```
1.00: First version
```

## Стратегия

На [форуме forexfactory](https://www.forexfactory.com/thread/1060592-ea-friday-gold-rush) нашел пост с элементарной стратегией для золота. 

> **Покупай золото в четверг в 14:45 и продавай в пятницу в 18:25. Эта элементарная стратегия показывает преимущество перед простым удержанием золота в 2024 году.**

![Friday Gold Rush vs Buy&Hold](UM001.%20EA%20vs%20BuyHold.png)

Советник не использует Take Profit, потому что закрытие происходит принудительно в определенное время. Stop loss можно установить по желанию или по результатам тестов.

## Тестирование
![Equity Graph 2024](UM002.%20Equity%202024.png)
![Backtest 2024](UM003.%20Backtest%202024.png)

## Параметры

##### 1. ENTER (ENT)
- [x] ENT_WD: Enter Weekday (0-SUN, 1-MON, ...)
- [x] ENT_HR: Enter Hour (0-23)
- [x] ENT_MN: Enter Min (0-59)
- [x] ENT_DIR: Enter direction 
- [x] ENT_LOT: Lot Size
- [x] ENT_SL_PNT: Stop loss, pnt (0-off) 

##### 2. EXIT (EXT)
- [x] `ENT_WD`: Exit Weekday (0-SUN, 1-MON, ...) 
- [x] `ENT_HR`: Exit Hour (0-23) 
- [x] `ENT_MN`: Exit Min (0-59)
   
##### 3. РАЗНОЕ (MS)
- [x] `MS_MGC`: Expert Adviser ID - Magic
- [x] `MS_EGP`: Expert Adviser Global Prefix
- [x] `MS_LOG_LL`: Log Level 
- [x] `MS_LOG_FI`: Log Filter IN String (use `;` as sep) 
- [x] `MS_LOG_FO`: Log Filter OUT String (use `;` as sep)
- [x] `MS_COM_EN`: Comment Enable (turn off for fast testing)
- [x] `MS_COM_IS`: Comment Interval, Sec