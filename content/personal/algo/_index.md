---
title: Algorithmic Trading
prev: personal
next: erp_dev
sidebar:
    open: true
publishDate: 2023-08-21
weight: 1
---

This page contains trading strategies I’ve worked on and my articles about algorithmic trading. Also there're my open-source development tools here. A lot of materials are published on thematic websites, and all current ones are shared on the Telegram channel.

{{< cards cols="2">}}
  {{< card link="https://t.me/TrueAlgoTrading" title="Telegram" subtitle="Subscribe to True AlgoTrading Channel to keep updated" icon="telegram-bw">}}
  {{< card link="https://www.mql5.com/en/search#!author=deniskislitsyn&module=mql5_module_codebase" title="MQL5" subtitle="My MQL5 publications" icon="globe-alt">}}
{{< /cards >}}

## Strategies Portfolio

Here is a list of the projects I have worked on. I have put each project into different categories based on the types of trading it uses. There is a description available for some `Public` projects, which may be of interest.

| # | Name | Type | Tags |
|---|------|------|------|
| 67 | **DWIB-MT5-Bot2** <br> The "Don't Worry" trading strategy uses a consolidation beyond the Initial Balance session and structure breakdown to enter positions | `Private` | [`Trend`](/personal/algo/trend) [`PA/SMC`](/personal/algo/pasmc) |
| 66 | **[PADD-Fractal-MT5-Ind](/personal/algo/indicators/066-padd-fractal-mt5-ind/)** <br> Indicator offers flexible fractal configuration, including the number of candles to the left and right, and the ability to filter based on sorted high/low values. <br> Free download [MQL5 Market](https://www.mql5.com/en/market/product/139095) | `Public` | [`Trend`](/personal/algo/trend) |
| 65 | **DS-Empirix-PA_Stoch** <br> The *PA Stoch* trading strategy by *[Empirix](https://empirix.ru)* is based on using the Stochastic oscillator as a trend indicator, along with confirming factors from Price Action | `Private` | [`Trend`](/personal/algo/trend) [`Indicator`](/personal/algo/indicator) [`Pattern`](/personal/algo/pattern) |
| 64 | **DS-Empirix-Squeeze** <br> The *Squeeze* trading strategy by *[Empirix](https://empirix.ru)* analyzes the MA channel ti identify unusual compressions and expansions for trade opportunities | `Private` | [`Trend`](/personal/algo/trend) [`Indicator`](/personal/algo/indicator) |
| 63 | **DS-Empirix-Relativity** <br> The *Relativity* trading strategy by *[Empirix](https://empirix.ru)* identifies the emergence of a trend without taking time or timeframes into account, relying solely on Renko candles | `Private` | [`Trend`](/personal/algo/trend) [`Renko`](/personal/algo/renko) [`Pattern`](/personal/algo/pattern) |
| 62 | **[SessionMA-MT5-Ind](/personal/algo/indicators/062-sessionma-mt5-ind/)** <br> SessionMA calculates the MA only on bars that fall within a specified session time window <br> Free download [MQL5 Market](https://www.mql5.com/ru/market/product/138136) | `Public` | [`Trend`](/personal/algo/trend) |
| 61 | **[ClassicRenkoOnTick-MT5-Ind](/personal/algo/indicators/061-classicrenkoontick-mt5-ind/)** <br> This MT5 indicator provides real-time updates of classic Renko charts focused on price movement, filtering out noise and highlighting trends <br> Free download [MQL5 Market](https://www.mql5.com/ru/market/product/137132) | `Public` | [`Trend`](/personal/algo/trend) |
| 60 | **[MAChannel-MT5-Ind](/personal/algo/indicators/060-machannel-mt5-ind/)** <br> Expert Advisors often use a channel around standard MAs. The indicator builds such a channel and has three buffers: MA, MA Channel Top and MA Channel Bottom <br> Free download [MQL5 Market](https://www.mql5.com/en/market/product/135784) | `Public` | [`Trend`](/personal/algo/trend) |
| 59 | **[ChaikinMoneyFlow-MT5-Ind](/personal/algo/indicators/059-chaikinmoneyflow-mt5-ind/)** <br> The Chaikin Money Flow (CMF) is an indicator created by Marc Chaikin in the 1980s to monitor the accumulation and distribution of a stock over a specified period <br> Free download [MQL5 Market](https://www.mql5.com/ru/market/product/135679) | `Public` | [`Volume`](/personal/algo/volume) |
| 58 | **DS-SPTR** <br> The bot trades according to a private trend detection strategy | `Private` | [`Trend`](/personal/algo/trend) |
| 57 | **DS-SPCTR** <br> The bot trades according to a private countertrend detection strategy | `Private` | [`Trend`](/personal/algo/trend) |
| 56 | **DS-LunaticDay** <br> The bot trades according to a private strategy based on the identification of trend days | `Private` | [`Trend`](/personal/algo/trend) |
| 55 | **DS-SP1IO** <br> The bot trades on a private strategy of bounces from envelope boundaries   | `Private` | [`Trend`](/personal/algo/trend) [`Indicator`](/personal/algo/indicator) [`Range`](/personal/algo/range) |
| 54 | **DS-SPNIB-MT5-Bot** <br> The bot trades according to a private strategy of searching and breaking through trading channels   | `Private` | [`Trend`](/personal/algo/trend) [`Indicator`](/personal/algo/indicator) [`Range`](/personal/algo/range) |
| 53 | **SBSystem** <br> The bot trades using a private strategy based on a combination of indicators | `Private` | [`Trend`](/personal/algo/trend) [`Indicator`](/personal/algo/indicator) |
| 52 | **[AT-ZigZagADX](/personal/algo/rating/052-at-zigzagadx/)** <br> The bot trades in the direction of the last ZigZag edge as long as ADX, WPR, and TEMA are confirmed | `Public` | [`Trend`](/personal/algo/trend) [`Indicator`](/personal/algo/indicator) |
| 51 | **[FridayGoldRush-MT5-Bot](/personal/algo/rating/051-fridaygoldrush-mt5-bot/)** <br> Bot for MetaTrader 5 trades on a combination of ZigZig and WPR indicators and candlestick patterns <br> Free download [MQL5 Market](https://www.mql5.com/en/market/product/131729) | `Public` | [`Trend`](/personal/algo/trend) |
| 50 | **[AT-ZigZagColorBars](/personal/algo/rating/050-at-zigzagcolorbars/)** <br> Bot for MetaTrader 5 trades on a combination of ZigZig and WPR indicators and candlestick patterns | `Public` | [`Trend`](/personal/algo/trend) [`Indicator`](/personal/algo/indicator) |
| 49 | **[NYMB-MGridAssistant-MT5-Bot](/personal/algo/rating/049-nymb-mgridassistant-mt5-bot/)** <br> A bot assistant works with a manual trade, automatically averaging it with two Martingale grids | `Private` | [`Tool`](/personal/algo/tool) [`Grid`](/personal/algo/grid) [`GUI`](/personal/algo/gui) |
| 48 | **Order Book Scanner** <br> This tool lets you keep a order book history in SQLite and then look at it later | `Private` | [`Tool`](/personal/algo/tool) |
| 47 | **Three Black Crows & Three White Soldiers** <br> Classic pattern strategy  | `Private` | [`Pattern`](/personal/algo/pattern) |
| 46 | **[DV-FSSI](/personal/algo/rating/047-dv-fssi/)** <br> The multicurrency EA uses [fxssi.com](https://fxssi.com) indicators to trade breakouts of correlated crowd's SL clusters  | `Public` | [`Zone`](/personal/algo/zone) [`Indicator`](/personal/algo/indicator) |
| 45 | **DC1440min** <br> Trend trading strategy for futures market based on levels detection | `Private` | [`Trend`](/personal/algo/trend) [`Zone`](/personal/algo/zone) |
| 44 | **CL60min** <br> Trend trading strategy for futures market based on ADX, MACD, MA indicators and range breakout | `Private` | [`Indicator`](/personal/algo/indicator) [`Trend`](/personal/algo/trend) [`Range`](/personal/algo/range) |
| 43 | **GS480min** <br> Trend trading strategy for futures market based on ADX indicator | `Private` | [`Indicator`](/personal/algo/indicator) [`Trend`](/personal/algo/trend) |
| 42 | **Silaev - HI** <br> by Alexander Silaev the author of "Money without fools" book | `Private` | [`Pattern`](/personal/algo/pattern) [`Trend`](/personal/algo/trend) |
| 41 | **Silaev - BR** <br> by Alexander Silaev the author of "Money without fools" book | `Private` | [`Pattern`](/personal/algo/pattern) [`Trend`](/personal/algo/trend) |
| 40 | **Silaev - UN** <br> by Alexander Silaev the author of "Money without fools" book | `Private` | [`Pattern`](/personal/algo/pattern) [`Trend`](/personal/algo/trend) |
| 39 | **Silaev - PR** <br> by Alexander Silaev the author of "Money without fools" book | `Private` | [`Pattern`](/personal/algo/pattern) [`Trend`](/personal/algo/trend) |
| 38 | **[Fractal Fibo FVG](/personal/algo/rating/038-fff/)** <br> The trading indicator for MetaTrader 5 builds FVG inside Fibo by Fractals | `Public` | [`Pattern`](/personal/algo/pattern) [`Fibo`](/personal/algo/fibo) [`Zone`](/personal/algo/zone) |
| 37 | **Anchor Zone Setup** <br> The strategy based on "Anchor Zone Setup" of L.A. Little book "Trend Qualification and Trading" | `Private` | [`Pattern`](/personal/algo/pattern) [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range) |
| 36 | **Pattern And Divergence Detector** <br> The bot trades a custom pattern and divergence or convergence of price and indicator | `Private` | [`Divergence`](/personal/algo/divergence) [`Pattern`](/personal/algo/pattern) [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range)  [`Indicator`](/personal/algo/indicator) |
| 35 | **Three Orders Zone from Fibo** <br> The bot trades rebounds from Fibo levels of support and resistance zones | `Private` | [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range) [`Indicator`](/personal/algo/indicator)  [`Fibo`](/personal/algo/fibo)  |
| 34 | **[VWAP Crossing](/personal/algo/rating/034-vwap/)** <br>The bot trades from VWAP crossing | `Public` | [`Indicator`](/personal/algo/indicator) |
| 33 | **[SMC Structure Trade](/personal/algo/rating/033-smc-structure/)** <br>The bot trades retracement after BOS or CHoCH | `Public` | [`PA/SMC`](/personal/algo/pasmc)  [`Fibo`](/personal/algo/fibo) [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range)  |
| 32 | **[Advanced Fractal Sweep](/personal/algo/rating/032-afs/)** <br>The bot trades by sweeping levels off fractals filtering by trends | `Public` | [`Fractral`](/personal/algo/fractal)  [`Trend`](/personal/algo/trend) [`PA/SMC`](/personal/algo/pasmc)  |
| 31 | **[Multi TF Trend Tool](/personal/algo/rating/031-mtf-trend-tool/)** <br>The tool to check multi TF trend using SMC structure | `Public` | [`Tool`](/personal/algo/tool)  [`GUI`](/personal/algo/gui) <br> [`Trend`](/personal/algo/trend)  [`PA/SMC`](/personal/algo/pasmc) |
| 30 | **[Fibo Two Orders](/personal/algo/rating/030-fibo2o/)** <br>The trading strategy of the bot is Fibo retracement after BOS | `Public` | [`PA/SMC`](/personal/algo/pasmc)  [`Fibo`](/personal/algo/fibo)  [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range) [`GUI`](/personal/algo/gui) |
| 29 | **News Breakout** <br>The trading strategy of the bot is a catching breakout at the moment of a significant news release | `Private` | [`News`](/personal/algo/news)  [`HTF`](/personal/algo/htf)  |
| 28 | **News Flow** <br>The trading strategy of the bot is a breakout at the moment of a significant news release in the direction of overall economic expectations, whether growth or decline | `Private` | [`News`](/personal/algo/news) |
| 27 | **[PALL-E](/personal/algo/rating/grids/006_meet_palle/)** <br>The bot is the result of the evolution of the grid trading system, which was specially created in 2019 for XAUUSD | `Public` | [`Grid`](/personal/algo/grid) [`Indicator`](/personal/algo/indicator)  |
| 26 | **Daily Inside Bar Setup** <br>The bot for DIBS strategy | `Private` | [`Pattern`](/personal/algo/pattern) |
| 25 | **Time Price Opportunity** <br>The bot for DIBS strategy | `Private` | [`Indicator`](/personal/algo/indicator) [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range) |
| 24 | **Zigzager** <br>The bot trades from the levels of the standard ZigZag indicator | `Private` | [`Indicator`](/personal/algo/indicator)  [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range) |
| 23 | **Crypto Tele Broker** <br>The Telegram bot executes transactions on cryptocurrency exchanges based on users' messages | `Private` | [`Tool`](/personal/algo/tool)  [`Crypto`](/personal/algo/crypto) |
| 22 | **Trading Time Indicator** <br>The indicator draws the periods available for trading on the chart | `Private` | [`Tool`](/personal/algo/tool)  [`Indicator`](/personal/algo/indicator) [`GUI`](/personal/algo/gui) |
| 21 | **Stat Script** <br>The script generates a report on the history of EA trades, filtering them by comment part or magic number | `Private` | [`Tool`](/personal/algo/tool) |
| 20 | **Breakout Profit** <br>The bot trades breakouts or bounces from daily lows/highs | `Private` | [`Indicator`](/personal/algo/indicator) [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range) |
| 19 | **ATR Rages Grid** <br>The bot trades narrowing ATR ranges | `Private` | [`Indicator`](/personal/algo/indicator) [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range) [`Grid`](/personal/algo/grid) |
| 18 | **[Pattern 34 Detector](/personal/algo/indicators/018-pattern34/)** <br>The bot detects custom "Pattern 34" and trades from it on FX or BO | `Public` | [`Pattern`](/personal/algo/pattern) |
| 17 | **Volume Candle** <br>The bot detects and trades custom "Volume Candlestick" pattern | `Private` | [`Pattern`](/personal/algo/pattern) |
| 16 | **AutoLocker** <br>The bot locks positions when drawdown is reached | `Public` | [`MoneyMan`](/personal/algo/moneyman) |
| 15 | **Ethereum ADX trading** <br>The strategy for ETHUSDT with entering and exiting the position according to ADX | `Private` | [`Indicator`](/personal/algo/indicator)  [`Crypto`](/personal/algo/crypto)  |
| 14 | **Sport Bet Arbitrage** <br>The strategy for ETHUSDT with entering and exiting the position according to ADX | `Private` | [`Arbitrage`](/personal/algo/arbitrage) |
| 13 | **Elder Divergence** <br>The Elder MACD/RSI Divergence Strategy | `Private` | [`Indicator`](/personal/algo/indicator) [`Divergence`](/personal/algo/divergence) |
| 12 | **Virtual Order News Trading Bot** <br>Trade on outstanding news and try to catch strong price moving. There are so lots of traps when milliseconds and spread matter. | `Private` | [`News`](/personal/algo/news)  [`HTF`](/personal/algo/htf) |
| 11 | **Crypto Advanced Arbitrage Bot** <br>Advanced crypto arbitrage Telegram bot for Binance, Bybit, KuCoin, OKX | `Private` | [`HTF`](/personal/algo/htf)  [`Arbitrage`](/personal/algo/arbitrage)  [`Crypto`](/personal/algo/crypto) |
| 10 | **HTF Arbitrage** <br>The MetaTrader 4&5 HTF Bots with third party highspeed updating rates API | `Private` | [`HTF`](/personal/algo/htf)  [`Arbitrage`](/personal/algo/arbitrage) |
| 9 | **SMT Three Symbol Divergence** <br>The bot looks for divergence between three assets EURUSD, GBPUSD and DXY on HTF. When it finds one, it enters the trade after BOS on LTF. | `Private` | [`Divergence`](/personal/algo/divergence) [`PA/SMC`](/personal/algo/pasmc) |
| 8 | **STP Tool** <br>The bot places different order based on manually drawn Fibonacci-Object | `Private` | [`Tool`](/personal/algo/tool) [`GUI`](/personal/algo/gui) |
| 7 | **Multi Indicator crypto trading bot** <br>The bot uses multi timeframe EMA, MACD and RSI setup for crypto trading on Binance | `Private` | [`Indicator`](/personal/algo/indicator)  [`Crypto`](/personal/algo/crypto) |
| 6 | **Fair Value Gap Zone** <br>The bot detects FVG and trades zone retracement | `Private` | [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range) [`PA/SMC`](/personal/algo/pasmc) |
| 5 | **Four Advanced Grids** <br>The bot handles two multidirectional grids at once, and it opens orders based on the Indicator. Each grid can be blocked by a reverse grid, so the bot can control up to four grids at the same time | `Private` | [`Grid`](/personal/algo/grid)  [`Indicator`](/personal/algo/indicator) |
| 4 | **Springfield Three Grids** <br>The bot simultaneously manages 3 grids on a single instrument with different parameters | `Private` | [`Grid`](/personal/algo/grid) |
| 3 | **Three Orders Zone** <br>The bot trades rebounds from support and resistance zones | `Private` | [`Zone`](/personal/algo/zone) [`Range`](/personal/algo/range) [`Indicator`](/personal/algo/indicator) |
| 2 | **Tip Top AI** <br>The bot uses AI generated strategy to detect entry point by Tail length algorithm | `Public` | [`Pattern`](/personal/algo/pattern) [`ML&AI`](/personal/algo/mlai) |
| 1 | [**Eve On Haloperidol**](/personal/algo/research/baza/005_params_for_eve_on_haloperidol) <br>The trading strategy of Baza's Eve grid bot has been improved with protection against unidirectional price movement that won't budge | `Public` | [`Grid`](/personal/algo/grid)  [`Indicator`](/personal/algo/indicator) |

