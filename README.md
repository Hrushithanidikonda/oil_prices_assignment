#  Time Series Forecasting of Brent Crude Oil Prices
## Project Summary

This repository contains a comprehensive time series analysis and forecasting of Brent crude oil prices using two widely used models: **ARIMA (AutoRegressive Integrated Moving Average)** and **Facebook Prophet**. The project aims to model and predict oil prices using historical data from July 2020 to December 2022 and validate the forecasts using real data from January 2023 to June 2025.

The focus is not only on model implementation but also on **critical analysis**, **model comparison**, and **forecast interpretation**, making it suitable for academic and applied research.

---

##  Objectives

- Preprocess and analyze daily Brent crude oil price data.
- Test and enforce stationarity for ARIMA modeling.
- Implement and optimize both ARIMA and Prophet models.
- Forecast oil prices for 24 months beyond the training period.
- Evaluate forecasts against actual observed data.
- Provide insightful interpretation and future recommendations.

---

##  Repository Structure

```bash
 oil_prices_assignment/
├── Oil_Price_TimeSeries_ARIMA_Prophet_Forecasting.ipynb   # Main notebook
├── data/
│   ├── oil_price_cleaned.csv                               # Cleaned training data (2020–2022)
│   └── RBRTEd.csv                                           # Actual EIA data (2023–2025)
├── images/
│   ├── daily_prices.png                                     # Historical data plot
│   ├── acf_pacf.png                                         # ACF and PACF plots
│   ├── arima_forecast.png                                   # ARIMA forecast with CI
│   ├── prophet_forecast.png                                 # Prophet forecast vs actual
│   └── prophet_components.png                               # Prophet trend and seasonality
├── report.docx (or .pdf)                                   # Full academic report
└── README.md                                               # This file

##  Models Used
ARIMA (AutoRegressive Integrated Moving Average)
Suitable for stationary time series with autocorrelation.

Model selected: ARIMA(6,1,7) based on AIC minimization.

Required differencing (d=1) due to initial non-stationarity.

🔸 Facebook Prophet
Decomposable model for trend and seasonality.

Works well with non-stationary data and missing values.

Easily interpretable components (trend, yearly, weekly).

Model Evaluation

| Metric                  | ARIMA (6,1,7) | Prophet   |
| ----------------------- | ------------- | --------- |
| In-Sample RMSE          | 2.17          | 3.12      |
| Forecast RMSE (2023–25) | 5.90          | 6.45      |
| Interpretability        | Medium        | High      |
| Handling Missing Data   | Moderate      | Excellent |

 Key Insights
Both models performed well up to 12 months, but diverged post-2024 due to external shocks.

Neither model accounts for exogenous factors such as policy changes or global conflicts.

Hybrid or multivariate approaches may offer better real-world performance.



