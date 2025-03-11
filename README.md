# Stock Price Prediction Using LSTM with Attention

## Overview

This project implements a deep learning model using Long Short-Term Memory (LSTM) with an Attention Mechanism to predict stock prices. The attention layer helps the model focus on relevant time steps, improving accuracy in forecasting stock movements.

## Dataset

This dataset includes the daily historical stock prices for Google (GOOGL) spanning from 2020 to 2025. It features essential financial metrics such as opening and closing prices, daily highs and lows, adjusted close prices, and trading volumes. The information offers valuable insights into the stock's performance over a five-year timeframe.

**Column Descriptions:**

**Price**: Date of the stock data (needs cleaning as the first two rows are headers).

**Adj Close**: Adjusted closing price, accounting for events like dividends and splits.

**Close**: Closing price of the stock at the end of the trading day.

**High**: Highest price of the stock during the trading day.

**Low**: Lowest price of the stock during the trading day.

**Open**: Opening price of the stock at the start of the trading day.

**Volume**: Number of shares traded during the day.

***Dataset sourced from Kaggle.***

## Model Architecture

🔹 Data Preprocessing

- Normalization using MinMaxScaler

- Splitting into training and testing datasets

- Creating sequences for time-series forecasting

🔹 LSTM with Attention Mechanism

- LSTM layers to capture temporal dependencies

- Attention layer to assign importance to key time steps

- Fully connected layers for final prediction

- Loss function: Mean Squared Error (MSE)

- Optimizer: Adam with learning rate scheduling

## Training & Evaluation

- Early Stopping and ReduceLROnPlateau to optimize training

- Performance metrics:

    - Train RMSE: 5.51
    - Test RMSE: 8.41
    - Test RMSE as % of mean price: 4.89%

- Visualization of actual vs. predicted stock prices using Matplotlib & Seaborn

## Dependencies

- Python
- TensorFlow, NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn

📌 Results

The model effectively captures stock price trends.

Attention mechanism enhances feature importance, leading to better predictions.
