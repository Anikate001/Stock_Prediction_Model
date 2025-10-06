Stock Price Prediction Using Walk-Forward Ridge Regression



This project demonstrates a robust machine learning workflow for time series stock price prediction using historical closing prices.
It features a Ridge Regression model with walk-forward validation, clever feature engineering, and techniques to avoid overfitting.

How It Works
Dataset: Loads any stock CSV from a folder of historical NASDAQ/ETF prices (Kaggle or Yahoo Finance).

Feature Engineering: Automatically creates lagged features from previous closing prices (adjustable look-back window).

Walk-Forward Validation: Splits the time series chronologically—training always on past, testing on future—avoiding information leakage.

Model Choice: Uses Ridge Regression for regularization, tackling overfitting compared to tree-based models.

Intelligent Tricks:

Avoids random splits (leads to data leakage in time series).

Visualizes train/test prediction curves for overfit diagnosis.

Separately reports train and test errors.

Visualization: Beautiful matplotlib plots compare real vs predicted prices for out-of-sample and in-sample periods.

Extensible: Easily swap to more features (volume, indicators) or advanced models (LSTM, XGBoost).

Notable Technical Choices
Walk-Forward Split: Only uses past data to predict the future, simulating real market scenarios instead of synthetic random splits.

Lag Features: Builds a sliding window feature set, capturing price movement patterns (with user-controllable depth).

Regularization: Ridge regression prevents numerical overfitting.

Clear Metric Reporting: Shows train/test MSE and MAE for honest assessment.

Example Results
Train MSE: As low as possible without overfitting.

Test MSE: Significantly better generalization than random forest or shuffled splits.

![Actual vs Predicted Closing Prices](

How to Use
Put your stock CSV data in the target folder.

Run each cell in the notebook in order:

Import packages

Load and clean the data

Make lagged features

Chronologically split train/test

Train and evaluate the Ridge model

Visualize and interpret results

Swap in other stocks, experiment with lag depth or regularization.

Extend with volume, technical indicators, or more models for better results.
