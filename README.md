#  Time Series Forecasting of Brent Crude Oil Prices

##  Overview

This project forecasts daily Brent crude oil prices using two time series models:  
- **ARIMA**: Captures autocorrelation and short-term patterns.  
- **Facebook Prophet**: Captures trend and seasonality in non-stationary data.

Data spans **July 2020 to Dec 2022** for training and **Jan 2023 to June 2025** for validation.

---

##  Key Steps

1. **Data Cleaning**  
   - Handled missing values, duplicates  
   - Converted to daily frequency  

2. **Stationarity Check**  
   - ADF Test, ACF/PACF plots  
   - Differencing applied (ARIMA only)

3. **Model Building**  
   - ARIMA(6,1,7) via grid search  
   - Prophet with default + tuned settings  

4. **Forecasting & Evaluation**  
   - 24-month forecast  
   - Compared to real prices (2023–2025)  
   - RMSE used for evaluation

---

##  Results Summary

| Metric          | ARIMA     | Prophet   |
|-----------------|-----------|-----------|
| RMSE (In-Sample)| 2.17      | 3.12      |
| RMSE (Forecast) | 5.90      | 6.45      |

- **ARIMA**: Better short-term accuracy  
- **Prophet**: Easier to interpret trends  
- **Limitation**: Both models missed external shocks (e.g., geopolitics)

---

##  Future Enhancements

- Include exogenous factors (SARIMAX)  
- Try hybrid models (ARIMA + LSTM)  
- Use news sentiment for better real-world adaptation

---

##  References

- Hyndman & Athanasopoulos, *Forecasting: Principles and Practice*  
- Taylor & Letham, *Forecasting at Scale*  
- [EIA Brent Oil Prices](https://www.eia.gov/dnav/pet/pet_pri_spt_s1_d.htm)  
- [Statsmodels](https://www.statsmodels.org) | [Prophet](https://facebook.github.io/prophet)

---

##  Status

 Completed as part of academic coursework – July 2025  
 All files and results available in this repository




