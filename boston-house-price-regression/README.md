# Boston House Price Regression

Linear regression on the Boston housing dataset to predict median home value (`MEDV`, modeled as `log(MEDV)`).

## Approach

1. Summary statistics, univariate and bivariate EDA, correlation heatmap
2. Train/test split and multicollinearity check with VIF (dropped `TAX`)
3. OLS model with statsmodels, then iterative removal of insignificant variables (p > 0.05)
4. Regression assumption checks: mean of residuals, homoscedasticity, linearity, normality of errors
5. Cross-validation and coefficient interpretation

## Results (from the notebook output)

| Metric | Value |
|---|---|
| Adjusted R² | 0.771 |
| Test RMSE (log scale) | 0.186 |
| Test MAPE | 4.90% |

Train and test errors are nearly identical (train RMSE 0.198), indicating no overfitting. `RM` (rooms per dwelling) and `LSTAT` (% lower-status population) were the strongest drivers of price.
