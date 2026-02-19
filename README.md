# Germany Power Market Analysis

## Overview
This project analyzes electricity prices and demand in Germany using ENTSO-E data.

The goal is to understand price behavior, detect spikes, and build predictive models.

---

## Dataset
- Source: ENTSO-E Transparency Platform
- Data:
  - Day-ahead electricity prices
  - Actual total load
- Time period: 2022–2024

---

## Key Analysis

### 1. Price Trends
- Strong volatility observed in 2022
- Stabilization in later years

### 2. Load vs Price
- Weak correlation (~0.2)
- Indicates external factors influence prices

### 3. Price Spikes
- Detected using 95th percentile
- Concentrated in high-volatility periods

---

## Feature Engineering
- Lag features (price_lag1, price_lag7)
- Rolling averages (price_ma7, load_ma7)
- Time features (day of week, month)

---

## Models

### Linear Regression
- Poor performance (non-linear problem)

### Random Forest Regressor
- MAE: ~21 EUR/MWh
- R²: ~0.41

---

## Key Insights

- Electricity prices are highly volatile
- Demand alone does not explain price movements
- Historical price patterns are important predictors

---

## Tools Used
- Python
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab

---

## Project Structure
