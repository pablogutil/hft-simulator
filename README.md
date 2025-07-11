# HFT Strategy Simulator ⚡📉

A simplified high-frequency trading (HFT) backtesting engine — perfect for testing market-making, arbitrage, and latency-sensitive strategies.

---

## 💡 What It Does

- ⏱️ Simulates nanosecond-level execution latency  
- 🧮 Runs backtests on real-time or historical order book data  
- 💹 Tests naive HFT strategies:  
  - Market making  
  - Spread arbitrage  
  - Momentum bursts  

- 📊 Live PnL and order flow charts with Plotly

---

## ⚙️ Tech Stack

- **Python** (`asyncio`, `pandas`, `numpy`)
- **Data Sources:** Alpaca API or `ccxt` (for crypto)
- **Visualization:** Plotly Dash

---

## 🧪 Example Strategy

```python
# Market maker strategy
if best_bid - best_ask > spread_threshold:
    place_limit_order('buy', best_bid - 0.01)
    place_limit_order('sell', best_ask + 0.01)
