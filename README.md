# Stpwise_regression_TF

This script demonstrates how to perform stepwise regression using Scikit-learn and statsmodels libraries. Stepwise regression is a technique used to select the most important features in a dataset by iteratively adding or removing features based on their contribution to the model's performance. It aims to create a simpler, more interpretable model with better performance. The script also visualizes the results using matplotlib and seaborn.

Dependencies

pandas

numpy

matplotlib

seaborn

scikit-learn

statsmodels

Stepwise Regression Overview

Stepwise regression consists of two main techniques: forward selection and backward elimination. The algorithm starts with an empty model and proceeds in the following manner:

Forward Selection: At each step, the algorithm adds the feature that most improves the model according to a pre-defined criterion, such as the lowest p-value or highest F-statistic.

Backward Elimination: At each step, the algorithm removes the least significant feature, i.e., the one with the highest p-value or lowest F-statistic, if it meets a pre-defined threshold.

The algorithm stops when no more features can be added or removed based on the pre-defined criteria.

Steps

Import necessary libraries: Import the required libraries for data manipulation, visualization, and regression modeling.

Generate random data: Generate a random dataset for regression with 1000 samples, 10 features, and a noise level of 0.1.

Split the data: Split the dataset into 80% training and 20% testing sets.

Define the stepwise selection function: Create a function that performs stepwise feature selection using forward selection and backward elimination based on p-value thresholds.

Perform stepwise selection: Apply the stepwise selection function on the training data to identify the most important features.

Train the final model: Train an Ordinary Least Squares (OLS) regression model on the training data using the selected features.

Evaluate the model: Evaluate the model's performance on the test data using mean squared error and R-squared metrics.

Visualize the correlation matrix: Plot the correlation matrix of the selected features using a colormap.

Usage

To run this script, make sure you have the required dependencies installed. Execute the script in a Python environment, and the output will display the stepwise feature selection process, the selected features, model performance metrics, and the correlation matrix of the selected features.

Theory

Stepwise regression is a variable selection technique used in multiple regression models to find the most relevant subset of predictor variables. It is an iterative process that involves forward selection and backward elimination of variables based on their statistical significance in the model. The primary goal is to improve model interpretability and performance by reducing multicollinearity and overfitting, which can occur when including too many variables in the model.

The significance of each variable is typically assessed using p-values, which measure the probability of observing the given data under the null hypothesis. A low p-value indicates that the variable is statistically significant and contributes to the model's predictive power. Conversely, a high p-value suggests that the variable is not significant and may not provide useful information for predicting the response variable.

In this script, the stepwise selection function uses p-value thresholds to determine whether to include or exclude a variable from the model. The forward selection process adds variables with p-values below a specified threshold (e.g., 0.01), while the backward elimination process removes variables with p-values above a different threshold (e.g., 0.05). The algorithm iteratively refines the model until no more variables can be added or removed based on these criteria.
