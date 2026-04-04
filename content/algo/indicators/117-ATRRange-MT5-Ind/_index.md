---
title: 117. ATRRange-MT5-Ind
type: docs
prev: bots
next: 
sidebar:
  open: true
draft: false
publishDate: 2026-04-03
weight: 117
---

* Coding by Denis Kislitsyn | denis@kislitsyn.me | [kislitsyn.me](https://kislitsyn.me/personal/algo)
* MQL5: [ATR Range Indicator](https://www.mql5.com/en/market/product/162717)
* Version: 1.00

## Что нового?
```
1.00: First version
```

## Описание

**ATRRange-MT5-Ind** — индикатор для MetaTrader 5, который строит каналы волатильности на основе ATR с тремя уровнями множителей.

![Layout](UM001.%20Layout.png)

### Принцип работы

Индикатор:
1. **Рассчитывает ATR** — использует стандартный Average True Range
2. **Рисует три канала** вокруг цены закрытия:
   - **Top1/Bottom1** (синие) — Close ± ATR × Multi1
   - **Top2/Bottom2** (оранжевые) — Close ± ATR × Multi2
   - **Top3/Bottom3** (красные) — Close ± ATR × Multi3
3. **Динамические уровни** — каналы автоматически расширяются/сужаются в зависимости от волатильности

## Установка

1. Скопируйте `ATRRange.mq5` в `MQL5/Indicators/`
2. Перекомпилируйте в MetaEditor
3. Добавьте индикатор на график

## Параметры

- **`ATR Period`**: Период ATR
  - По умолчанию: `14`

- **`Multi1`**: Множитель для первого канала
  - По умолчанию: `1.0`

- **`Multi2`**: Множитель для второго канала
  - По умолчанию: `2.0`

- **`Multi3`**: Множитель для третьего канала
  - По умолчанию: `3.0`

