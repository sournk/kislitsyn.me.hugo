---
title: Algorithmic Trading
aliases:
  - /personal/algo/
  - /personal/
sidebar:
    open: true
cascade:
  type: docs
publishDate: 2023-08-21
weight: 1
---

A portfolio of algo-trading projects: automated strategies, MT5 indicators, development libraries, and research. Public projects have detailed write-ups and free downloads.

{{< cards cols="2">}}
  {{< card link="https://t.me/TrueAlgoTrading" title="Telegram" subtitle="Subscribe to True AlgoTrading Channel to keep updated" icon="telegram-bw">}}
  {{< card link="https://www.mql5.com/en/search#!author=deniskislitsyn&module=mql5_module_codebase" title="MQL5" subtitle="My MQL5 publications" icon="globe-alt">}}
{{< /cards >}}

## Explore by Category

{{< cards cols="3">}}
  {{< card link="#trend--breakout" title="Trend & Breakout (18)" subtitle="Following momentum and directional moves using indicators and price structure" icon="trending-up">}}
  {{< card link="#mean-reversion" title="Mean Reversion (9)" subtitle="Trading pullbacks to equilibrium from overbought/oversold zones and key levels" icon="switch-horizontal">}}
  {{< card link="#price-action--smart-money" title="Price Action & Smart Money (8)" subtitle="Institutional order flow, market structure shifts, and liquidity-driven entries" icon="eye">}}
  {{< card link="#pattern--candlestick" title="Pattern & Candlestick (12)" subtitle="Recognizing repeatable chart formations, divergences, and anomalies" icon="template">}}
  {{< card link="#grid--averaging" title="Grid & Averaging (5)" subtitle="Position averaging with risk controls, adaptive spacing, and drawdown protection" icon="view-grid">}}
  {{< card link="#news--event-driven" title="News & Event-Driven (4)" subtitle="Reacting to macro releases, economic calendar, and seasonal effects" icon="newspaper">}}
  {{< card link="#arbitrage" title="Arbitrage (3)" subtitle="Exploiting price discrepancies across venues, brokers, and asset classes" icon="lightning-bolt">}}
  {{< card link="#tools--assistants" title="Tools & Assistants (8)" subtitle="Trade management, analytics, and workflow automation for manual and algo traders" icon="adjustments">}}
  {{< card link="indicators/" title="Indicators" subtitle="6 public MT5 indicators for technical analysis" icon="chart-bar">}}
  {{< card link="dev/" title="Dev Libraries" subtitle="Open-source MQL5 development tools" icon="code">}}
  {{< card link="research/" title="Research & Blog" subtitle="Grid bot reliability, platform comparisons" icon="book-open">}}
{{< /cards >}}

## Strategies Portfolio

There is a description available for some `Public` projects, which may be of interest.

### Trend & Breakout

Trend-following and breakout strategies based on technical indicators: MA, ADX, ZigZag, Renko, Keltner channels, and more.

