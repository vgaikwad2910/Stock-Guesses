# Stock-Guesses
Creating a repo for all my stock price guesses and practice models
Google Stock Forecasting: Multivariate LSTM vs. ProphetA comparative study of deep learning and statistical time-series analysis for one-step-ahead price prediction.
Overview: This project evaluates the predictive power of Long Short-Term Memory (LSTM) neural networks against Facebook's Prophet model. By integrating multivariate technical indicators, the project explores how deep learning captures local momentum shifts that traditional statistical models might overlook. 
Technical 
StackLanguage: Python 3.12
Deep Learning: TensorFlow/Keras (Stacked LSTM Architecture)
Statistical Modeling: Facebook Prophet
Feature Engineering: pandas-ta (RSI, MACD, SMA)
Data Source: yfinance (5 years of $GOOGL$ history)

Key Insight: One-Step vs. Recursive Forecasting
Initially, a 7-day recursive forecast was attempted, resulting in a "Recursive Spiral of Doom." This project highlights a critical senior-level takeaway:

The Problem: Recursive forecasting compounds small errors, leading to "hallucinated" price drops.

The Solution: We shifted to One-Day Ahead Forecasting, ensuring every prediction is grounded in 100% real historical data to maintain a robust 2.14% MAPE.

📊 Results
The models were backtested on a 45-day unseen validation set to ensure statistical significance.

LSTM Backtest MAPE: 2.1% (Superior at catching volatility)

Prophet Backtest MAPE: 6.5% (Strong at identifying long-term seasonal trends)
 
