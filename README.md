# Dual‑Branch LSTM + Black–Litterman

**Overview**  
Use a dual‑branch LSTM to forecast 5‑day log‑returns for six U.S. stocks, then build portfolios via Markowitz and Black–Litterman.

**Features**  
- **Technical**: SMA, RSI, MACD, ATR, OBV  
- **Macro**: VIX & 10Y yield + 5‑day momentum  

**Model**  
- LSTM(64) for technical + LSTM(32) for macro  
- Concatenate → Dense → 6‑dim return vector  

**Portfolio**  
- **Markowitz**: directly uses LSTM forecasts  
- **Black–Litterman**: blends market‑implied returns with LSTM views  
