---
title: 74. WC-MeanReversion-BBDC-MT5-Bot
type: docs
prev: bots
next: 
sidebar:
  open: true
draft: false
publishDate: 2025-07-23
weight: 74
---

WC: Mean reversion bot trades using Bollinger Bands and Donchian Chanel indicators

* Coding by Denis Kislitsyn | denis@kislitsyn.me | [kislitsyn.me](https://kislitsyn.me/personal/algo)
* Version: 1.00

## What's new?
```
1.00: First version
```

## How It Works?

1.  **📈 Buy:**
      - The price broke below the lower boundary of the Bollinger Bands but quickly returned.
      - At the same time, the price hasn’t updated its lows for a long time (according to the Donchian Channel).
      - This means sellers are weakening, and it’s a signal to go long.
2. **📉 Sell:**
      - The price went above the upper boundary of the Bollinger Bands but then returned back.
      - Meanwhile, the price hasn’t updated its highs for a long time (according to the Donchian Channel).
      - This may be a sign that the upward movement has ended, and the price is ready to decline.
3. 📏 Risk Management:
      -  Stop Loss and Take Profit are automatically calculated by the bot based on current volatility using the ATR (Average True Range) indicator.
4. ❌ Exiting a Position:
      - If the price goes beyond the boundaries of the Donchian Channel, the bot closes the trade.  

## Installation | Установка

**RU:** Пошаговую инструкцию по установке торговых советников и индикаторов читай [README_INSTALL.md](README_INSTALL.md)
**EN:** For step-by-step instructions on installing Expert Advisors and indicators read [README_INSTALL.md](README_INSTALL.md).

## Bot's Input

#### 1. TRADE
- [x] `Magic(20250723)` - Bot's ID
- [x] `Lots(0)` - Lot Size
- [x] `BPeriod(100)` -  Bollinger Bands: Period
- [x] `BDeviation(1)` - Bollinger Bands: Deviation
- [x] `DonchPeriod(100)` -  Donchian Chanel: Period
- [x] `CPeriod(100)` -  Check trend Period (Max and Min prices rise or fall on this period)
- [x] `AtrPeriod(21)` - ATR: Period
- [x] `Stop(4)` - SL ATR Ratio
- [x] `Take(4)` - TP ATR Ratio
- [x] `Slippage(30)` - Max slippage allowed

#### 2. HARD SL
- [x] `HSLDay(31)` - Hard SL: Period to get profit, days (0-off)
- [x] `HSLLoss(100)` - Hard SL: Max loss allowed, account currency

#### 3. TIME FILTER
- [x] `F_TIM_MON("07:00-22:00")` - Mon allowed intervals "HH:MM(:SS)" (''-N/A; ';'-sep) 
- [x] `F_TIM_TUE("07:00-22:00")` - Tue allowed intervals "HH:MM(:SS)" (''-N/A; ';'-sep)
- [x] `F_TIM_WED("07:00-22:00")` - Wed allowed intervals "HH:MM(:SS)" (''-N/A; ';'-sep)
- [x] `F_TIM_THU("07:00-22:00")` - Thu allowed intervals "HH:MM(:SS)" (''-N/A; ';'-sep) 
- [x] `F_TIM_FRI("07:00-22:00")` - Fri allowed intervals "HH:MM(:SS)" (''-N/A; ';'-sep) 
- [x] `F_TIM_SAT("")` - Sat allowed intervals "HH:MM(:SS)" (''-N/A; ';'-sep) 
- [x] `F_TIM_SUN("")` - Sun allowed intervals "HH:MM(:SS)" (''-N/A; ';'-sep) 