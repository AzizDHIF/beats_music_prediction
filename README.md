# beats_music_prediction
This is my work that i have done in  a kaggle competition  to predict the song's beats-per-minute.
Song BPM Prediction – Kaggle Competition

This repository contains my solution for a Kaggle competition on predicting Beats Per Minute (BPM) of songs using feature engineering and an ensemble stacking model.

Overview

The goal of this competition is to predict the BPM (beats per minute) of songs based on audio and metadata features. Accurate BPM prediction is crucial for applications like:

DJ software and music mixing

Music recommendation systems

Fitness / rhythm-based applications

Approach
1. Data Preprocessing

Missing values handled with imputation

Outlier detection and scaling (RobustScaler)

Feature selection to reduce noise

2. Feature Engineering

Extracted interaction terms between rhythm and frequency features

Created statistical aggregations (mean, variance, skewness)

Normalized continuous variables

Encoded categorical features with target and frequency encodings

3. Models Used

Base learners for stacking:

LightGBM (gradient boosting)

XGBoost

RandomForest

Meta-model (stacking layer):

Ridge Regression for stable blending

4. Training Setup

5-Fold Cross Validation for robust RMSE estimation

Hyperparameter tuning using Optuna / GridSearch

Stacking implemented via sklearn.ensemble.StackingRegressor

5. Evaluation

Metric: Root Mean Squared Error (RMSE)

Achieved strong performance compared to baseline models
