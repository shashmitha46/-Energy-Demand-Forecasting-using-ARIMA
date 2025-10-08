# Energy Demand Forecasting using ARIMA

Forecast electricity demand using ARIMA time-series modeling on historical load data.

## Project Overview

- **Objective:** Predict future electricity load (demand) based on past data using ARIMA modeling.  
- **Data:** Hourly energy load (and optionally solar generation) time series.  
- **Approach:**  
  1. Data preprocessing (handling missing values, converting timestamps)  
  2. Stationarity test (e.g. ADF)  
  3. Model parameter selection (p, d, q via ACF / PACF or auto methods)  
  4. Train ARIMA model  
  5. Forecast future load and compare against actuals  
  6. Evaluate using metrics like RMSE, MAE, MAPE  

## Results Summary
- The ARIMA model captures the overall trend and cyclic/daily fluctuations in the electricity load data.
- Forecasted values closely track the actual demand curve, especially for short-to-medium horizons.
- Evaluation metrics (RMSE, MAE, etc.) are relatively low, indicating good predictive accuracy.

### Limitations:
- ARIMA may struggle with strong seasonality over longer horizons.
- External factors (weather, holidays) are not included.
- Model retraining may be needed to adapt to changes over time.

## Future Enhancements
- Extend to SARIMA or Seasonal ARIMA to explicitly model seasonal patterns.
- Use ARIMAX by incorporating exogenous variables (temperature, holidays, economic indicators).
- Compare with machine learning or deep learning methods (e.g., Prophet, LSTM).
- Automate periodic model retraining and update forecasts in real time.

## Acknowledgments
- Satyajit Pattnaik - Special thanks for the comprehensive tutorial and guidance. This project was developed by following the tutorial: [Energy Demand Forecasting Tutorial](https://youtu.be/0KVsYgsaY5s?si=KHcwvUd5r3faYaBH)
- Time series forecasting methodology from statistical literature
- ARIMA implementation using statsmodels library
- Energy consumption datasets from public sources
