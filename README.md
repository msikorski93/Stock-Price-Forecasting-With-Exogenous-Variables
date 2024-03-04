# Stock-Price-Forecasting-With-Exogenous-Variables
Time series forecasting (close prices) with different estimators. This project focused on adding exogenous fetures to the predicting models. The stock price data was collected and loaded via `yfinance` API. The idea behind was to enrich the dataset and improve the model learning. With proper feature selection we achived accurate price estimations with the following evaluation metrics:

| Model                | RMSE    | 6-Fold Cross-<br>Validation | R<sup>2 | MAE     | MAPE [%] |
|----------------------|---------|-----------------------------|---------|---------|----------|
| SARIMAX              | 7.9388  | 2.6185                      | 0.9993  | 5.7220  | 0.0052   |
| RNN                  | 81.5023 | 0.0226                      | 0.9257  | 64.9433 | 0.0556   |
| LSTM                 | 19.4527 | 0.0071                      | 0.9959  | 16.1197 | 0.0147   |
| Prophet              | 8.0641  | 1.8883                      | 0.9993  | 5.8148  | 0.0052   |
| Linear<br>Regression | 7.9390  | 1.0217                      | 0.9993  | 5.7226  | 0.0052   |
| SVR                  | 44.1079 | 0.0571                      | 0.9789  | 42.5849 | 0.0419   |
| XGBoosting           | 20.8949 | 0.0533                      | 0.9953  | 14.7921 | 0.0127   |

Among the chosen regressors the linear regression outperformed all the other estimators. Although the SARIMAX model had practically the same performance and is much more widely applied among the data science community, the linear regressor is much easier to develop and understand. Its high performance proves that our engineered variables are linearly correlated with the target feature. Adding extra variables is very beneficial. Not only does this enrich the dataset, but also provides more information and therefore improves regression performance.
