# 📘 ऑर्डर के प्रकार (Types of Orders in Trading)
**सम्पूर्ण गाइड इन हिंदी – Beginner से Pro Traders तक**

---

## 🔶 भूमिका (Introduction)

जब आप किसी भी बाजार में (जैसे: Stock, Forex, Commodity, Futures) ट्रेड करते हैं, तो ब्रोकर को अपनी "Buy" या "Sell" की इच्छा बताने के लिए आपको **Order Place** करना होता है।

📌 पर सवाल है:

- क्या तुरंत खरीदना चाहिए या किसी खास भाव पर?
- गिरते प्राइस में नुकसान कैसे रोका जाए?
- टारगेट हिट होते ही प्रोफिट कैसे लॉक हो?

➡️ इन जरूरतों के लिए Market में अलग-अलग प्रकार के Orders होते हैं।

---

## 📑 इस गाइड में हम 4 मुख्य Order Types को समझेंगे:

1. Market Order  
2. Limit Order  
3. Stop Loss Order  
4. Bracket Order  

---

## 🔷 1. Market Order (मार्केट ऑर्डर)

📖 **परिभाषा:**  
Market Order वह होता है जिसमें आप मौजूदा Price पर तुरंत Buy/Sell करना चाहते हैं।

🔧 **तकनीकी व्याख्या:**  
कोई Price Limit नहीं होती। Broker जिस प्राइस पर सबसे पहले ऑर्डर match कर सकेगा, वहीं Execute कर देगा।

📉 **व्यवहारिक उदाहरण:**  
Infosys ₹1540 पर दिख रहा था। Market Order लगाया → Actual Execution ₹1542 पर हुआ (यह Slippage कहलाता है)

⚖️ **फायदे:**
- Execution तुरंत होता है ✅
- कोई opportunity Miss नहीं होती ✅

❌ **नुकसान:**
- Price Control नहीं होता ❌  
- Volatile Market में ज्यादा Slippage ❌

🎯 **कब प्रयोग करें?**  
👉 जब आपको तुरंत Entry/Exit करनी हो

---

## 🔷 2. Limit Order (लिमिट ऑर्डर)

📖 **परिभाषा:**  
Limit Order में आप खुद तय करते हैं कि किस Price पर Order Execute होना चाहिए।

🔧 **तकनीकी व्याख्या:**  
Order तब तक **Pending** रहेगा जब तक Market उस Price तक न आ जाए।

📉 **व्यवहारिक उदाहरण:**  
TCS ₹3820 चल रहा है, आप ₹3800 पर Limit Buy Order लगाते हैं। अगर Price वहां तक नहीं आया → Order Executed नहीं होगा।

⚖️ **फायदे:**
- Price Control ✅  
- Slippage से बचाव ✅

❌ **नुकसान:**
- Execution की गारंटी नहीं ❌  
- Trade छूट सकता है ❌

🎯 **कब प्रयोग करें?**  
👉 Swing या Positional Trading में

---

## 🔷 3. Stop Loss Order (स्टॉप लॉस ऑर्डर)

📖 **परिभाषा:**  
नुकसान को रोकने के लिए लगाया गया **सुरक्षा कवच** — जब प्राइस एक Trigger Level पर पहुंचे तो ऑटोमैटिक Sell हो जाए।

🔧 **प्रकार:**

### 🅐 SL – Stop Loss Limit:
- Trigger Price: ₹95  
- Limit Price: ₹94.80  
- Execution: Price ₹95 हिट होते ही Attempt होता है ₹94.80 पर Fill करने का

### 🅑 SL-M – Stop Loss Market:
- सिर्फ Trigger Price देते हैं  
- Trigger Hit होते ही **Market Price** पर Auto Execution

📉 **उदाहरण:**  
आपने ₹7000 पर शेयर खरीदा, ₹6900 पर SL-M लगाया → Price गिरकर ₹6898 पर Auto Sell हो गया।

⚖️ **फायदे:**
- Loss Control ✅  
- Discipline बनी रहती है ✅

❌ **नुकसान:**
- SL-M में Price Control नहीं ❌  
- SL में Fill की गारंटी नहीं ❌

🎯 **कब प्रयोग करें?**  
👉 Intraday / Futures में अनिवार्य

---

## 🔷 4. Bracket Order (ब्रैकेट ऑर्डर)

📖 **परिभाषा:**  
एक Advanced Order जिसमें आप Entry, Stop Loss और Target — तीनों एकसाथ Define करते हैं।

🔧 **तकनीकी व्याख्या:**  
जिसमें OCO Logic (One Cancels Other) होता है:  
👉 एक Hit होगा, दूसरा Auto-Cancel।

📉 **उदाहरण:**  
Entry: ₹500  
Target: ₹510  
SL: ₹495  
➡️ ₹510 Hit → Profit Booked, SL Cancelled

⚖️ **फायदे:**
- Auto Exit ✅  
- Risk/Reward Pre-Defined ✅

❌ **नुकसान:**
- हर ब्रोकर सपोर्ट नहीं करता ❌  
- थोड़ा Complex हो सकता है ❌

🎯 **कब प्रयोग करें?**  
👉 Intraday Strategy Trades में

---

## 📊 तुलना तालिका (Comparison Table)

| ऑर्डर टाइप | Execution Speed | Price Control | Risk Management | प्रयोग कब करें? |
|------------|------------------|----------------|------------------|------------------|
| 🟢 Market Order | ⚡ Fast | ❌ नहीं | ❌ नहीं | Beginners / Urgent Entry |
| 🟡 Limit Order | ⏳ Medium | ✅ हाँ | ❌ नहीं | Positional / Precise Entry |
| 🔴 Stop Loss | ⏱ Auto on Trigger | ✅ (SL) / ❌ (SL-M) | ✅ हाँ | Risk-Controlled Trading |
| 🟣 Bracket Order | 🤖 Auto | ✅ हाँ | ✅ Full | Intraday Strategy Trades |

---

## 📚 निष्कर्ष (Conclusion)

हर ऑर्डर टाइप का उपयोग उसकी Situation पर निर्भर करता है:

- **📢 Market Order** → जब तुरंत एंट्री चाहिए
- **🎯 Limit Order** → जब Price Control ज़रूरी हो
- **🛡️ Stop Loss** → जब Risk को Control करना हो
- **🧠 Bracket Order** → जब Discipline + Auto Exit चाहिए

✅ एक सफल Trader वही है जो सही समय पर **सही Order Type** का चुनाव करता है।

---

