# 🛡️ NovaPay Fraud Detection System

## 📌 Project Overview
This project focuses on building an automated Machine Learning system to detect fraudulent digital money transfers for NovaPay. The primary business goal was to maximize fraud detection (Recall) while maintaining **zero customer friction** (100% Precision), ensuring no legitimate users have their accounts wrongfully locked.

## 🚀 Key Features & Methodologies
* **Feature Engineering:** Created custom behavioral metrics, including `velocity_burst` (tracking high-frequency transactions) and `account_very_new`, which proved to be the strongest predictors of fraud.
* **Model Selection:** Evaluated Logistic Regression, LightGBM, XGBoost, and Random Forest.
* **Hyperparameter Tuning:** Optimized a Random Forest Classifier using `RandomizedSearchCV` to achieve peak performance.
* **Explainable AI (XAI):** Integrated **SHAP (SHapley Additive exPlanations)** to break the "black box" and provide operations teams with human-readable explanations (Risk & Protective factors) for every flagged transaction.

## 📊 Business Impact & Results
The tuned Random Forest model achieved exceptional results on unseen test data:
* **Precision:** 100% (Only 1 false positive out of ~2,000 legitimate transactions).
* **Recall:** 92% (Successfully caught 283 out of 309 fraud attempts).
* **ROC-AUC:** 0.97

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, SHAP, Matplotlib, Joblib
* **Deployment Readiness:** Model and explainer pipelines exported via `joblib` for easy API integration.

## 📂 Files in this Repository
* `NovaPay_Fraud_Detection_Final.ipynb`: The complete master notebook containing EDA, training, and SHAP analysis.
* `NovaPay_Fraud_Presentation.pdf`: Stakeholder slide deck summarizing business insights.
