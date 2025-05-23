---
title: 32. Advanced Fractal Sweep
type: docs
prev: bots
next: 
sidebar:
  open: true
draft: false
publishDate: 2024-11-30
weight: 32
---

Торговый советник для MetaTrader 5, которые торгует отскоки от фильтрованных уровней фракталов

* Created by Denis Kislitsyn | denis@kislitsyn.me | [kislitsyn.me](https://kislitsyn.me)
* Version: 1.11

{{< callout type="warning">}}
Бот не гарантирует прибыль. Бот не гарантирует 100% защиты депозита. Используйте бота на свой страх и риск.
{{< /callout >}}

![Layout](UM001.%20Layout.png)

## Что нового

```
1.11: [*] Исправлена ошибка неверного расчета позиций закрытых по SL с перепутанным BUY/SELL.
1.10: [*] Исправлена ошибка неверного расчета позиций закрытых по SL из точного сравнения double.
1.09: [*] Релиз без ограничений.
1.08: [*] Исправлена ошибка фильтра по количеству позиций в рынке для одновременного открытия нескольких позиций от разных фракталов.
1.07: [*] 'FRCN' теперь проверяет мин дистанцию от фрактала до O или C свечи, в зависимости, что меньше.
1.06: [+] Подключен индикатор фракталов 'MT5 Fractal Indicator'.
1.05: [*] Уровень фрактала остается активным при касании пункт в пункт.
1.04: [+] Добавлены параметры '*_FRCN' - мин. дистанция от фрактала до закрытия пробивающей свечи.\r\n1.03: [+] Фильтр исчезающих фракталов Williams.\r\n1.02: [*] Исправлена ошибка перепутанных фильтров для разных режимов.
1.03: [+] Фильтр исчезающих фракталов Williams.
1.02: [*] Исправлена ошибка перепутанных фильтров для разных режимов.
1.01: [+] Фракталы Williams.
1.00: [+] Релиз.
```

## Установка

1. **Обновите терминал MetaTrader 5 до последней версии:** `Help->Check For Updates->Latest Release Version`. 
    - Если советник или индикатор не запускается, то проверьте сообщения на вкладке `Journal`. Возможно вы не обновили терминал до нужной версии.
    - Иногда для тестирования советников рекомендуется обновить терминал до самой последней бета-версии: `Help->Check For Updates->Latest Beta Version`. На прошлых версиях советник может не запускаться, потому что скомпилирован на последней версии терминала. В этом случае вы увидите сообщения на вкладке `Journal` об этом.
2. **Скопируйте файл бота `*.ex5` в каталог данных** терминала `MQL5\Experts\`. Открыть каталог данных терминала `File->Open Data Folder`.
3. **Скопируйте файл индикатора `*.ex5` в каталог данных** терминала `MQL5\Indicators\`. Открыть каталог данных терминала `File->Open Data Folder`.
4. **Установите бесплатный индикатор `Structure Blocks`** из маркета MetaTrader 5. Введите в строку поиска "Structure Blocks" и в открывшемся окне нажмите установить. Установка из маркета возможна только после логина в телеграмме в ваш аккаунт MetaQuotes.
5. **Откройте график нужной пары**.
6. **Переместите советника из окна `Навигатор` на график**.
7. **Установите в настройках бота галочку `Allow Auto Trading`**.
8. **Включите режим автоторговли** в терминале, нажав кнопку `Algo Trading` на главной панели инструментов.

## Требования

1. [x] **СИГНАЛ: Поиск неснятых фракталов для потенциального входа.** 
    На каждой новой свече **выбранного на графике ТФ** бот находит все фракталы снизу и сверху. От каждого из них он строит уровни вправо. Все пробитые уровни бот перестает отслеживать на пробитие. Список уровней, который бот мониторит выведены в окно сообщений.
2. [x] **СИГНАЛ: Поиск снятых фракталов тенью**
    На каждой новой свече **выбранного на графике ТФ** бот проверяет снимает ли прошлая свеча какой-то уровень своим фитилем, а не телом. 
3. [x] **СИГНАЛ: Проверка фрактальных расстояний для корректного сигнала**
    Далее бот проверяет снятый уровень фрактала на допуски по его расстояниям: до фитиля снявшей уровень свечи, до ее закрытия, до прошлого фрактала.
4. [x] **ВХОД: Отдельные настройки для: тренд, против и флэт**
    У бота отдельные настройки для входа в сделку по тренду, против и флэту.
5. [x] **ВХОД: Отдельные настройки для сделок после 17:00**
    Также выделены настройки для входов после 17:00.
6. [x] **ВХОД: Перерасчет лота под маржу на аккаунте**
    Если после открытия позиции указанным лотом свободная маржа аккаунта превысит 50% баланса, то бот уменьшит лот так, чтобы не превышать это значение.
7. [x] **ФИЛЬТР: Единственная сделка в рынке**
    Фильтр проверяет и ограничивает входы, если уже есть открытые позиции.
8. [x] **ФИЛЬТР: Время работы**
    Бот не открывает позиции вне указанного времени.
9. **ФИЛЬТР: Торговля в новости**
    Бот не открывает позиции в указанный диапазон вокруг новости. Бот выбирает новости из встроенного в терминал календаря MetaQuotes, которые касаются выбранного на графике символа. В настройках можно указать новости какой важности нужно фильтровать.
    > **ВАЖНО:**
    Фильтр новостей не работает в тестере, потому что терминал не имеет доступ к календарю в нем.
10. [x] **ФИЛЬТР: Макс. количество сделок в день**
    Бот проверяет сколько сделок закрыто за сегодня и при превышении указанного значения перестает открывать позиции.
11. [x] **ФИЛЬТР: Макс. количество SL в день**
    Бот проверяет сколько сделок закрыто за сегодня по SL и при превышении указанного значения перестает открывать позиции.
12. [x] **ФИЛЬТР: Тренд**
    Бот определяет тренд с помощью индикатора `Structure Blocks` по тем же правилам, что в боте `OK-SymExp-MT5-Bot`. 
    Бот может определять тренд на отличном от выбранного на графике ТФ. Его можно задать в настройках. 
13. [x] **ФИЛЬТР: Спред и проскальзывание**
    Бот может отфильтровывать сделки, если в момент входа спред превышает указанное значение. Максимальное проскальзывание бот передает брокеру в приказе на открытие позиции. Исполнение этого правила выполняет брокер по его правилам.
14. [x] **ФИЛЬТР: Ценовой гэп**
    Бот может отфильтровать сделки, если ценовой гэп на соседних свечах превышает указанное значение.
15. [x] **ВЫХОД: Принудительное закрытие ордеров в конце дня**
    Бот может принудительно закрывать позиции в указанное время.
16. [x] **ДОП: Полное логирование**
    Все операции бот записывает в стандартный лог терминала с разными уровнями важности:
        - `DEBUG`: Любая выполненная проверка входа для каждого фрактала будет записана в лог.
        - `INFO`: С этим уровнем записываются успешные события: прохождения фильтров, загрузки новостей или изменения параметров открываемых позиций.
        - `WARN`: Любые операции с рынком записываются с этим уровнем.
        - `ERROR` и `CRITICAL` бот использует для записи об ошибках.
17. [x] **ДОП: Защита от повторных запуске на одном инструменте**
    Бот проверяет запуск на другом графике и таком же инструменте. Если находит уже запущенный бот, то выдает предупреждение.
18. [x] **ДОП: Защита от внешних факторов и синхронизация при сбое**
    После любых ошибок бот пытается повторить операции, пока они актуальны.

## Настройки

#### 1. СЕТАП (SET)
- [x] `FDP`: Глубина поиска фракталов, баров
- [x] `FRT`: Тип фрактала: `PADD` или `Williams`
- [x] `FPD_FBC`: Количество баров вокруг пика фрактала, шт
- [x] `FPD_FPS`: Пики баров фрактала упорядочены
- [x] `FPD_FBS`: Основания баров фрактала упорядочены
- [x] `TTF`: TF определения тренда

#### 2. ВХОД (ENT)
- [x] `GN_SLPG`: Max проскальзывание, пункт (0-откл)
- [x] `GN_MGPR`: Max доля маржи от баланса после входа, % (0-откл)

#### 2.1. ВХОД ПО ТРЕНДУ ↑↑/↓↓ (ENT)
- [x] `OT_LOT`: ↑↑/↓↓: Лот
- [x] `OT_SLD`: ↑↑/↓↓: Стоплосс, пункт
- [x] `OT_TPD`: ↑↑/↓↓: Тейкпрофит, пункт

#### 2.2. ВХОД ПРОТИВ ТРЕНДА ↑↓/↓↑ (ENT)
- [x] `AT_LOT`: ↑↓/↓↑: Лот
- [x] `AT_SLD`: ↑↓/↓↑: Стоплосс, пункт
- [x] `AT_TPD`: ↑↑/↓↓: Тейкпрофит, пункт

#### 2.3. ВХОД ВО ФЛЭТЕ → (ENT)
- [x] `FL_LOT`: →: Лот
- [x] `FL_SLD`: →: Стоплосс, пункт
- [x] `FL_TPD`: →: Тейкпрофит, пункт

#### 2.4. ВХОД ПОСЛЕ ВРЕМЕНИ T (ENT)"
- [x] `TM_HRS`: T: Час начала (>24-откл)
- [x] `TM_LOT`: T: Лот
- [x] `TM_SLD`: T: Стоплосс, пункт
- [x] `TM_TPD`: T: Тейкпрофит, пункт

#### 3. ФИЛЬТРЫ (FIL)"
- [x] `GN_SLD`: Max спред, пункт (0-откл)
- [x] `GN_PGAP`: Max ценовой гэп, пункт (0-откл)
- [x] `GN_POPN`: Max кол-во позиций в рынке, шт (0-откл)
- [x] `GN_PPDN`: Max кол-во позиций в день, шт (0-откл)
- [x] `GN_PSLN`: Max кол-во SL позиций в день, шт (0-откл)
- [x] `TM_STRT`: Время начала открытия позиций (формат HH:MM)
- [x] `TM_FNSH`: Время окончания открытия позиций (формат HH:MM)
- [x] `TM_CLEN`: Закрыть позиции принудительно в HH:MM
- [x] `TM_CLTM`: Время принудительного закрытия позиций (формат HH:MM)
- [x] `NS_ENBL`: Включить фильтр новостей (не работает в тестере)
- [x] `NS_FRMN`: Фильтровать до выхода новости, мин
- [x] `NS_TOMN`: Фильтровать после выхода новости, мин
- [x] `NS_IMPT`: Начиная с какой важности фильтровать новости

#### 3.1. ФИЛЬТРЫ ВОСХ+ЛОНГ ↑+↑ (FIL)
- [x] `UL_ENBL`: ↑+↑: Тогровля включена
- [x] `UL_WICK`: ↑+↑: Min дистанция свипа, пункт
- [x] `UL_FRCN`: ↓+↑: Min дистанция от Фрактала до C или O, пункт
- [x] `UL_FRCL`: ↑+↑: Max дистанция от Фрактала до Закрытия, пункт
- [x] `UL_FRPF`: ↑+↑: Min дистанция от Фрактала до Прошлого, пункт

#### 3.2. ФИЛЬТРЫ ВОСХ+ШОРТ ↑+↓ (FIL)"
- [x] `US_ENBL`: ↑+↓: Тогровля включена
- [x] `US_WICK`: ↑+↓: Min дистанция свипа, пункт
- [x] `US_FRCN`: ↓+↑: Min дистанция от Фрактала до C или O, пункт
- [x] `US_FRCL`: ↑+↓: Max дистанция от Фрактала до Закрытия, пункт
- [x] `US_FRPF`: ↑+↓: Min дистанция от Фрактала до Прошлого, пункт

#### 3.3. ФИЛЬТРЫ НИЗХ+ЛОНГ ↓+↑ (FIL)
- [x] `DL_ENBL`: ↓+↑: Тогровля включена
- [x] `DL_WICK`: ↓+↑: Min дистанция свипа, пункт
- [x] `DL_FRCN`: ↓+↑: Min дистанция от Фрактала до C или O, пункт
- [x] `DL_FRCL`: ↓+↑: Max дистанция от Фрактала до Закрытия, пункт
- [x] `DL_FRPF`: ↓+↑: Min дистанция от Фрактала до Прошлого, пункт

#### 3.4. ФИЛЬТРЫ НИЗХ+ШОРТ ↓+↓ (FIL)
- [x] `DS_ENBL`: ↓+↓: Тогровля включена
- [x] `DS_WICK`: ↓+↓: Min дистанция свипа, пункт
- [x] `DS_FRCN`: ↓+↑: Min дистанция от Фрактала до C или O, пункт
- [x] `DS_FRCL`: ↓+↓: Max дистанция от Фрактала до Закрытия, пункт
- [x] `DS_FRPF`: ↓+↓: Min дистанция от Фрактала до Прошлого, пункт

#### 3.5. ФИЛЬТРЫ ФЛЭТ+ЛОНГ →+↑ (FIL)"
- [x] `FL_ENBL`: →+↑: Тогровля включена
- [x] `FL_WICK`: →+↑: Min дистанция свипа, пункт
- [x] `FL_FRCN`: ↓+↑: Min дистанция от Фрактала до C или O, пункт
- [x] `FL_FRCL`: →+↑: Max дистанция от Фрактала до Закрытия, пункт
- [x] `FL_FRPF`: →+↑: Min дистанция от Фрактала до Прошлого, пункт

#### 3.6. ФИЛЬТРЫ ФЛЭТ+ШОРТ →+↓ (FIL)"
- [x] `FS_ENBL`: →+↓: Тогровля включена
- [x] `FS_WICK`: →+↓: Min дистанция свипа, пункт
- [x] `FS_FRCN`: ↓+↑: Min дистанция от Фрактала до C или O, пункт
- [x] `FS_FRCL`: →+↓: Max дистанция от Фрактала до Закрытия, пункт
- [x] `FS_FRPF`: →+↓: Min дистанция от Фрактала до Прошлого, пункт

#### 4. ГРАФИКА (UI)
- [x] `UI_COL_FL`: Цвет флэта
- [x] `UI_COL_UP`: Цвет бычьего тренда
- [x] `UI_COL_DN`: Цвет медвежьего тренда
- [x] `UI_IFR_EN`: Добавить индикаторы 'PADD-Fractal' при запуске
- [x] `UI_ISB_EN`: Добавить индикаторы 'Struture Blocks' при запуске

#### 5. MISCELLANEOUS (MSC)
- [x] `MSC_MGC`: Expert Adviser ID - Magic
- [x] `MSC_EGP`: Expert Adviser Global Prefix
- [x] `MSC_LOG_LL`: Log Level
- [x] `MSC_LOG_FI`: Log Filter IN String (use ';' as sep)
- [x] `MSC_LOG_FO`: Log Filter OUT String (use ';' as sep) 