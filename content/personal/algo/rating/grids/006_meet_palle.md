---
title: Meet PALL-E
type: docs
prev: grids
next: 
sidebar:
  open: true
draft: false
publishDate: 2023-10-18
---

![Reinforced Grid Bot](/images/personal/050/050.%20palle_logo_200x200.svg)

In 2023, many robots were draining deposits on gold, even on conservative settings. I did [research on the reasons for the drains]({{< ref "/personal/algo/research/baza/003_eve_siyah_carsamba" >}}) on one of the popular trading bots. At that time I came to the following conclusions:

{{< callout type="error" >}}
**Main Conclusion:** Grid robots with Martingale averaging and no protection against deposit drain will lose it. 
{{< /callout >}}

{{< callout type="warning" >}}
**Main Sequence:** I will write my own advisor with deposit protection. It will definitely not be a fast way...
{{< /callout >}}

## The PALL-E Trading Bot

A year of development, research, strategy improvements and optimisation of settings for **_safe_** (as safe as possible) grid trading with averaging has passed. The result is the **_PALL-E_** trading bot for MetaTrader 5.

A trading strategy is implemented in *PALL-E*:

{{% steps %}}

### Opening Trades Only On the Trend
The bot uses a combination of indicators: RSI, custimised MA, ADX, ZigZag and SuperTrend, simultaneously and on different timeframes.

### Safe Martingale Averaging
This is the main feature of the bot. The bot does not average until it detects a trend reversal. Each next position is only opened when the trend has reversed to the right of the grid. As a result, the bot has no open positions at fixed intervals. The averaging distances depend on the current price behaviour.

### Adaptive TakeProfit and Averaging Distances
The bot determines the appropriate distance for the next averaging and can dynamically adjust the TP of the grid at each averaging knee.

### Automatic Locking on Drawdown
The function of locking open positions and stopping Expert Advisors when the set drawdown level is reached is placed in a separate bot that works on accounts where other robots are trading simultaneously. 

{{% /steps %}}

## PALL-E Testing Results for XAUUSD 

*Broker*: Roboforex-Pro 
*Model*: Real Ticks
*Initial deposit*: $100000

### Conservative Set

*Interval*: 01.01.2018-01.10.2024
*Profit*: starting 3% to 10% per month.
*Drawdown*: 17%
*Potential drawdown if PALL-E started averaging the moments of gold's biggest non-stop moves from 2018 to 2024*: 37% 

![Conservative](/images/personal/050/050.%202024-10-01-Conservative-0.03.png)
Full report on MT5 testing results - [download zip](https://github.com/sournk/baza_bot_backtest/blob/main/050/XAUUSD-2024-10-01-Conservative-0.03.zip).

### Aggressive Set

These settings cannot be applied to any historical period. They are highly dependent on the current nature of the instrument's movement. They should be reviewed regularly and **applied only in periods when the instrument is in a standard price movement!**

*Interval*: 01.01.2024-01.10.2024
*Profit*: 13,6% per month
*Drawdown*: 20%

![Aggressive](/images/personal/050/050.%202024-10-01-Aggressive.png)
Full report on MT5 testing results - [download zip](https://github.com/sournk/baza_bot_backtest/blob/main/050/XAUUSD-2024-10-01-Aggressive.zip).

## Inputs

### Basic Strategy Settings
![Basic settings](/images/personal/050/050.%20Inputs-0.png)

### Indicator Combination Settings

![SuperTrend](/images/personal/050/050.%20Inputs-1.png)

![MA](/images/personal/050/050.%20Inputs-2.png)

![ZigZag](/images/personal/050/050.%20Inputs-3.png)

![ADX](/images/personal/050/050.%20Inputs-4.png)

![RSI](/images/personal/050/050.%20Inputs-5.png)

## Bot Usage Options

1. **Copytrading on RoboForex with conservative settings**. 
    - *Subscription:* Free and without verification.
    - *Account Type:* Pro-Cent.
    - *Minimum deposit:* $1000.
    - *Commission on profit:* 15%.
    - *Lock positions:* At 40% drawdown. 
    - *Adjustment of settings: Regularly once a month.
2. **Copytrading on RoboForex with aggressive settings**. 
    - *Subscription:*Free and without verification.
    - *Account Type:* Pro-Cent.
    - *Minimum deposit:* $1000.
    - *Commission on profit:* 15%.
    - *Lock positions:* None.
    - *Adjustment of settings: Regularly once a month.
3. **Installation of the bot in your MetaTrader 5**. 
    - **Robot price:* Price is negotiable at **Installation of the bot to your RoboForex referral account**.
    - *Account type:* Pro-Cent.
    - *Minimum deposit:* Any.
    - *Commission on profit:* 0%.
    - *Lock of positions:* Customizable at will.    
    - *Adaptation of settings*: Performed by yourself if necessary.

{{< callout type="info">}}
Text to Telegram **[@sournkz](https://t.me/sournkz)** to connect copytrading or install the robot in your terminal.
{{< /callout >}}

 ## Important Warning

1. The PALL-E robot does not guarantee a profit.
2. The PALL-E robot does not guarantee deposit protection.
3. The PALL-E robot can hold positions from a few minutes to several weeks.
4. use the PALL-E robot at your own risk.