| # | Name | Type |
|---|------|------|
| 1 | **[NovuPark-MT5-Bot](/algo/rating/073-novupark)** <br> The bot trades on the original closed strategy based on a combination of technical indicators based on Schaff Trend Cycle | `Public` |
| 2 | **DS-LW-2MA-MT5-Bot** <br> Larry Williams' trading strategy based on two MAs and designed for SP500 futures | `Private` |
| 3 | **DS-KJ-MomentumKeltnerCombo-MT5-Bot** <br> Momentum & Keltner Stochastic Combo | `Private` |
| 4 | **DS-Empirix-Squeeze** <br> The *Squeeze* strategy by *[Empirix](https://empirix.ru)* analyzes MA channel compressions and expansions | `Private` |
| 5 | **DS-Empirix-Relativity** <br> The *Relativity* strategy by *[Empirix](https://empirix.ru)* identifies trends relying solely on Renko candles | `Private` |
| 6 | **DS-SPTR** <br> The bot trades according to a private trend detection strategy | `Private` |
| 7 | **DS-LunaticDay** <br> The bot trades based on the identification of trend days | `Private` |
| 8 | **DS-SPNIB-MT5-Bot** <br> The bot trades by searching and breaking through trading channels | `Private` |
| 9 | **SBSystem** <br> The bot trades using a private strategy based on a combination of indicators | `Private` |
| 10 | **[AT-ZigZagADX](/algo/rating/052-at-zigzagadx/)** <br> The bot trades in the direction of the last ZigZag edge as long as ADX, WPR, and TEMA are confirmed | `Public` |
| 11 | **[AT-ZigZagColorBars](/algo/rating/050-at-zigzagcolorbars/)** <br> Bot for MetaTrader 5 trades on a combination of ZigZag and WPR indicators and candlestick patterns | `Public` |
| 12 | **[DV-FSSI](/algo/rating/047-dv-fssi/)** <br> The multicurrency EA uses [fxssi.com](https://fxssi.com) indicators to trade breakouts of correlated crowd's SL clusters | `Public` |
| 13 | **DC1440min** <br> Trend trading strategy for futures market based on levels detection | `Private` |
| 14 | **CL60min** <br> Trend trading strategy for futures based on ADX, MACD, MA indicators and range breakout | `Private` |
| 15 | **GS480min** <br> Trend trading strategy for futures market based on ADX indicator | `Private` |
| 16 | **Breakout Profit** <br> The bot trades breakouts or bounces from daily lows/highs | `Private` |
| 17 | **Ethereum ADX trading** <br> The strategy for ETHUSDT with entering and exiting the position according to ADX | `Private` |
| 18 | **Multi Indicator crypto trading bot** <br> The bot uses multi timeframe EMA, MACD and RSI setup for crypto trading on Binance | `Private` |

### Mean Reversion

Strategies that trade reversals to the mean: zone bounces, VWAP, envelope boundaries, and support/resistance levels.

| # | Name | Type |
|---|------|------|
| 1 | **DS-Empirix-DennisRichards-MT5-Bot** <br> Trading strategy 'Dennis Richards' developed by *[Empirix](https://empirix.ru)* team | `Private` |
| 2 | **DS-SPCTR** <br> The bot trades according to a private countertrend detection strategy | `Private` |
| 3 | **DS-SP1IO** <br> The bot trades on a private strategy of bounces from envelope boundaries | `Private` |
| 4 | **Anchor Zone Setup** <br> The strategy based on "Anchor Zone Setup" of L.A. Little book "Trend Qualification and Trading" | `Private` |
| 5 | **Three Orders Zone from Fibo** <br> The bot trades rebounds from Fibo levels of support and resistance zones | `Private` |
| 6 | **[VWAP Crossing](/algo/rating/034-vwap/)** <br> The bot trades from VWAP crossing | `Public` |
| 7 | **Time Price Opportunity** <br> The bot trades based on TPO / Market Profile zones | `Private` |
| 8 | **Zigzager** <br> The bot trades from the levels of the standard ZigZag indicator | `Private` |
| 9 | **Three Orders Zone** <br> The bot trades rebounds from support and resistance zones | `Private` |

### Price Action & Smart Money

Smart Money Concept (SMC/ICT): BOS/CHoCH detection, Fibonacci POI, Fair Value Gaps, SMT divergence.

| # | Name | Type |
|---|------|------|
| 1 | **DW-DontWorry-PIVOT-MT5-Bot** <br> "Don't Worry" trading strategy uses Pivot Point and Price Action indicator | `Private` |
| 2 | **DW-IB-MT5-Bot** <br> The "Don't Worry" strategy uses consolidation beyond the Initial Balance session and structure breakdown | `Private` |
| 3 | **[Fractal Fibo FVG](/algo/rating/038-fff/)** <br> The trading indicator for MetaTrader 5 builds FVG inside Fibo by Fractals | `Public` |
| 4 | **[SMC Structure Trade](/algo/rating/033-smc-structure/)** <br> The bot trades retracement after BOS or CHoCH | `Public` |
| 5 | **[Advanced Fractal Sweep](/algo/rating/032-afs/)** <br> The bot trades by sweeping levels off fractals filtering by trends | `Public` |
| 6 | **[Fibo Two Orders](/algo/rating/030-fibo2o/)** <br> The trading strategy of the bot is Fibo retracement after BOS | `Public` |
| 7 | **SMT Three Symbol Divergence** <br> The bot looks for divergence between EURUSD, GBPUSD and DXY on HTF, enters after BOS on LTF | `Private` |
| 8 | **Fair Value Gap Zone** <br> The bot detects FVG and trades zone retracement | `Private` |

### Pattern & Candlestick

Candlestick pattern detection, divergence strategies, and ML/AI-based pattern recognition.

| # | Name | Type |
|---|------|------|
| 1 | **DS-Empirix-PA_Stoch** <br> The *PA Stoch* strategy by *[Empirix](https://empirix.ru)* uses Stochastic as a trend indicator with Price Action confirmation | `Private` |
| 2 | **Three Black Crows & Three White Soldiers** <br> Classic candlestick pattern strategy | `Private` |
| 3 | **Silaev - HI** <br> by Alexander Silaev the author of "Money without fools" book | `Private` |
| 4 | **Silaev - BR** <br> by Alexander Silaev the author of "Money without fools" book | `Private` |
| 5 | **Silaev - UN** <br> by Alexander Silaev the author of "Money without fools" book | `Private` |
| 6 | **Silaev - PR** <br> by Alexander Silaev the author of "Money without fools" book | `Private` |
| 7 | **Pattern And Divergence Detector** <br> The bot trades a custom pattern and divergence or convergence of price and indicator | `Private` |
| 8 | **Daily Inside Bar Setup** <br> The bot for DIBS strategy | `Private` |
| 9 | **[Pattern 34 Detector](/algo/indicators/018-pattern34/)** <br> The bot detects custom "Pattern 34" and trades from it on FX or BO | `Public` |
| 10 | **Volume Candle** <br> The bot detects and trades custom "Volume Candlestick" pattern | `Private` |
| 11 | **Elder Divergence** <br> The Elder MACD/RSI Divergence Strategy | `Private` |
| 12 | **Tip Top AI** <br> The bot uses AI generated strategy to detect entry point by Tail length algorithm | `Public` |

### Grid & Averaging

Grid averaging systems with adaptive take-profit, drawdown protection, and multi-grid management.

| # | Name | Type |
|---|------|------|
| 1 | **[PALL-E](/algo/rating/grids/006_meet_palle/)** <br> The bot is the result of the evolution of the grid trading system, specially created in 2019 for XAUUSD | `Public` |
| 2 | **ATR Ranges Grid** <br> The bot trades narrowing ATR ranges | `Private` |
| 3 | **Four Advanced Grids** <br> The bot handles two multidirectional grids at once, each grid can be blocked by a reverse grid | `Private` |
| 4 | **Springfield Three Grids** <br> The bot simultaneously manages 3 grids on a single instrument with different parameters | `Private` |
| 5 | [**Eve On Haloperidol**](/algo/research/baza/005_params_for_eve_on_haloperidol) <br> Baza's Eve grid bot improved with protection against unidirectional price movement | `Public` |

### News & Event-Driven

Strategies based on news releases, economic calendar, and day-of-week anomalies.

| # | Name | Type |
|---|------|------|
| 1 | **[FridayGoldRush-MT5-Bot](/algo/rating/051-fridaygoldrush-mt5-bot/)** <br> The bot exploits a day-of-week pattern on XAUUSD: buy Thursday, sell Friday <br> Free download [MQL5 Market](https://www.mql5.com/en/market/product/131729) | `Public` |
| 2 | **News Breakout** <br> The bot catches breakout at the moment of a significant news release | `Private` |
| 3 | **News Flow** <br> The bot trades breakout at news release in the direction of overall economic expectations | `Private` |
| 4 | **Virtual Order News Trading Bot** <br> Trade on outstanding news and try to catch strong price moving | `Private` |

### Arbitrage

High-frequency and statistical arbitrage across brokers and exchanges.

| # | Name | Type |
|---|------|------|
| 1 | **Sport Bet Arbitrage** <br> Cross-market arbitrage strategy | `Private` |
| 2 | **Crypto Advanced Arbitrage Bot** <br> Advanced crypto arbitrage Telegram bot for Binance, Bybit, KuCoin, OKX | `Private` |
| 3 | **HTF Arbitrage** <br> The MetaTrader 4&5 HFT Bots with third party highspeed updating rates API | `Private` |

### Tools & Assistants

Utilities, GUI assistants, and risk management tools for traders.

| # | Name | Type |
|---|------|------|
| 1 | **[NYMB-MGridAssistant-MT5-Bot](/algo/rating/049-nymb-mgridassistant-mt5-bot/)** <br> A bot assistant works with a manual trade, automatically averaging it with two Martingale grids | `Private` |
| 2 | **Order Book Scanner** <br> This tool lets you keep an order book history in SQLite and then look at it later | `Private` |
| 3 | **[Multi TF Trend Tool](/algo/rating/031-mtf-trend-tool/)** <br> The tool to check multi TF trend using SMC structure | `Public` |
| 4 | **Crypto Tele Broker** <br> The Telegram bot executes transactions on cryptocurrency exchanges based on users' messages | `Private` |
| 5 | **Trading Time Indicator** <br> The indicator draws the periods available for trading on the chart | `Private` |
| 6 | **Stat Script** <br> The script generates a report on the history of EA trades, filtering them by comment part or magic number | `Private` |
| 7 | **AutoLocker** <br> The bot locks positions when drawdown is reached | `Public` |
| 8 | **STP Tool** <br> The bot places different orders based on manually drawn Fibonacci-Object | `Private` |

### Indicators

Public open-source indicators for MetaTrader 5 — see the full [Indicators](/algo/indicators/) section.

| # | Name |
|---|------|
| 1 | **[PADD-Fractal-MT5-Ind](/algo/indicators/066-padd-fractal-mt5-ind/)** <br> Flexible fractal configuration with sorted high/low filtering — [MQL5 Market](https://www.mql5.com/en/market/product/139095) |
| 2 | **[SessionMA-MT5-Ind](/algo/indicators/062-sessionma-mt5-ind/)** <br> MA calculated only within a specified session time window — [MQL5 Market](https://www.mql5.com/ru/market/product/138136) |
| 3 | **[ClassicRenkoOnTick-MT5-Ind](/algo/indicators/061-classicrenkoontick-mt5-ind/)** <br> Real-time classic Renko charts focused on price movement — [MQL5 Market](https://www.mql5.com/ru/market/product/137132) |
| 4 | **[MAChannel-MT5-Ind](/algo/indicators/060-machannel-mt5-ind/)** <br> A channel around MA with three buffers: MA, Top, Bottom — [MQL5 Market](https://www.mql5.com/en/market/product/135784) |
| 5 | **[ChaikinMoneyFlow-MT5-Ind](/algo/indicators/059-chaikinmoneyflow-mt5-ind/)** <br> CMF indicator to monitor accumulation and distribution — [MQL5 Market](https://www.mql5.com/ru/market/product/135679) |
