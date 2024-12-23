---
title: 06. Подбор параметров для двух периодов, когда Ева сливала депозит
type: docs
prev: 
next: 
weight: 6
publishDate: 2023-10-13
---

В тестере стратегий запустил перебор параметров своего робота, чтобы найти их сочетание для прохождения двух периодов, когда оригинальная Ева 100% сливает депозит: 
- в сентябре 2023 (слив реальных депозитов);
- в мае 2019 (по результатам бэктестов). 

Подобрать параметры для прохождения "сложных" периодов оказалось просто. Ниже отчеты о прохождении Евой на галоперидоле этих периодов с прибылью и минимальной просадкой депозита. 

![Май 2019](/images/personal/040/2019-05%20-%20Tester%20Report.png)
![Сентябрь 2023](/images/personal/040/2023-09%20-%20Tester%20Report.png)

Подбирал параметры для лота 0.1 на $10000 депозита как и прошлых бэктестах:
- Размер сетки, ограничив 16 ордерами.
- Шаг открытия ордеров.
- Дистанция до Take-Profit.
- Разные таймфреймы ордеров после 10-го.

Есть конечно ложка дегтя - найденные параметры хорошо проходят периоды "пике" цены, но имеют низкую прибыль в других периодах. Правда успел проверить всего несколько месяцев. И еще в некоторые месяцы такие настройки долго держат открытые сетки - 5 и более дней.

Пока продолжаю оптимизатором искать лучшие параметры и придумывать как на ходу роботу подстраивать параметры под конкретную ситуацию с ценой, чтобы периоды "пике" проходить аккуратно и возвращаться к настройкам, близким к оригинальной Еве в остальные периоды.

To be continued...