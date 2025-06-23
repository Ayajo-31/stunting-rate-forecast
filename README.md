# Title: Forecasting Stunting in Nigeria

## Background
Malnutrition persists as a major public health challenge in Nigeria, and it plays a role in the high child mortality rate in Nigeria. Stunting (height for age), that is, a child who is too short for his or her age, is high in Nigeria, ranging between 36% to 41% between 2003 to 2023, according to NDHS. This indicates that approximately 4 children in every 10 in Nigeria are stunted. Now, with the inflation rate in Nigeria skyrocketing, getting to its peak in 2025, it is still projected to keep increasing (The ARIMA model forecasts ever-rising inflation rates). Which begs the question: inflation rises, the consumer-price index keeps increasing, and food becomes more costly to produce and too expensive to buy. This puts children at risk of not getting adequate food for their growth and development. This makes them vulnerable to death. These deaths (as well as stunting because it affects the cognitive development of the child) rob Nigeria of demographic dividends.

## Goal
Build a time series forecasting model (ARIMA/Bayesian) to predict stunting prevalence among under-5 children and the influence of inflation on future stunting rates.

## Data Source
NDHS (2003, 2008, 2013, 2023) and Statista, and worlddata. ![Click here for inflation data sources](https://www.statista.com/statistics/383132/inflation-rate-in-nigeria/) [](https://www.worlddata.info/africa/nigeria/inflation-rates.php)

## Method
Tried ARIMA for forecasting stunting rates, shifted to Bayesian due to data irregularity.

### Project Steps
1. I got stunting rates using NDHS reports, and inflation rates using Statista and WorldData reports.
2. Prepared and scaled the Data.
3. Built the Bayesian Regression Model and checked Posterior Results, which revealed the model fitted properly (suitable for small data, fixing the problem I had with the ARIMA models).
5. Switched to Bayesian time series (PyMC) modeling.
6. Predicted future stunting based on projected inflation.

## Outcome
The Bayesian model revealed that if inflation increases by 1 standard deviation, stunting increases by ~1 percentage point. The chart below shows what the Nigeria under-5 stunting rate will be if based on inflation rates.
![Stunting Forecast](https://github.com/Ayajo-31/stunting-rate-forecast/blob/main/forecast_stunting_rate_2028_vs_inflation_rate.png)

[Click here to view the raw notebook](https://github.com/Ayajo-31/stunting-rate-forecast/blob/main/Bayesian_Timeseries_for_Analysis.ipynb)
⚠️ Note: GitHub notebook rendering has issues due to widget metadata. For now, open the raw file or upload to Google Colab.

## Next Steps
- Explore machine learning alternatives
- Explore wasting rates
