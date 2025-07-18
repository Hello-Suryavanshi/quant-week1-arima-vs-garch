ARIMA vs GARCH: Predicting Volatility of the S&P 500

Objective
Compare ARIMA and GARCH models in predicting the daily volatility of S&P 500 log returns using 10 years of data.

Models Used
- ARIMA(1,0,1) model on returns
- GARCH(1,1) model on returns to model volatility clustering

Evaluation Metrics
- ARIMA  
  - RMSE: 0.7455  
  - MAE: 0.5245

- GARCH 
  - RMSE: 0.2743  
  - MAE: 0.1795

GARCH significantly outperformed ARIMA in forecasting volatility.

Visualizations
- Actual vs predicted volatility plot
- Volatility model disagreement plot (ARIMA vs GARCH)

How to Run
1. Clone the repo
2. Install dependencies:
pip install -r requirements.txt
3. Run the notebook inside `notebook/`

What I Learned
- Volatility is not constant — it clusters
- GARCH is great for capturing real-world financial risk
- ARIMA is limited in modeling financial return volatility
