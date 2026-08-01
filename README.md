# Air Passenger Forecasting using SARIMA

## Project Overview

This project develops a **Seasonal AutoRegressive Integrated Moving Average (SARIMA)** model to forecast monthly airline passenger demand. The project demonstrates the complete workflow of a time series forecasting problem, including data preprocessing, exploratory data analysis, stationarity testing, parameter tuning, model evaluation, and future forecasting.

The objective is to accurately model historical passenger demand and generate reliable forecasts for future months using a tuned SARIMA model.

---

## Dataset

- **Dataset:** Airline Passengers Dataset
- **Time Period:** January 1949 – December 1960
- **Frequency:** Monthly
- **Observations:** 144
- **Target Variable:** Total Monthly Airline Passengers

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn
- Jupyter Notebook

---

## Project Workflow

- Data Loading and Preprocessing
- Exploratory Data Analysis (EDA)
- Stationarity Testing using the Augmented Dickey-Fuller (ADF) Test
- First-Order Differencing
- Seasonal Differencing
- ACF and PACF Analysis
- Initial SARIMA Model Development
- Hyperparameter Tuning
- Forecast Evaluation
- Future Passenger Forecasting

---

## Methodology

### 1. Data Preprocessing

- Loaded the Airline Passengers dataset.
- Converted the month column to datetime format.
- Set the month column as the time-series index.
- Checked for missing values and verified data quality.

### 2. Exploratory Data Analysis

The original time series revealed:

- A clear upward trend.
- Strong yearly seasonality.
- Increasing variance over time.

These observations indicated that the series was non-stationary.

---

### 3. Stationarity Testing

The Augmented Dickey-Fuller (ADF) test was used to determine stationarity.

The following transformations were applied:

- First-order differencing
- Seasonal differencing with a lag of 12

The transformed series achieved stationarity with a statistically significant ADF result.

---

### 4. SARIMA Model Development

The initial model selected was:

**SARIMA(1,1,1)(0,1,1,12)**

The model was evaluated on a holdout testing period.

---

### 5. Hyperparameter Tuning

Multiple SARIMA parameter combinations were evaluated.

The best-performing model was:

**SARIMA(1,1,2)(0,1,2,12)**

---

## Model Performance

### Initial Model

| Metric | Value |
|--------|------:|
| RMSE | 74.04 |

### Tuned Model

| Metric | Value |
|--------|------:|
| MAE | 38.31 |
| RMSE | 41.92 |
| R² Score | 0.6850 |

The tuned model substantially improved forecasting accuracy while preserving the long-term trend and yearly seasonal patterns.

---

## Future Forecast

The final tuned SARIMA model was trained using the complete historical dataset and used to forecast passenger demand for the next 12 months.

The forecasts indicate:

- Continued long-term growth in passenger demand.
- Strong yearly seasonal behavior.
- Highest passenger demand during the middle of the year.
- Lower passenger demand during the beginning and end of the year.

---

## Repository Structure

```text
air-passenger-forecasting-sarima/
│
├── air_passenger_forecasting.ipynb
├── airline-passengers.csv
├── requirements.txt
└── README.md
```

---

## How to Run

1. Clone the repository.

```bash
git clone https://github.com/alkasingh26/air-passenger-forecasting-sarima.git
```

2. Navigate to the project directory.

```bash
cd air-passenger-forecasting-sarima
```

3. Install the required packages.

```bash
pip install -r requirements.txt
```

4. Launch Jupyter Notebook.

```bash
jupyter notebook
```

5. Open:

```text
air_passenger_forecasting.ipynb
```

6. Run all notebook cells sequentially.

---

## Key Learning Outcomes

This project demonstrates practical experience with:

- Time Series Analysis
- Stationarity Testing
- Seasonal Differencing
- SARIMA Model Development
- Hyperparameter Tuning
- Forecast Evaluation
- Future Time Series Forecasting
- Python Data Analysis Libraries

---

## Future Improvements

Potential improvements include:

- Automatic hyperparameter optimization using Grid Search.
- Comparison with Prophet and LSTM models.
- Cross-validation for time series forecasting.
- Deployment as an interactive forecasting web application.

---

## Author

**Alka Singh**

GitHub: https://github.com/alkasingh26
