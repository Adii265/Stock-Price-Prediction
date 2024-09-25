# Stock Price Prediction


****Overview****

This project involves analyzing time series data using Long Short-Term Memory (LSTM) models. The goal is to evaluate different configurations of LSTM models to forecast time series data accurately. The analysis includes experimenting with seasonality, lookback periods, and threshold settings to determine their impact on model performance.

****Key Components****

**1. Data Preparation**
a. Time series data (df_close_series) is preprocessed and scaled using MinMaxScaler.
b. Seasonal decomposition is performed to extract seasonal, trend, and residual components.
c. Stationarity is check using Dicky-Fller Test.

**2. Models Evaluated**
a. LSTM without Seasonality:
Lookback = 1, Threshold = 0
Lookback = 4, Threshold = 7
b. LSTM with Seasonality:
Lookback = 1, Threshold = 7
Lookback = 4, Threshold = 7

**3. Performance Metrics**
Mean Absolute Error (MAE) is calculated for both training and testing datasets.


****Results:****

![image](https://github.com/user-attachments/assets/4420a9b1-873c-4029-889d-2305bc453702)

1. LSTM with No Seasonality, Lookback = 1, Threshold = 0:
Best performance with the lowest MAE on both training and test data.
Suitable for capturing short-term dependencies with minimal complexity.

2. LSTM with No Seasonality, Lookback = 4, Threshold = 7:
Increased MAE compared to Lookback = 1, indicating underfitting with longer history.
Struggles to generalize well with additional past data points.

3. LSTM with Seasonality, Lookback = 1, Threshold = 7:
Significantly higher MAE, indicating that adding seasonality introduces complexity that the model struggles to capture effectively with a short lookback.
Shows signs of overfitting.

4. LSTM with Seasonality, Lookback = 4, Threshold = 7:
Improved generalization compared to no seasonality, with close train and test errors.
Balances short-term and seasonal patterns well, but overall higher MAE than the simplest model.

****Files****

Amazon.csv - Dataset of Amazon stocks


****Contact****

For questions or suggestions, please contact [Your Name] at [Your Email].

