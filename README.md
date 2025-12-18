# Stock Price Prediction using ARIMA
This project demonstrates a time-series forecasting pipeline designed to predict stock market trends. Specifically, it utilizes historical data for Reliance Industries (RELIANCE.NS) to train an ARIMA (AutoRegressive Integrated Moving Average) model and forecast future closing prices.

## 🚀 Project Overview
The notebook covers the end-to-end process of financial time-series analysis:

1.Real-Time Data Acquisition: Using the yfinance library to download historical stock data directly from Yahoo Finance.
2.Data Preprocessing: Extracting and cleaning "Close" prices for consistent time-series modeling.
3.Model Training: Implementing an ARIMA(5, 1, 0) model to capture the underlying patterns in stock price fluctuations.
4.Performance Evaluation: Measuring model accuracy using Mean Squared Error (MSE).
5.Visualization: Generating comprehensive plots to compare actual stock prices against the model's predicted values.

## 🛠️ Technical Stack
The project is built using the following Python libraries:
1.yfinance: For fetching market data.
2.pandas & numpy: For data manipulation and array processing.
3.statsmodels: For the ARIMA implementation and statistical analysis.
4.matplotlib: For creating visual price charts.
5.scikit-learn: For calculating evaluation metrics like MSE.

📊 Methodology
> Data Source: Historical data for RELIANCE.NS from 2020-01-01 to 2023-01-01.
> Train-Test Split: The dataset is divided into training and testing sets to validate the model's predictive power on unseen data.
> Forecasting: The ARIMA model is trained on the initial segment and then "forecasts" the subsequent steps corresponding to the test period.

📈 Results
The model produces a visual representation of the stock's trajectory, identifying how closely the predicted red line (forecast) tracks the actual blue line (market price). The Mean Squared Error (MSE) is used as the primary metric to quantify the variance between predicted and actual values.

📂 File Structure
> predictive.ipynb: The primary Jupyter Notebook containing the code, data fetching logic, and analysis.

🚀 How to Use
1.Clone the Repository:
Bash

git clone https://github.com/yourusername/stock-prediction-arima.git

2.Install Dependencies:
Bash

pip install yfinance pandas statsmodels matplotlib scikit-learn

3.Run the Analysis: Open the notebook in Jupyter or Colab and execute the cells to see the real-time data fetch and prediction results.
