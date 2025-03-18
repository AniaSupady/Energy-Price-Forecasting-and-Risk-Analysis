# Energy-Price-Forecasting-and-Risk-Analysis
Energy Price Forecasting: Compares ARIMA, SARIMA, XGBoost, Random Forest, and ensemble models for predicting energy prices. Includes feature engineering, model evaluation, and risk assessment.



# Energy Price Forecasting Model Comparison

## Models Implemented

1. **ARIMA (AutoRegressive Integrated Moving Average)**
   - A classical time series forecasting method
   - Order: (1, 1, 1)

2. **SARIMA (Seasonal ARIMA)**
   - ARIMA with added seasonal component
   - Order: (1, 1, 1), Seasonal Order: (1, 1, 1, 12)

3. **XGBoost**
   - An advanced implementation of gradient boosting
   - Parameters: n_estimators=100, learning_rate=0.1

4. **Random Forest**
   - An ensemble learning method based on decision trees
   - Parameters: n_estimators=100

5. **Ensemble**
   - Simple average of XGBoost and Random Forest predictions

## Model Performance

| Model         | MAE    | RMSE   |
|---------------|--------|--------|
| ARIMA         | 2.27   | 2.86   |
| SARIMA        | 3.15   | 4.05   |
| XGBoost       | 0.93   | 1.18   |
| Random Forest | 0.83   | 1.04   |
| Ensemble      | 0.84   | 1.06   |

## Key Findings

1. Machine learning models (Random Forest and XGBoost) outperformed traditional time series models (ARIMA and SARIMA) for this dataset.
2. Random Forest showed the best performance with the lowest MAE (0.83) and RMSE (1.04).
3. The simple ensemble of XGBoost and Random Forest did not improve upon the individual model performances.
4. SARIMA performed worse than ARIMA, suggesting that the added seasonal component did not capture useful patterns in this data.

## Risk Metrics

- Price Volatility: 26.33% (annualized)
- 95% Value at Risk: -40.56%

These metrics indicate significant price fluctuations and potential for substantial downside risk in daily returns.

## Next Steps

1. Further tune hyperparameters of the best-performing models (Random Forest and XGBoost).
2. Explore more advanced ensemble techniques.
3. Investigate why traditional time series models underperformed and consider alternative specifications.
4. Conduct feature importance analysis to understand key drivers of price movements.
5. Implement rolling window analysis to assess model stability over time.
