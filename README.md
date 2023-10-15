# Case-Shiller Index Analysis

## Introduction

This analysis aims to examine the Case-Shiller Index, a widely used indicator of U.S. housing market performance. We will explore the factors affecting the Case-Shiller Index and develop regression models to predict its values. The analysis will include data collection, preprocessing, and evaluation of various regression models.

## Data Collection and Preprocessing

### Data Sources

We gathered data from multiple sources:
- Case-Shiller Home Price Index
- Working Population Statistics
- Construction Material Prices
- Consumer Price Index (CPI)
- Unemployment Rate
- Federal Funds Rate
- Income Data
- Number of Households
- Housing Subsidy Data
- Percentage of Older Population

### Data Preprocessing

The data preprocessing steps included handling missing values, converting date columns, and merging various datasets to create a consolidated dataset for analysis. Additionally, we performed linear interpolation to fill missing values and filtered the data for analysis from 2003 to 2023.

## Exploratory Data Analysis

We conducted exploratory data analysis to understand the relationships and correlations between variables. Key findings include:
- Strong positive correlations between Per Capita GDP, CPI, and Num Households.
- Working Population is negatively correlated with the Federal Funds Rate.
- The Consumer Price Index (CPI) strongly correlates with economic factors.
- Num Households, Subsidy, and Old Percentage are strongly correlated.

## Regression Models

We evaluated several regression models to predict the Case-Shiller Index:

### Linear Regression

Linear regression fits a linear model to the data and is used to understand the relationship between independent and dependent variables.

### K Nearest Neighbors (KNN)

KNN is a technique that finds the K-nearest training examples to a new data point and predicts the output based on these neighbors.

### Support Vector Regression (SVR)

SVR is a method to predict a continuous variable by finding the best-fitting linear regression model within a certain margin of error.

### Decision Trees

Decision trees use a tree-like graph of decisions to make predictions and are useful for non-linear relationships in data.

### XGBoost Regressor

XGBoost is a robust regression algorithm known for its predictive accuracy and customizable loss functions.

### Random Forest Regressor

Random Forest is an ensemble method that combines multiple decision trees to reduce variance and improve prediction accuracy.

### LightGBM Regressor

LightGBM is an efficient gradient-based learning algorithm ideal for regression tasks.

## Model Comparison and Evaluation

We compared the performance of the models using metrics such as Mean Absolute Error (MAE), Root Mean Square Error (RMSE), and R^2 scores on the test data. The following is the comparative analysis:

- Decision Tree (DT) and XGBoost (XGB) have the lowest RMSE on the test data, indicating superior predictive accuracy.
- K-Nearest Neighbors (KNN) also performs well with a low RMSE and a high R^2 score.
- Linear Regression and Ridge have similar performance with slightly higher RMSE values.
- Random Forest (RF) and LightGBM Regressor perform well with lower RMSE and higher R^2 compared to linear models.
- Support Vector Regressor (SVR) has the highest RMSE and the lowest R^2, indicating lower predictive power.

## Feature Importance

Feature importance analysis reveals that "Per Capita GDP" is the most influential feature in predicting the Case-Shiller Index for both the XGBoost and Random Forest models.

## Conclusion

In conclusion, the Random Forest and XGBoost models are the top performers in predicting the Case-Shiller Index. These models provide the lowest MAE on the test data. Feature importance analysis highlights the significance of economic factors, with "Per Capita GDP" being the most influential. The analysis demonstrates the potential to predict housing market performance and provides valuable insights for real estate market analysis.

## References

- Data sources: [List data sources here]
- Scikit-Learn documentation: [Scikit-Learn](https://scikit-learn.org/stable/index.html)
- XGBoost documentation: [XGBoost](https://xgboost.readthedocs.io/en/latest/)
- Random Forest documentation: [Random Forest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)
- LightGBM documentation: [LightGBM](https://lightgbm.readthedocs.io/en/latest/)
- Case-Shiller Index information: [S&P Dow Jones Indices](https://www.spglobal.com/spdji/en/)
