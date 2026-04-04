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
  {{< card link="#trend--breakout" title="Trend & Breakout (35)" subtitle="Following momentum and directional moves using indicators and price structure" icon="trending-up">}}
  {{< card link="#mean-reversion" title="Mean Reversion (16)" subtitle="Trading pullbacks to equilibrium from overbought/oversold zones and key levels" icon="switch-horizontal">}}
  {{< card link="#price-action--smart-money" title="Price Action & Smart Money (11)" subtitle="Institutional order flow, market structure shifts, and liquidity-driven entries" icon="eye">}}
  {{< card link="#pattern--candlestick" title="Pattern & Candlestick (14)" subtitle="Recognizing repeatable chart formations, divergences, and anomalies" icon="template">}}
  {{< card link="#grid--averaging" title="Grid & Averaging (5)" subtitle="Position averaging with risk controls, adaptive spacing, and drawdown protection" icon="view-grid">}}
  {{< card link="#news--event-driven" title="News & Event-Driven (5)" subtitle="Reacting to macro releases, economic calendar, and seasonal effects" icon="newspaper">}}
  {{< card link="#arbitrage" title="Arbitrage (5)" subtitle="Exploiting price discrepancies across venues, brokers, and asset classes" icon="lightning-bolt">}}
  {{< card link="#tools--assistants" title="Tools & Assistants (9)" subtitle="Trade management, analytics, and workflow automation for manual and algo traders" icon="adjustments">}}
  {{< card link="indicators/" title="Indicators (8)" subtitle="8 public MT5 indicators for technical analysis" icon="chart-bar">}}
  {{< card link="dev/" title="Dev Libraries (3)" subtitle="Open-source MQL5 development tools" icon="code">}}
  {{< card link="research/" title="Research & Blog (7)" subtitle="Grid bot reliability, platform comparisons" icon="book-open">}}
{{< /cards >}}

## Strategies Portfolio

There is a description available for some `Public` projects, which may be of interest.

### Trend & Breakout

Trend-following and breakout strategies based on technical indicators: MA, ADX, ZigZag, Renko, Keltner channels, and more.

