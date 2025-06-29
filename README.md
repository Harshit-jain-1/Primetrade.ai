# Primetrade.ai
#  Bitcoin Market Sentiment & Trader Performance Analysis

## Overview

This project explores the relationship between **Bitcoin market sentiment** (Fear/Greed) and **historical trader performance** on Hyperliquid.  
It aims to uncover hidden patterns that can help develop smarter trading strategies.

---

##  Datasets

- **Bitcoin Market Sentiment**
  - Columns: `Date`, `Classification` (`Fear` or `Greed`)

- **Hyperliquid Trader Data**
  - Columns: `Account`, `Coin`, `Execution Price`, `Size Tokens`, `Size USD`, `Side`, `Timestamp IST`, `Start Position`, `Direction`, `Closed PnL`, `Transaction Hash`, `Order ID`, `Crossed`, `Fee`, `Trade ID`, `Timestamp`

---

## ⚙️ Features

- Clean and merge both datasets by `Date`
- Label encode categorical columns (`symbol`, `event`, `side`)
- Add engineered features (`win` flag, dummy `leverage`)
- Join daily sentiment with trades to see how sentiment affects trading outcomes
- Build multiple visualizations to reveal hidden patterns
- Train a simple ML model to predict profitable trades, comparing performance **with vs without** sentiment data

---

## 📊 Visualizations

The analysis includes:
1. **7-Day Rolling Average of Fear/Greed Sentiment** - Sentiment Trend by lineplot
2.**Bitcoin Fear/Greed Over Time** — how profit varies in Fear vs Greed 
3. **Leverage vs Closed PnL** — scatter plot colored
4. **Feature Correlation Matrix** — see the corelation by heatmap
5. **Daily Total PnL ** — time series view of profit trends
6. **Closed PnL Distribution** — shows overall profit/loss spread

---

## 🤖 Machine Learning

- **Target:** Predict if a trade will be profitable (`win` flag)
- **Features:** Execution Price, Size, Fee, Leverage, Symbol (encoded), Event (encoded), Side (encoded), Sentiment
- Trains a `RandomForestClassifier` and compares accuracy with and without sentiment data
- Evaluates performance with **accuracy**, **classification report**, and **confusion matrix**

---
