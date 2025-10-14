# Tutors Lessons Prices Prediction

<img width="1140" height="511" alt="изображение" src="https://github.com/user-attachments/assets/20a9d45c-4d27-4b59-a096-81a1e432348a" />

This repository contains a solution for the Kaggle competition [Tutors Lessons Prices Prediction](https://www.kaggle.com/competitions/tutors-lessons-prices-prediction), where the task is to predict the average hourly price of tutors based on their profile features.

## Overview

- **Task**: Regression — predicting mean hourly price of tutors.  
- **Input**: Tutor profiles with categorical and numerical features.  
- **Datasets**:
  - **Train**: Tutor profiles with `mean_price` as the target.  
  - **Test**: Tutor profiles without `mean_price`.  
- **Evaluation Metric**: RMSE (Root Mean Squared Error).

## Solution

- **Model**: **CatBoostRegressor** (gradient boosting on decision trees).  
- **Training setup**:
  - Categorical features encoded using one-hot and multi-hot encoding.  
  - Numerical features standardised and missing values imputed.  
  - Model trained with 2000 iterations, learning rate 0.05, depth 6, and RMSE as eval metric.  
- **Validation**: Train/test split and 5-fold cross-validation.  
- **Metrics**: MAE, MSE, R2 score.  
- **Results**:  
  - Test score on Kaggle: **68.5 RMSE**.  

### Repository structure
- **tutors.ipynb** – Jupyter Notebook with full data preprocessing, feature engineering, model training, evaluation, and test predictions.  
- **[submission.csv](https://mega.nz/file/XupWXALZ#KSAT8vv5vZOL57kL_y-t55Vln9QYCe4X8PrvFlP7AoU)** – Predicted `mean_price` for the test set.