| # | Name | Type |
|---|------|------|
| 1 | **DS-FF-EMAScalping-MT5-Bot** <br> EMA Scalping: short-term EMA-based scalping strategy (details undisclosed) | `Private` |
| 2 | **DS-TLAP-PSAR-MT5-Bot** <br> TLAP PSAR: trend-following Parabolic SAR reversal strategy with optional EMA slope, ADX strength and HTF PSAR filters, PSAR-based trailing SL and R:R TP | `Private` |
| 3 | **DS-KS-Uptrend-MT5-Bot** <br> Uptrend M15: long-only multi-asset VWMA trend strategy that buys pullbacks to fast VWMA in uptrend, with ATR-based SL and slow-VWMA trailing stop across stocks, gold, gas and indices | `Private` |
| 4 | **DS-FSR-H4Daily-MT5-Bot** <br> H4 Daily: trend-following EMA crossover confirmed by ADX direction and MACD sign, with signal-bar SL, R:R TP, optional breakeven and trailing stop | `Private` |
| 5 | **DS-FSR-BetterVolume-MT5-Bot** <br> Better Volume zone breakout: detects Buy/Sell Climax zones via volume analysis, enters on zone boundary breakout with R:R TP and optional trailing stop | `Private` |
| 5 | **UniBreakout-MT5-Bot** <br> Universal Breakout: trades breakouts or rebounds from previous day / session range boundaries with ATR-based SL, R:R TP and trailing stop | `Private` |
| 7 | **DS-FSR-MACDMom-MT5-Bot** <br> MACD Momentum: enters on MACD/MA crossover confirmed by V-shaped Momentum pattern, with ATR-based SL and R:R breakeven exit | `Private` |
| 8 | **DS-FSR-Pit-MT5-Bot** <br> "Pit" strategy: trend-following entry on correction end using EMA trend filter and MACD/SMA crossover with ATR-based SL and R:R exit | `Private` |
| 9 | **DS-FQ-KC60-MT5-Bot** <br> Parabolic SAR crossover with dual MA filter (MA10/MA20), exits on profit drawdown from peak or reversal signal | `Private` |
| 10 | **DS-FX-Prosto-MT5-Bot** <br> FX Prosto: MA crossover strategy that enters at a fixed time based on price position relative to MA, with per-day session filters and optional timed exit | `Private` |
| 11 | **DS-FQ-NQ30m-MT5-Bot** <br> Donchian Channel breakout for NASDAQ futures with ADX filter, session time windows and ATR-based stop loss | `Private` |
| 12 | **DS-CH-Doncian5520-MT5-Bot** <br> Donchian Channel M15 intraday breakout for stocks with ATR filter, SMA trend confirmation and channel-based trailing SL | `Private` |
| 13 | **DS-DO-3MA-MT5-Bot** <br> Three MA trend strategy: enters on fast/middle/slow MA crossovers with ATR volatility and ADX trend filters | `Private` |
| 14 | **DS-FQ-Venom-MT5-Bot** <br> Pivot-based breakout with RSI filter, break-even and profit protection on 3H timeframe | `Private` |
| 15 | **DS-FQ-NR4-MT5-Bot** <br> NR4 Opening Range Breakout: enters on range expansion with stretch factor on daily timeframe | `Private` |
| 16 | **DS-FQ-Socrates-MT5-Bot** <br> Channel breakout strategy: Buy Stop on bars high / Sell Stop on bars low with bar pattern filter | `Private` |
| 17 | **DS-DErricoPortfolio-MT5-Bot** <br> Consolidation breakout strategy with volume confirmation by Domenico D'Errico (Stocks & Commodities) | `Private` |
| 18 | **[NovuPark-MT5-Bot](/algo/rating/073-novupark)** <br> The bot trades on the original closed strategy based on a combination of technical indicators based on Schaff Trend Cycle | `Public` |
| 19 | **DS-LW-2MA-MT5-Bot** <br> Larry Williams' trading strategy based on two MAs and designed for SP500 futures | `Private` |
| 20 | **DS-KJ-MomentumKeltnerCombo-MT5-Bot** <br> Momentum & Keltner Stochastic Combo | `Private` |
| 21 | **DS-Empirix-Squeeze** <br> The *Squeeze* strategy by *[Empirix](https://empirix.ru)* analyzes MA channel compressions and expansions | `Private` |
| 22 | **DS-Empirix-Relativity** <br> The *Relativity* strategy by *[Empirix](https://empirix.ru)* identifies trends relying solely on Renko candles | `Private` |
| 23 | **DS-SPTR** <br> The bot trades according to a private trend detection strategy | `Private` |
| 24 | **DS-LunaticDay** <br> The bot trades based on the identification of trend days | `Private` |
| 25 | **DS-SPNIB-MT5-Bot** <br> The bot trades by searching and breaking through trading channels | `Private` |
| 26 | **SBSystem** <br> The bot trades using a private strategy based on a combination of indicators | `Private` |
| 27 | **[AT-ZigZagADX](/algo/rating/052-at-zigzagadx/)** <br> The bot trades in the direction of the last ZigZag edge as long as ADX, WPR, and TEMA are confirmed | `Public` |
| 28 | **[AT-ZigZagColorBars](/algo/rating/050-at-zigzagcolorbars/)** <br> Bot for MetaTrader 5 trades on a combination of ZigZag and WPR indicators and candlestick patterns | `Public` |
| 29 | **[DV-FSSI](/algo/rating/047-dv-fssi/)** <br> The multicurrency EA uses [fxssi.com](https://fxssi.com) indicators to trade breakouts of correlated crowd's SL clusters | `Public` |
| 30 | **DC1440min** <br> Trend trading strategy for futures market based on levels detection | `Private` |
| 31 | **CL60min** <br> Trend trading strategy for futures based on ADX, MACD, MA indicators and range breakout | `Private` |
| 32 | **GS480min** <br> Trend trading strategy for futures market based on ADX indicator | `Private` |
| 33 | **Breakout Profit** <br> The bot trades breakouts or bounces from daily lows/highs | `Private` |
| 34 | **Ethereum ADX trading** <br> The strategy for ETHUSDT with entering and exiting the position according to ADX | `Private` |
| 35 | **Multi Indicator crypto trading bot** <br> The bot uses multi timeframe EMA, MACD and RSI setup for crypto trading on Binance | `Private` |

### Mean Reversion

Strategies that trade reversals to the mean: zone bounces, VWAP, envelope boundaries, and support/resistance levels.

| # | Name | Type |
|---|------|------|
| 1 | **RG-VWAPCross-MT5-Bot** <br> VWAP Cross: intraday mean reversion that places limit orders at VWAP level depending on price side, with session filter, partial fill logic and SL/TP cooldown pauses | `Private` |
| 2 | **DS-FQ-SQXETH-MT5-Bot** <br> StrategyQuant X adaptation of Donchian Channel mean reversion with MA filter for crypto trading | `Private` |
| 3 | **DS-FQ-POI-MA-MT5-Bot** <br> POI-MA Mean Reversion: Donchian Channel breakout contrarian strategy with long MA filter and short MA exit | `Private` |
| 4 | **DS-XCap-MT5-Bot** <br> Long-only statistical mean reversion for stocks: buys when price hits minimum filter boundary with negative spread, exits on spread recovery | `Private` |
| 5 | **DS-PDFade-MT5-Bot** <br> Previous Day Range Fakeout: fades false breakouts beyond PDH/PDL with ADX sideways filter, targeting mid-range | `Private` |
| 6 | **DS-BollingerSnapback-MT5-Bot** <br> Bollinger Bands snapback strategy: enters on bar return inside BB channel with ATR-based SL/TP | `Private` |
| 7 | **[WC-MeanReversion-BBDC-MT5-Bot](/algo/rating/074-WC_MeanReversion-BBDC/)** <br> Mean reversion strategy using Bollinger Bands and Donchian Channel with ATR-based risk management | `Public` |
| 8 | **DS-Empirix-DennisRichards-MT5-Bot** <br> Trading strategy 'Dennis Richards' developed by *[Empirix](https://empirix.ru)* team | `Private` |
| 9 | **DS-SPCTR** <br> The bot trades according to a private countertrend detection strategy | `Private` |
| 10 | **DS-SP1IO** <br> The bot trades on a private strategy of bounces from envelope boundaries | `Private` |
| 11 | **Anchor Zone Setup** <br> The strategy based on "Anchor Zone Setup" of L.A. Little book "Trend Qualification and Trading" | `Private` |
| 12 | **Three Orders Zone from Fibo** <br> The bot trades rebounds from Fibo levels of support and resistance zones | `Private` |
| 13 | **[VWAP Crossing](/algo/rating/034-vwap/)** <br> The bot trades from VWAP crossing | `Public` |
| 14 | **Time Price Opportunity** <br> The bot trades based on TPO / Market Profile zones | `Private` |
| 15 | **Zigzager** <br> The bot trades from the levels of the standard ZigZag indicator | `Private` |
| 16 | **Three Orders Zone** <br> The bot trades rebounds from support and resistance zones | `Private` |

### Price Action & Smart Money

Smart Money Concept (SMC/ICT): BOS/CHoCH detection, Fibonacci POI, Fair Value Gaps, SMT divergence.

| # | Name | Type |
|---|------|------|
| 1 | **DS-HTT-BreakAndRetest-MT5-Bot** <br> ICT Break & Retest: identifies support/resistance zones, waits for breakout and retest confirmation, enters in breakout direction with zone-based SL and R:R TP | `Private` |
| 2 | **DW-DontWorry-FVG-MT5-Bot** <br> FVG based strategy: trades sequential Fair Value Gaps and Balanced Price Ranges with session filter and trailing SL | `Private` |
| 3 | **DS-RallyBaseRally-MT5-Bot** <br> Rally-Base-Rally / Drop-Base-Drop pattern trading with multi-TF CHoCH confirmation | `Private` |
| 4 | **DW-DontWorry-PIVOT-MT5-Bot** <br> "Don't Worry" trading strategy uses Pivot Point and Price Action indicator | `Private` |
| 5 | **DW-IB-MT5-Bot** <br> The "Don't Worry" strategy uses consolidation beyond the Initial Balance session and structure breakdown | `Private` |
| 6 | **[Fractal Fibo FVG](/algo/rating/038-fff/)** <br> The trading indicator for MetaTrader 5 builds FVG inside Fibo by Fractals | `Public` |
| 7 | **[SMC Structure Trade](/algo/rating/033-smc-structure/)** <br> The bot trades retracement after BOS or CHoCH | `Public` |
| 8 | **[Advanced Fractal Sweep](/algo/rating/032-afs/)** <br> The bot trades by sweeping levels off fractals filtering by trends | `Public` |
| 9 | **[Fibo Two Orders](/algo/rating/030-fibo2o/)** <br> The trading strategy of the bot is Fibo retracement after BOS | `Public` |
| 10 | **SMT Three Symbol Divergence** <br> The bot looks for divergence between EURUSD, GBPUSD and DXY on HTF, enters after BOS on LTF | `Private` |
| 11 | **Fair Value Gap Zone** <br> The bot detects FVG and trades zone retracement | `Private` |

### Pattern & Candlestick

Candlestick pattern detection, divergence strategies, and ML/AI-based pattern recognition.

| # | Name | Type |
|---|------|------|
| 1 | **DS-FSR-Giraffe-MT5-Bot** <br> "Giraffe" Engulfing pattern strategy: enters on bullish/bearish engulfing candles with pin-bar filter and ATR-based take profit | `Private` |
| 2 | **DS-DO-FlagGann-MT5-Bot** <br> Flag pattern breakout with Gann angles: detects converging flag lines, validates trend on segment B, enters on flag boundary breakout | `Private` |
| 3 | **DS-Empirix-PA_Stoch** <br> The *PA Stoch* strategy by *[Empirix](https://empirix.ru)* uses Stochastic as a trend indicator with Price Action confirmation | `Private` |
| 4 | **Three Black Crows & Three White Soldiers** <br> Classic candlestick pattern strategy | `Private` |
| 5 | **Silaev - HI** <br> by Alexander Silaev the author of "Money without fools" book | `Private` |
| 6 | **Silaev - BR** <br> by Alexander Silaev the author of "Money without fools" book | `Private` |
| 7 | **Silaev - UN** <br> by Alexander Silaev the author of "Money without fools" book | `Private` |
| 8 | **Silaev - PR** <br> by Alexander Silaev the author of "Money without fools" book | `Private` |
| 9 | **Pattern And Divergence Detector** <br> The bot trades a custom pattern and divergence or convergence of price and indicator | `Private` |
| 10 | **Daily Inside Bar Setup** <br> The bot for DIBS strategy | `Private` |
| 11 | **[Pattern 34 Detector](/algo/indicators/018-pattern34/)** <br> The bot detects custom "Pattern 34" and trades from it on FX or BO | `Public` |
| 12 | **Volume Candle** <br> The bot detects and trades custom "Volume Candlestick" pattern | `Private` |
| 13 | **Elder Divergence** <br> The Elder MACD/RSI Divergence Strategy | `Private` |
| 14 | **Tip Top AI** <br> The bot uses AI generated strategy to detect entry point by Tail length algorithm | `Public` |

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
| 1 | **DS-XBarNewsDelay-MT5-Bot** <br> News breakout strategy: enters on sustained move after key macro releases (NFP, CPI, FOMC) | `Private` |
| 2 | **[FridayGoldRush-MT5-Bot](/algo/rating/051-fridaygoldrush-mt5-bot/)** <br> The bot exploits a day-of-week pattern on XAUUSD: buy Thursday, sell Friday <br> Free download [MQL5 Market](https://www.mql5.com/en/market/product/131729) | `Public` |
| 3 | **News Breakout** <br> The bot catches breakout at the moment of a significant news release | `Private` |
| 4 | **News Flow** <br> The bot trades breakout at news release in the direction of overall economic expectations | `Private` |
| 5 | **Virtual Order News Trading Bot** <br> Trade on outstanding news and try to catch strong price moving | `Private` |

### Arbitrage

High-frequency and statistical arbitrage across brokers and exchanges.

| # | Name | Type |
|---|------|------|
| 1 | **DS-HTF-SpreadScalper-MT5-Bot** <br> HFT Spread Scalper: exploits asynchronous Bid/Ask pricing by placing limit orders inside the spread with tick-speed and spread-stability filters | `Private` |
| 2 | **DS-Carry-MT5-Bot** <br> Carry Trade: multi-pair bot that profits from positive swap differentials with trend (MA) and momentum (ADX+RSI) filters | `Private` |
| 3 | **Sport Bet Arbitrage** <br> Cross-market arbitrage strategy | `Private` |
| 4 | **Crypto Advanced Arbitrage Bot** <br> Advanced crypto arbitrage Telegram bot for Binance, Bybit, KuCoin, OKX | `Private` |
| 5 | **HTF Arbitrage** <br> The MetaTrader 4&5 HFT Bots with third party highspeed updating rates API | `Private` |

### Tools & Assistants

Utilities, GUI assistants, and risk management tools for traders.

| # | Name | Type |
|---|------|------|
| 1 | **Metarun** <br> Picks the best optimization runs of an EA in MetaTrader 5 Strategy Tester and generates a report | `Private` |
| 2 | **[NYMB-MGridAssistant-MT5-Bot](/algo/rating/049-nymb-mgridassistant-mt5-bot/)** <br> A bot assistant works with a manual trade, automatically averaging it with two Martingale grids | `Private` |
| 3 | **Order Book Scanner** <br> This tool lets you keep an order book history in SQLite and then look at it later | `Private` |
| 4 | **[Multi TF Trend Tool](/algo/rating/031-mtf-trend-tool/)** <br> The tool to check multi TF trend using SMC structure | `Public` |
| 5 | **Crypto Tele Broker** <br> The Telegram bot executes transactions on cryptocurrency exchanges based on users' messages | `Private` |
| 6 | **Trading Time Indicator** <br> The indicator draws the periods available for trading on the chart | `Private` |
| 7 | **Stat Script** <br> The script generates a report on the history of EA trades, filtering them by comment part or magic number | `Private` |
| 8 | **AutoLocker** <br> The bot locks positions when drawdown is reached | `Public` |
| 9 | **STP Tool** <br> The bot places different orders based on manually drawn Fibonacci-Object | `Private` |

### Indicators

Public open-source indicators for MetaTrader 5 — see the full [Indicators](/algo/indicators/) section.

| # | Name |
|---|------|
| 1 | **ATRRange-MT5-Ind** <br> ATR Range: draws three volatility channels around price using ATR with configurable multipliers — [MQL5 Market](https://www.mql5.com/en/market/product/162717) |
| 2 | **SessionRange-MT5-Ind** <br> Custom Session Range: draws High/Low/Middle channel for a configurable trading session with Previous Day and Current Day modes — [MQL5 Market](https://www.mql5.com/en/market/product/162711) |
| 3 | **[PADD-Fractal-MT5-Ind](/algo/indicators/066-padd-fractal-mt5-ind/)** <br> Flexible fractal configuration with sorted high/low filtering — [MQL5 Market](https://www.mql5.com/en/market/product/139095) |
| 4 | **[SessionMA-MT5-Ind](/algo/indicators/062-sessionma-mt5-ind/)** <br> MA calculated only within a specified session time window — [MQL5 Market](https://www.mql5.com/ru/market/product/138136) |
| 5 | **[ClassicRenkoOnTick-MT5-Ind](/algo/indicators/061-classicrenkoontick-mt5-ind/)** <br> Real-time classic Renko charts focused on price movement — [MQL5 Market](https://www.mql5.com/ru/market/product/137132) |
| 6 | **[MAChannel-MT5-Ind](/algo/indicators/060-machannel-mt5-ind/)** <br> A channel around MA with three buffers: MA, Top, Bottom — [MQL5 Market](https://www.mql5.com/en/market/product/135784) |
| 7 | **[ChaikinMoneyFlow-MT5-Ind](/algo/indicators/059-chaikinmoneyflow-mt5-ind/)** <br> CMF indicator to monitor accumulation and distribution — [MQL5 Market](https://www.mql5.com/ru/market/product/135679) |
