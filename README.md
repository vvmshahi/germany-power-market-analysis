# Germany Power Market Analysis & Price Forecasting

## Overview

This project analyzes electricity price behavior in the German power market using ENTSO-E data (2022–2024).

The objective is to understand key market drivers, identify price spikes, and build predictive models to support trading and decision-making.

---

## Dataset

- Source: ENTSO-E Transparency Platform
- Data:
  - Day-ahead electricity prices
  - Actual electricity demand (load)
- Frequency: 15-minute data aggregated to daily level
- Time period: 2022–2024

---

## Key Analysis

### 1. Price Behaviour
- Significant volatility observed during 2022 energy crisis
- Price normalization in 2023–2024

### 2. Demand vs Price
- Weak correlation (~0.2)
- Indicates demand alone is insufficient to explain price movements

### 3. Price Spikes
- Extreme price events identified using 95th percentile
- Spikes clustered during high-volatility periods

---

## Feature Engineering

To improve predictive performance, additional features were created:

- Lag features: `price_lag1`, `price_lag7`
- Rolling statistics: `price_ma7`, `load_ma7`
- Time features: day of week, month

---

## Models

### Linear Regression
- Poor performance due to non-linear price dynamics

### Random Forest Regressor
- MAE: ~21 EUR/MWh
- R²: ~0.41
- Captures non-linear relationships and temporal dependencies

---

## Key Insights

- Electricity prices are highly volatile and driven by multiple factors
- Demand alone is not a strong predictor of price
- Historical price patterns (lags) significantly improve forecasting accuracy
- External market conditions likely play a major role in price spikes

---

## Trading Perspective

- Price spikes represent potential trading opportunities
- Predictive modeling can support short-term price expectations
- Incorporating additional factors (weather, fuel prices) could improve strategy performance

---

## Tools Used

- Python
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab

---

## Project Structure

germany-power-market-analysis/
│
├── germany_power_market_analysis.ipynb
├── README.md



---

## Conclusion

This project demonstrates an end-to-end workflow from raw market data to actionable insights and predictive modeling, aligned with real-world energy market analysis and trading use cases.
