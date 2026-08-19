# Stock Price Prediction

Machine learning project focused on predicting the next day's stock closing price using regression models and different data-splitting strategies.

## Overview

This project uses historical stock price data to predict the next day's closing price. The analysis compares Linear Regression and Random Forest models while examining how preprocessing, feature engineering, and train-test splitting affect model performance.

## Approach

- Converted and sorted date-time data
- Removed non-trading days and checked for time gaps
- Created `NextDayClose` as the prediction target
- Performed feature engineering and scaling
- Compared different train-test split strategies:
  - Random split with shuffling
  - Random split without shuffling
  - Date-based cutoff
  - Time-aware 80/20 split

## Models

- Linear Regression
- Random Forest Regressor
- Naive baseline

## Evaluation Metrics

- MAE
- RMSE
- R²
- MAPE

## Key Findings

- Linear Regression performed strongly across multiple experiments.
- A shuffled split produced very high R² values, but performance changed substantially with time-aware evaluation.
- Random Forest was competitive with shuffled data but became unstable with unshuffled and time-aware splits.
- Using only the Close feature performed better than adding several engineered features in the time-aware experiment.
- The results highlight the importance of using appropriate validation strategies for time-dependent data.

## Visualizations

The project includes:

- Stock closing-price trends over time
- Actual vs predicted values
- Residual analysis
- Correlation heatmap
- Model performance comparisons
- Linear Regression coefficient comparisons

## Technologies

Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
