---
title: 66. PADD-Fractal-MT5-Ind
type: docs
prev: bots
next: 
sidebar:
  open: true
draft: false
publishDate: 2025-05-21
weight: 66
---

* Coding by: Denis Kislitsyn | denis@kislitsyn.me | [kislitsyn.me](https://kislitsyn.me)
* Версия: 1.01

![Layout](UM001.%20Layout.png)

Indicator offers flexible fractal configuration, including the number of candles to the left and right, and the ability to filter based on sorted high/low values.

Key Features
	•	Detects upward or downward fractals
	•	Configurable number of candles on both sides
	•	Optional sorting checks for high/low values
	•	Arrow drawing on the chart

Parameters

1. Main (B)
	•	Fractal Type (InpFractalType): Up / Down
	•	Arrow Code (InpArrowCode): Unicode symbol for arrow
	•	Arrow Color (InpArrowColor): Color for drawing

2. Filters (F)
	•	Bars Left/Right (InpLeftBarCount / InpRightBarCount): Number of candles to check before and after
	•	Sorted High/Low Left/Right: Boolean filters for sorting

3. Misc (M)
	•	Log Level (InpLogLevel): ERROR, INFO, etc.
	•	Global Prefix (InpGlobalPrefix): For buffer IDs