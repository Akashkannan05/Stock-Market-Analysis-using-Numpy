# Stock Market Analysis & Forecasting Tool (Practice Project)

This project is a **Python-based stock market analysis and forecasting tool**, developed purely for **learning and practice purposes**.

It performs a comprehensive set of technical analyses and basic trend prediction using historical stock data and Nifty index data (or any similar market index). The tool is interactive and helps understand how various stock indicators are calculated and interpreted in real-world trading.

---

## Purpose of This Project

This project was created as a **personal learning exercise** to:
- Understand how to work with financial datasets using **Pandas** and **NumPy**
- Learn how technical indicators like **SMA, EMA, RSI, Beta, ATR** are calculated
- Practice **data visualization** using **Matplotlib**
- Implement **simple linear regression** for stock price forecasting
- Improve Python programming skills and numerical logic

---

## Features and Functionalities

### 1. CSV Data Loading & Cleaning
- Reads two CSV files (one for stock data, one for index/market data)
- Cleans up commas in numerical columns
- Converts the cleaned data to NumPy arrays

### 2. Feature Extraction
- Extracts key stock data columns:
  - `Date`, `Open`, `High`, `Low`, `PrevClose`, `Close`, `VWAP`, `Volume`, etc.
- Converts string data to appropriate numeric types

### 3. Returns Calculation
- **Daily Returns**:  
  \[(\text{Close} - \text{PrevClose}) / \text{PrevClose}\]
- **Cumulative Returns**:  
  \[(\text{Close} - \text{Last Close}) / \text{Last Close}\]

### 4. Simple Moving Average (SMA)
- User input for period (5, 50, 200 days)
- Compares SMA with current price to determine trend:
  - Uptrend / Downtrend / Stable

### 5. Exponential Moving Average (EMA)
- Calculates EMA using:
  \[\text{EMA}_t = \text{Price}_t \cdot \alpha + \text{EMA}_{t-1} \cdot (1 - \alpha)\]
- Smooths recent price action with more weight on recent data

### 6. Volatility Metrics
- **Standard Deviation %**: Indicates overall volatility
  - < 3% → Safe
  - > 6% → Suitable for traders
- **Average True Range (ATR)**:
  - Indicates how much the stock price moves on average each day
  - Useful for setting stop-loss levels

### 7. Beta (β) – Market Correlation
- Compares stock and market (Nifty) returns
- Indicates:
  - β > 1: More volatile than market
  - 0 < β < 1: Less volatile
  - β < 0: Inversely correlated

### 8. Volume & Trend Strength
- Compares SMA and Volume Moving Average (VMA)
- Uses percentage match to determine:
  - Strong uptrend / Weak uptrend
  - Strong downtrend / Weak downtrend

###  9. RSI – Relative Strength Index
- Measures momentum of price movement
- RSI > 70 → Overbought (possible drop)  
- RSI < 30 → Oversold (possible rise)

### 10. Stock Price Prediction (Linear Regression)
- Fits a regression line using recent closing prices
- Predicts next 3 days of prices
- Plots:
  - Actual prices
  - Regression line
  - Forecasted prices

---

## 🛠 Technologies Used

- **Python**
- **NumPy**
- **Pandas**
- **Matplotlib**

---

## ⚠️ Disclaimer

> This tool is created **only for practice and educational purposes**.  
> It is **not intended for actual trading, investing, or financial advice**.  
> Real-world stock trading involves many more factors, data sources, and risk considerations.

---

## 📌 How to Use

1. Clone or download the script.
2. Make sure you have the required packages:
   ```bash
   pip install numpy pandas matplotlib
