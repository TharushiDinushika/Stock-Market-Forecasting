# Stock-Market-Forecasting
This project aims to create a machine learning model that predicts stock market trends, specifically focusing on predicting the target value for the next day. The goal is to help decide whether a particular company’s stock is suitable for buying or selling based on its predicted behavior. The model uses historical stock data to make these predictions and applies advanced techniques to make the process more accurate and efficient.

# Used Framework
## LightGBM - Light Gradient-Boosting Machine
LightGBM is a free and open-source distributed gradient-boosting framework for machine learning, originally developed by Microsoft. It is based on decision tree algorithms and used for ranking, classification and other machine learning tasks.

Why LightGBM?

It efficiently handles large datasets without excessive memory usage.

It captures complex feature interactions.

It handles categorical variables effectively.

# Dataset
[JPX Tokyo Stock Exchange Dataset](https://www.kaggle.com/competitions/jpx-tokyo-stock-exchange-prediction/data)

# Feature Engineering

## 1. Price Adjustment Features
   
  AdjustedClose:
  Represents the adjusted closing price of the stock, accounting for corporate actions like splits and dividends, ensuring consistency over time.

## 2. Time-Based Features
   
  Day, Month, Year:
  The day, month, and year extracted from the date.

## 3. Lag Features
   
  Provides information on immediate historical performance.

  Lag_Close_1:
  The closing price of the stock on the previous trading day.
  
  Lag_Close_5:
  The closing price of the stock five trading days ago.
  
  Lag_Volume_1:
  The trading volume on the previous trading day.

## 4. Rolling Statistics
   
  Provide a dynamic view of trends and patterns over a defined period.

   Volatility_30Day:
     Rolling 30-day standard deviation of log returns of the adjusted close price.
   
   MovingAvg_20Day:
     Rolling 20-day mean of the adjusted close price.

## 5. Technical Indicator
   
  ATR (Average True Range):
  Measures the average range (high-low differences) over the last 5 days, incorporating gaps from the previous close.


