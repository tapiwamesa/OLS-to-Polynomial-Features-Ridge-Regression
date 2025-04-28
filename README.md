# OLS-to-Polynomial-Features-Ridge-Regression | California Housing Price Prediction

## Project Overview

This project aims to predict median house values in California using socio-economic and geographic features from the **California Housing dataset** (U.S. Census Bureau). The dataset includes attributes like median income, average number of rooms, population, and house age, aggregated at the block group level.

The challenge is to accurately model the relationship between these features and housing prices, which may involve both linear and nonlinear interactions.

## Problem Statement

Traditional linear modeling methods such as Ordinary Least Squares (OLS) provided a good starting point but showed limited predictive power. Therefore, the project explores more advanced techniques like Ridge Regression and polynomial feature transformations to enhance prediction accuracy and model generalization.

## Objectives

- Build a baseline model using **Ordinary Least Squares (OLS)** regression and evaluate its performance.
- Apply **Ridge Regression** to address potential overfitting and improve the model's robustness.
- Introduce **Polynomial Features** to capture non-linear relationships between features.
- Compare all models based on **R² scores** for both training and test datasets.
- Recommend the most effective modeling approach for this problem.

## Model Comparisons and Key Findings

- **OLS Regression** (with feature engineering):  
  - Feature engineering was attempted by creating derived features from existing ones.
  - This only marginally improved the model's R² score from **60.1% to 61%** on training data.
  - On unseen data, the model stagnated at **59.7%**, indicating poor generalization.

- **Ridge Regression**:
  - Introducing Ridge regularization **did not improve** model performance compared to OLS.
  - In fact, Ridge performed slightly worse than OLS with feature engineering.

- **Ridge Regression with Polynomial Features** (degree = 2):
  - Significantly improved model performance.
  - Achieved a training R² score of **68%** and a test/generalization R² score of **65%**.
  - Successfully captured nonlinear relationships in the data that simpler models missed.

## Conclusion

Comparing OLS, Ridge Regression, and Ridge Regression with Polynomial Features demonstrated that **model complexity can be beneficial** when appropriate for the data. The relationship between features and the target is crucial in selecting a modeling strategy. 

In this case, Ridge Regression with polynomial features proved to be the most optimal approach, outperforming simpler linear models. Future work could explore **ensemble methods** (such as Random Forests or Gradient Boosting) to potentially achieve even better performance.

## Technologies Used

- Python
- Scikit-learn
- Pandas
- NumPy
- Matplotlib and Seaborn (for visualization)
