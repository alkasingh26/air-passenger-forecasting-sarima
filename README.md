# Air Passenger Forecasting using SARIMA

## Project Overview

This project develops a Seasonal AutoRegressive Integrated Moving Average (SARIMA) model to forecast monthly airline passenger demand. The workflow covers data preprocessing, stationarity testing, model selection, parameter tuning, model evaluation, and future forecasting.

## Dataset

- Source: Airline Passengers dataset
- Time Period: 1949–1960
- Frequency: Monthly
- Observations: 144

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn
- Jupyter Notebook

## Methodology

- Data preprocessing
- Exploratory Data Analysis
- Augmented Dickey-Fuller (ADF) Test
- First-order and seasonal differencing
- ACF & PACF analysis
- SARIMA model development
- Hyperparameter tuning
- Forecast evaluation
- Future demand forecasting

## Final Model

SARIMA(1,1,2)(0,1,2,12)

## Model Performance

| Metric | Value |
|--------|------:|
| MAE | 38.31 |
| RMSE | 41.92 |
| R² Score | 0.6850 |

## Results

The tuned SARIMA model successfully captured the long-term trend and annual seasonality in airline passenger demand while substantially improving forecasting accuracy over the initial model.

## Future Forecast

The final model forecasts passenger demand for the next 12 months, predicting continued growth with recurring seasonal peaks.

## Repository Structure
