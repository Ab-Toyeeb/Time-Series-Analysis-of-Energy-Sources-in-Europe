# Time-Series-Analysis-of-energy-sources-in-Europe

This project focuses on the modeling and forecasting of energy generation across selected European countries using time series analysis. It leverages Seasonal ARIMA (SARIMAX) models to predict daily energy outputs of both renewable and non-renewable sources and evaluates forecast accuracy using multiple performance metrics.

**Objective**\
To build a single time series forecasting model that accurately predict the daily generation of four energy sources in selected European countries and evaluate the performance using RMSE, MAE, and MASE.

**Countries Analyzed**\
  Germany  
  Spain  
  Finland  
  Netherlands

**Energy Sources Modeled**\
 Fossil Gas,
 Fossil Hard Coal,
 Solar,
 Wind Onshore.

**Methodology**\
Modeling Approach
The SARIMAX model is employed for each energy source and country.
The configuration used is SARIMA(1,0,1)(1,0,1,7)
This reflects weekly seasonality (s=7), suitable for daily data.

Forecasts are generated on the test dataset for the first 90 days (January to March) of the year.

**Evaluation Strategy**\
Each forecast is evaluated against actual test data using three performance metrics:
1. RMSE (Root Mean Squared Error): Measures the average magnitude of forecast error.
2. MAE (Mean Absolute Error): Measures the average absolute difference between predicted and actual values.
3. MASE (Mean Absolute Scaled Error): Scales the absolute error by a naive seasonal forecast based on the training set. This allows model performance comparison across series of different scales.

**Project Pipeline**
1. Data Loading and Preprocessing  
   Normalized daily time series data are loaded for each country and energy source, split into training and testing sets.

2. Model Fitting
   A SARIMAX model is trained for each (country, energy) pair using the training data.

3. Forecasting
   Forecasts are generated for 90 days and aligned with actual test values.

4. Evaluation  
   Evaluation metrics (RMSE, MAE, MASE) are computed and printed for each country-energy pair.

5. Output Presentation  
   Evaluation results are printed in an interpretable format, highlighting performance variations across countries and energy types.

**File Structure**\
  Main notebook with complete code for:
  Data preparation
  SARIMAX modeling
  Forecasting
  Evaluation

**Dependencies**\
This project uses the following libraries:
pandas,
numpy,
statsmodels,
scikit-learn,
matplotlib,
seaborn,
scipy.

