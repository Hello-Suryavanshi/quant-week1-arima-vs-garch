📈 Week 1: ARIMA vs GARCH Volatility Prediction

This is Week 1 of my "Quant Learning-in-Public" series — a project-based exploration of financial modeling, AI, and data science.

🔍 Objective

Compare the performance of ARIMA(1,0,1) and GARCH(1,1) models in forecasting the volatility of daily returns on the S&P 500 Index.

📊 Data

- Source: [Yahoo Finance](https://finance.yahoo.com)
- Ticker: `^GSPC` (S&P 500 Index)
- Date Range: `2014-01-01` to `2024-12-31`

⚙️ Methodology

1. Download price data using `yfinance`
2. Compute log returns
3. Fit an ARIMA(1,0,1) model → estimate volatility via squared residuals
4. Fit a GARCH(1,1) model → estimate conditional volatility
5. Compute actual volatility using 21-day rolling standard deviation
6. Evaluate using RMSE and MAE

📈 Results

| Model | RMSE | MAE |
|-------|------|-----|
| ARIMA | 0.7455 | 0.5245 |
| GARCH | 0.2743 | 0.1795 |

> ✅ GARCH clearly outperformed ARIMA — making it a better candidate for volatility forecasting.

📷 Visuals

![Volatility Comparison](notebook/preview.png)

📦 Requirements
pip install -r requirements.txt
