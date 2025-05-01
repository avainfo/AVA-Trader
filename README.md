# Ava Trader

Ava Trader is an AI-powered crypto trading system designed to predict the short-term direction of the BTC/USDT market and execute high-confidence trades on Binance. The goal is to maximize profitability while minimizing risk through strict capital management and high-quality predictions.

---

## 🚀 Project Objectives

- **Predict** short-term market direction: `UP`, `DOWN`, or `STABLE` in the next **5 or 10 minutes**.
- **Trade** only when the model confidence is above a set threshold (e.g. ≥ 70%).
- **Maximize** win rate and risk/reward ratio.
- **Minimize** exposure to noise and drawdown.

---

## 🧠 Technical Stack

- **Target Asset**: BTC/USDT on Binance
- **Timeframe**: 1-minute candles
- **Prediction Horizon**: +5min and +10min
- **Prediction Type**: Multi-class classification (UP / DOWN / STABLE)
- **Trading Mode**: Semi-automated or fully automated

---

## 🔁 Project Pipeline

1. **Data Collection**
   - Historical 1-min OHLCV from Binance API
   - Real-time updates for live trading

2. **Feature Engineering**
   - Over 30 technical indicators (RSI, MACD, Bollinger Bands, etc.)
   - Time sequence construction (120-min sliding window)

3. **Labeling**
   - `UP`: +0.2% or more
   - `DOWN`: -0.2% or more
   - `STABLE`: between -0.2% and +0.2%

4. **Modeling**
   - Phase 1: LSTM
   - Phase 2: Transformer (if needed)
   - Hyperparameter tuning, early stopping, dropout

5. **Backtesting**
   - Evaluate on unseen historical data
   - Metrics: Accuracy, F1-score, Cumulative Return

6. **Paper Trading**
   - Run with real-time data, simulated capital

7. **Live Deployment**
   - Binance API integration for real orders
   - High-confidence signal execution

8. **Risk Management**
   - Max risk per trade: 1%
   - Stop Loss: -0.5%
   - Take Profit: +1%

---

## 📂 Folder Structure (WIP)

```
ava-trader/
├── data/                  # Raw and processed data
├── models/                # Trained models and configs
├── notebooks/             # Exploratory analysis
├── src/                   # Core Python code (features, models, etc.)
├── backtests/             # Strategy simulations
├── trading_bot/           # Live trading logic
├── dashboard/             # Visualization (Grafana/Streamlit)
└── docs/                  # Documentation
```

---

## 📊 Key Performance Targets

| Metric                     | Goal             |
|---------------------------|------------------|
| Accuracy                  | ≥ 55%            |
| Risk/Reward Ratio         | ≥ 1.5            |
| Max Drawdown              | ≤ 10%            |
| High Confidence Signals   | ≥ 30% of trades  |

---

## 📦 Requirements

- Python 3.10+
- Libraries: `pandas`, `numpy`, `ta`, `tensorflow` or `pytorch`, `ccxt`, `matplotlib`, etc.
- Binance API credentials (for live/paper trading)

---

## 📅 Roadmap

- ✅ Phase 1: Historical data collection
- 🔜 Phase 2: Feature engineering and labeling
- ⏳ Phase 3: Modeling (LSTM)
- 🧪 Phase 4: Backtesting
- 🟢 Phase 5: Paper trading
- 🟩 Phase 6: Real trading

---

## 📜 License

MIT — Feel free to use, modify, and contribute.

---

## 🤝 Contributions

If you want to contribute or adapt Ava Trader, feel free to open an issue or PR.

---

**Developed by Antonin Do Souto – 2025**
