---
title: 119. SessionRange-MT5-Ind
type: docs
prev: bots
next: 
sidebar:
  open: true
draft: false
publishDate: 2025-05-06
weight: 62
---

* Coding by Denis Kislitsyn | denis@kislitsyn.me | [kislitsyn.me](https://kislitsyn.me/personal/algo)
* MQL5: [Custom Session Range Indicator](https://www.mql5.com/en/market/product/162711)
* Version: 1.00

## Что нового?
```
1.00: First version
```

## Описание

**SessionRange-MT5-Ind** — индикатор для MetaTrader 5, который строит канал High/Low/Middle на основе заданной торговой сессии.

![Layout](UM001.%20Layout.png)

### Принцип работы

Индикатор:
1. **Определяет сессионный диапазон** — строит канал на основе high/low заданного временного окна
2. **Рисует три линии**:
   - **SessionTop** (синяя) — максимум сессии
   - **SessionMiddle** (серая пунктирная) — середина канала
   - **SessionBottom** (оранжевая) — минимум сессии
3. **Режим сессии (Mode)**:
   - `Previous Day` — для классического PDH/PDL (диапазон предыдущего дня)
   - `Current Day` — для отображения сессий текущего дня
4. **Поддерживает ночные сессии** — корректно обрабатывает переход через полночь
5. **Кэширует расчёты** — оптимизированная производительность

## Установка

1. Скопируйте `SessionRange-MT5-Ind.mq5` в `MQL5/Indicators/`
2. Перекомпилируйте в MetaEditor
3. Добавьте индикатор на график

## Параметры

- **`StartHour`**: Час начала сессии [0-23]
  - По умолчанию: `9`

- **`StartMin`**: Минута начала сессии [0-59]
  - По умолчанию: `0`

- **`EndHour`**: Час окончания сессии [0-23]
  - По умолчанию: `18`

- **`EndMin`**: Минута окончания сессии [0-59]
  - По умолчанию: `0`

- **`Mode`**: Режим сессии
  - `Current Day` — текущий день
  - `Previous Day` — предыдущий день
  - По умолчанию: `Current Day`

