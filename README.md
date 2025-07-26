# 🛳️ Titanic ML Survival Prediction Project

This repository contains my machine learning solution for the Titanic survival prediction challenge. The goal of the project was to build an accurate classifier to predict which passengers survived the Titanic disaster based on features like age, sex, ticket class, etc.

## 🚀 Tools & Libraries Used

- **AutoGluon**: For automated machine learning model training and ensemble selection
- **Optuna**: For hyperparameter optimization
- **Google Colab**: For model development and training
- **Pandas / Numpy / Sklearn**: For data manipulation and preprocessing

---

## 🧠 Project Overview

This project applies **AutoGluon TabularPredictor**, a powerful AutoML library developed by AWS, to automatically test and stack multiple model types (like LightGBM, CatBoost, Neural Networks, etc.) on the Titanic dataset.

I then used **Optuna**, a state-of-the-art hyperparameter optimization library, to fine-tune key AutoGluon hyperparameters such as:
- `ag_args_fit`
- `presets`
- `time_limit`
- `eval_metric`

This helped to systematically explore better configurations and boost prediction accuracy.

---

## ⚙️ Key Steps

1. **Data Preprocessing**
   - Cleaned and encoded missing values (e.g., `Age`, `Cabin`, `Embarked`)
   - Dropped or filled irrelevant features
2. **AutoML Training with AutoGluon**
   - Trained a model using `TabularPredictor`
   - Explored leaderboard of models with cross-validation and bagging
   - **Automatically created an ensemble of high-performing models** to boost accuracy
3. **Hyperparameter Optimization with Optuna**
   - Used `optuna.create_study` to explore high-performing configurations
   - Automatically selected the best set of hyperparameters for final training
4. **Prediction and Submission**
   - Made predictions on the Kaggle test set
   - Exported predictions to a submission-ready CSV

---

## 🗃️ Files Included

- `titanic_notebook.ipynb`: Core notebook with preprocessing, training, and optimization
- `AutogluonModels.zip`: Zipped AutoGluon model directory (optional, large file)
- `submission.csv`: Final CSV for Kaggle submission
- `titanic_opt.db`: Optuna study file storing best hyperparameter trials
- `README.md`: Project overview and instructions

---

## 🏁 Future Work

- Integrate **K-Fold cross-validation** to improve model robustness
- Automate additional feature engineering pipelines
- Deploy model as an interactive web app

---

## 🔖 Author

Izziemirg — Graduate Student in Business Analytics  
GitHub: [github.com/Izziemirg](https://github.com/Izziemirg)

---
