# 🔷 Pine Script Full Guide in Hindi (Ultra-Explained)

---

## 🔹 1. Pine Script क्या है? (Core Foundation)

**Pine Script** एक विशेष Programming Language है जो सिर्फ **TradingView** पर उपयोग होती है।

| उपयोग | उद्देश्य |
|-------|----------|
| Custom Indicator बनाना | RSI, EMA, VWAP जैसे Signals खुद डिज़ाइन करना |
| Alert Automation | Crossover या Pattern आने पर Notification |
| Strategy Testing | Backtest करना कि कोई Logic फायदे में है या नहीं |
| Visual Signals | Chart पर Signals, Labels, Color Change आदि लगाना |

📌 Syntax आसान है — Python, Java जैसे Complex Code की ज़रूरत नहीं होती।  
📌 सिर्फ कुछ लाइनों में आप एक Powerful Indicator या Strategy बना सकते हैं।

---

## 🔹 2. EMA क्या होता है? (Exponential Moving Average)

**EMA** एक Moving Average Indicator है जो Latest Price को ज्यादा Importance देता है।

| Parameter | 20 EMA | 50 EMA |
|-----------|--------|--------|
| Nature | Fast Moving | Slow Moving |
| Use | Entry / Scalping | Trend Confirmation |
| Suitable For | Intraday / Scalper | Swing / Positional Trader |

📈 जब **20 EMA**, 50 EMA को ऊपर से काटता है → Uptrend Start का Signal  
📉 जब 20 EMA, 50 EMA को नीचे से काटता है → Downtrend का Signal

---

## 🔹 3. Annotated Pine Script Code (Line-by-Line Explanation)

```pinescript
//@version=5
indicator("EMA Crossover with Signal", overlay=true)

> Pine Script का Version 5 सबसे नया है
> overlay=true मतलब Chart के ऊपर Indicator दिखाई देगा

e1 = ta.ema(close, 20)
e2 = ta.ema(close, 50)

> e1 → 20 EMA (Fast Line)
> e2 → 50 EMA (Slow Line)
> close मतलब Price का बंद होने वाला मूल्य

plot(e1, color=color.blue, title="20 EMA")
plot(e2, color=color.red, title="50 EMA")

> Chart पर 2 अलग-अलग रंगों की EMA Line Show होंगी

buy = ta.crossover(e1, e2)
sell = ta.crossunder(e1, e2)

> ￼Buy Signal: जब 20 EMA, 50 EMA को ऊपर से काटे
> Sell Signal: जब 20 EMA नीचे से काटे

plotshape(buy, location=location.belowbar, style=shape.labelup, color=color.green, text="BUY")
plotshape(sell, location=location.abovebar, style=shape.labeldown, color=color.red, text="SELL")

> Chart पर Auto Label Show होंगे – जहां Signal Trigger हुआ

alertcondition(buy, title="Buy Alert", message="20 EMA crossed above 50 EMA")
alertcondition(sell, title="Sell Alert", message="20 EMA crossed below 50 EMA")

> Alert डाल सकते हैं → जिससे Signal आते ही Email / App Notification मिल जाए

🔹 **4. इस Indicator को कैसे Use करें?**  
**Use Case:** *Intraday (15-Min Chart)*

| Condition        | Confirmation                              |
|------------------|--------------------------------------------|
| **Signal आया**   | 20 EMA ऊपर निकला 50 EMA से                 |
| **Trend**        | Chart पर Higher Highs बन रहे हों           |
| **Volume**       | Breakout के समय Volume ज़्यादा हो           |
| **Entry**        | Signal के बाद वाली Candle पर                |
| **SL**           | 20 EMA के नीचे                             |
| **Target**       | Previous Resistance या RR 1:2              |

🔹 5. Strategy Test कैसे करें?
आप इस Indicator को Strategy Mode में बदल सकते हैं:

//@version=5
strategy("EMA Crossover Strategy", overlay=true)

e1 = ta.ema(close, 20)
e2 = ta.ema(close, 50)

long = ta.crossover(e1, e2)
short = ta.crossunder(e1, e2)

if (long)
    strategy.entry("Buy", strategy.long)

if (short)
    strategy.close("Buy")

# 🔍 Strategy Tester में आपको यह जानकारी मिलेगी:

| 📊 Data           | 📘 Explanation                        |
|------------------|----------------------------------------|
| **Total Trades** | कितने Buy Signal आए                   |
| **Win %**        | कितने Profit में गए                   |
| **Net Profit**   | Total Profit/Loss (PL)                 |
| **Drawdown**     | Maximum नुकसान                        |
| **Avg Trade**    | Average Profit per Trade               |

📊 इसे आप TradingView के **“Strategy Tester”** Tab में देख सकते हैं।

---

# 🔹 6. Real Trading Routine (Live Market में कैसे Use करें)

| 🕒 Time   | 📋 Task                                               |
|----------|--------------------------------------------------------|
| **9:15** | Market Open → Chart पर 15M Timeframe खोलें              |
| **9:25** | EMA Script लगाएँ                                       |
| **9:30** | Alert On करें                                          |
| **9:35** | Signal आया → Candle Confirm करें                        |
| **9:40** | Entry करें → SL/TP सेट करें                            |
| **10:00**| Trade Track करें या Trail SL करें                      |

📌 **Important:**  
आपको Signal मिलेगा, पर **Entry तभी लें जब Volume + Candle दोनों Confirm करें।**

---

# 🔹 7. Advanced Ideas (Level Up Strategy)

| ⚙️ Add-On                         | 🎯 Benefit                                 |
|----------------------------------|--------------------------------------------|
| EMA + RSI > 50                   | Trend और Momentum Confirm होता है          |
| EMA + Volume Spike               | Breakout को Real मान सकते हैं              |
| EMA + Price Action (Pinbar)      | Fake Signal को Filter कर सकते हैं          |
| Multi-Timeframe EMA              | Higher Timeframe से Confirmation मिलता है  |
| Webhook Alert + Broker Bridge    | Automated Trading Possible होता है         |
