# 🧠 Personality Classification: Introvert vs Extrovert

This project focuses on building a machine learning model to classify whether a person is an **Introvert** or **Extrovert** based on behavioral and demographic features.

## 🎯 Project Goal

The objective is to:
- Analyze patterns in the behavioral data of individuals.
- Build and evaluate various classification models to distinguish between Introverts and Extroverts.
- Select the best-performing model based on F1-score and generalization ability.

## 📊 Dataset Overview

- **Source**: [Kaggle - Extrovert vs Introvert Behavior Data](https://www.kaggle.com/datasets/rakeshkapilavai/extrovert-vs-introvert-behavior-data)
- The dataset contains information such as:
  - Decision-making behavior
  - Communication style
  - Social comfort
  - Demographic indicators
  - Personality label: `Introvert` or `Extrovert`

Target variable (`Personality`) was encoded as:
- `1`: Introvert  
- `0`: Extrovert

## 🔍 Exploratory Data Analysis (EDA)

The following steps were taken:
- Checked for missing values and distribution of features.
- Visualized class balance (Introvert vs Extrovert).
- Plotted feature distributions and correlation heatmap for numerical features.

## ⚙️ Modeling Approach

### Preprocessing:
- Numerical features: Missing values imputed with median, then scaled with `StandardScaler`.
- Categorical features: Missing values imputed with mode, then encoded using `OneHotEncoder`.
- Pipelines were built using `ColumnTransformer` and `Pipeline` for clean and modular workflow.

### Models Trained:
- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree
- XGBoost

Cross-validation (5-fold Stratified K-Fold) was used to compare models based on **F1-score**.

## ✅ Final Model Performance

The **SVM model** was selected as the best model based on cross-validation and test results.

### Test Set Results:
- **Accuracy**: 92%
- **F1-score** (Introvert): 0.92
- **F1-score** (Extrovert): 0.92

### Confusion Matrix:
