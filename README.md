# BostonDataPrediction

[![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)](https://www.python.org/)
![Static Badge](https://img.shields.io/badge/Scikit-%23F7931E?style=for-the-badge&logo=scikit-learn&logoColor=%23F7931E&color=blue)
![Static Badge](https://img.shields.io/badge/Scipy-%238CAAE6?style=for-the-badge&logo=scipy&logoColor=%238CAAE6&color=yellow)
[![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
![Static Badge](https://img.shields.io/badge/Numpy-%23013243?style=for-the-badge&logo=Numpy&logoColor=%23013243&color=blue)
![Static Badge](https://img.shields.io/badge/MySQL-%234479A1?style=for-the-badge&logo=MySQL&logoColor=%234479A1&color=black)
![Static Badge](https://img.shields.io/badge/Plotly-%233F4F75?style=for-the-badge&logo=Plotly&logoColor=%233F4F75&color=black)



## Project Overview

This project employs a regression analysis to predict house prices in Boston using historical housing data. It focuses on exploring relationships between various house features and their impact on pricing, with an aim to develop a predictive model that assists in making informed real estate decisions. The end goal is to understand key drivers of house prices in Boston and provide accurate price predictions using machine learning techniques.



![Logo](Logo1.png)


## Data Description

The dataset utilized in this project is the renowned "Boston Housing Dataset" from the sklearn library. It comprises various attributes of houses in Boston neighborhoods, such as average number of rooms per dwelling, property tax rate, pupil-teacher ratio by town, and percent of lower status population. These factors are crucial in determining the market value of the houses.


## Methodology

### Data Preprocessing
Initial steps involve loading and examining the data for null values, ensuring there is no missing data which might affect predictive accuracy. Descriptive statistics help summarize the dataset's central tendency, dispersion, and shape.

### Feature Selection
Using correlation analysis, significant predictors of house prices were identified. A heatmap visualizes these relationships, helping select features that contribute most to the model.

### Model Building
Model building in this project involves several key steps, each crucial to developing a reliable predictive model:

**Data Standardization**: Before model training, it's important to standardize the data. This means scaling the features so they have a mean of zero and a standard deviation of one. This process is crucial because it ensures that all features contribute equally to the model's predictions, preventing variables with larger scales from dominating. In your project, the StandardScaler from sklearn.preprocessing was used to standardize the training data. The same scaler was then applied to the test data to maintain consistency.

**Training the Linear Regression Model**: Linear regression was chosen due to its efficiency in predicting a continuous variable and ease of interpretation. The model attempts to fit a linear equation to observed data. In your project:

1: The LinearRegression class from sklearn.linear_model was used.

2: The model was trained using the fit() method, which computes the coefficients (parameters) of the features that minimize the least square error between predicted and actual values in the training set.

**Feature Selection**: The features included in the model were chosen based on their correlation with the target variable (PRICE). Features with strong correlations are typically good predictors. This decision is often guided by examining a correlation matrix and plotting data visualizations like scatter plots and heatmaps to understand relationships between variables.

### Model Evaluation
Several statistical metrics were used:

**Residual Analysis**: This involves examining the differences between the observed values of the target variable and the values predicted by the model (residuals). 

1: Residual plots and density plots were used to check for the randomness of residuals, which is crucial for confirming assumptions about the linear model.

2: Ideally, residuals should be randomly dispersed around the central line and not show any discernible pattern. This was visualized using a scatter plot of predicted values against residuals.

**Error Metrics**:

1: Mean Absolute Error (MAE): This is the average of the absolute differences between predicted and actual values. It gives an idea of how wrong the predictions were, in units of the target variable.

2: Mean Squared Error (MSE): This is the average of the squares of the differences between predicted and actual values. It penalizes larger errors more than smaller ones, which is useful when large errors are particularly undesirable.

3: Root Mean Squared Error (RMSE): This is the square root of the MSE and is in the same units as the target variable. It is particularly useful because it gives a relatively high weight to large errors.

**Coefficient of Determination (R² Score)**: This metric indicates the proportion of the variance in the dependent variable that is predictable from the independent variables. It is a measure of how well unseen samples are likely to be predicted by the model.

**Adjusted R²**: This version of the R² score adjusts for the number of predictors in the model and is more suitable when comparing models with a different number of independent variables.


## Findings & Evaluation

The regression model performed reasonably well, with a final R² score indicating a decent level of explanation for variance in housing prices. Visualization of residuals confirmed assumptions of normality and homoscedasticity, essential for valid linear regression inference. Key predictors identified include RM, LSTAT, PTRATIO, and TAX.


![Logo](Logo2.png)


## Conclusion

The Boston Housing Data Prediction project highlights the capabilities of linear regression in real estate price forecasting. Despite its simplicity, the model efficiently captures significant relationships between features and house prices. Future improvements could involve experimenting with more complex models like Random Forest or Gradient Boosting to potentially enhance prediction accuracy. Additionally, incorporating more recent data or considering external factors like economic conditions could further refine the model's effectiveness.