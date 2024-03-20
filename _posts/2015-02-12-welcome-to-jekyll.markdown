---
layout: default
title: Linear Regression Documentation
---

# Linear Regression Documentation

## Introduction

Linear regression is a fundamental statistical technique used to model the relationship between a dependent variable and one or more independent variables. In this document, we'll discuss the basics of linear regression, its assumptions, implementation, and interpretation.

## Understanding Linear Regression

### What is Linear Regression?

Linear regression aims to find the best-fitting linear relationship between the independent variable(s) and the dependent variable. The equation of a simple linear regression model is:

$$
Y = \beta_0 + \beta_1X + \epsilon
$$

where:
- \(Y\) is the dependent variable.
- \(X\) is the independent variable.
- \(\beta_0\) is the intercept.
- \(\beta_1\) is the slope.
- \(\epsilon\) is the error term.

### Assumptions of Linear Regression

Linear regression relies on several assumptions:
1. Linearity: The relationship between the independent and dependent variables is linear.
2. Independence: The residuals (errors) are independent of each other.
3. Homoscedasticity: The variance of the residuals is constant across all levels of the independent variables.
4. Normality: The residuals follow a normal distribution.

## Implementation

### Simple Linear Regression

```python
# Python code example for simple linear regression
import numpy as np
from sklearn.linear_model import LinearRegression

# Sample data
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)
y = np.array([2, 3, 4, 5, 6])

# Create a linear regression model
model = LinearRegression()

# Fit the model
model.fit(X, y)

# Print the coefficients
print('Intercept:', model.intercept_)
print('Slope:', model.coef_)
