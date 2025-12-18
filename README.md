#📈 Financial Time Series Forecasting: Stock Price Prediction using ARIMA

This project focuses on predicting future stock prices by analyzing historical market data. Using the ARIMA statistical model, this analysis demonstrates how to handle non-stationary data, identify seasonal trends, and forecast financial metrics with measurable confidence.

## 🎯 Project Objective

The goal is to provide a quantitative framework for financial forecasting by:

    Extracting historical stock data (e.g., Apple, Google, or Tesla) using financial APIs.

    Evaluating Stationarity using the Augmented Dickey-Fuller (ADF) test.

    Optimizing Parameters (p,d,q) for the ARIMA model using ACF and PACF plots.

    Forecasting future closing prices and validating results against actual market movements.

## 🛠️ Tech Stack & Skills

    Language: Python 3.x

    Time Series Analysis: statsmodels (ARIMA, SARIMA, Seasonal Decomposition)

    Statistical Testing: Augmented Dickey-Fuller (ADF) Test

    Data Handling: Pandas, NumPy, yfinance (Yahoo Finance API)

    Visualization: Matplotlib, Seaborn (for trend and residual analysis)

    Evaluation: RMSE (Root Mean Squared Error), MAE (Mean Absolute Error), AIC/BIC Scores

## 📉 Project Workflow
### 1. Data Acquisition & Preprocessing

    Retrieved historical daily closing prices using the yfinance library.

    Handled missing dates and adjusted for stock splits/dividends.

    Visualized Trends: Identified upward/downward trends and potential seasonality.

### 2. Making the Data Stationary

ARIMA requires stationary data (constant mean and variance).

    ADF Test: Performed a statistical test to check for stationarity.

    Differencing (d): Applied first-order or second-order differencing to remove trends and stabilize the mean.

### 3. Model Identification (p,q Selection)

    Used Autocorrelation Function (ACF) plots to determine the Moving Average (q) term.

    Used Partial Autocorrelation Function (PACF) plots to determine the AutoRegressive (p) term.

### 4. Training and Forecasting

    Split the data into a training set (80%) and a testing set (20%) using a time-ordered split (no shuffling).

    Fitted the ARIMA(p, d, q) model.

    Generated a Forecast vs. Actual plot to visualize model accuracy.

## 📊 Evaluation Results

The model's performance was measured using standard time-series metrics:

    AIC (Akaike Information Criterion): Used to select the most parsimonious model.

    RMSE: [Insert Value, e.g., 2.45] — Indicates the average deviation of the forecast from actual prices.

    Mean Absolute Percentage Error (MAPE): [Insert Value, e.g., 1.5%] — Demonstrates the relative accuracy of the model.

## 📂 Repository Structure
├── data/                   # Historical CSV files (if not using API)
├── notebooks/              # Step-by-step ARIMA analysis & parameter tuning
├── src/                    # Python scripts for data fetching and testing
├── README.md               # Project documentation
└── requirements.txt        # List of dependencies (statsmodels, pandas, etc.)
