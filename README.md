# Employee Attrition Prediction using Machine Learning

## 📌 Project Overview

This project focuses on building a supervised machine learning model to
predict **employee attrition** (whether an employee is likely to leave
an organization).\
Beyond predictive performance, the project emphasizes
**interpretability, fairness, and business relevance**, making it
suitable for real-world HR decision-making.

------------------------------------------------------------------------

## 🎯 Objective

-   Predict employee attrition (Yes/No)
-   Identify key factors influencing attrition
-   Build an interpretable and fair model for HR analytics
-   Minimize **false negatives** (employees who leave but are not
    identified)

------------------------------------------------------------------------

## 📊 Dataset

-   **IBM HR Analytics Employee Attrition Dataset** (Kaggle)
-   Contains demographic, job-related, compensation, and performance
    features
-   Target Variable: **Attrition**

------------------------------------------------------------------------

## 🔍 Exploratory Data Analysis (EDA)

Key insights from EDA: - Attrition rate is **imbalanced (\~15--20%)** -
Higher attrition observed among: - Employees working overtime - Lower
income groups - Sales and Human Resources roles - Employees with long
gaps since last promotion - Younger employees show higher attrition risk
compared to senior employees

Correlation analysis revealed that: - Monthly income is negatively
correlated with attrition - Job satisfaction and work-life balance
strongly influence retention

------------------------------------------------------------------------

## 🛠 Feature Engineering

The following transformations were applied: - Encoding categorical
variables using **One-Hot Encoding** - Scaling numerical features using
**StandardScaler** - Derived features: - **WorkLifeIndex** (Work-life
balance + overtime + travel) - **Promotion Gap** (years since last
promotion) - **Tenure bands** (short, medium, long)

These features improved both model performance and interpretability.

------------------------------------------------------------------------

## 🤖 Models Trained

-   Logistic Regression (Primary Model)
-   Decision Tree
-   Random Forest

Class imbalance was handled using: - `class_weight='balanced'` -
Recall-focused evaluation metrics

------------------------------------------------------------------------

## 📈 Model Evaluation

Evaluation focused on metrics suitable for imbalanced data:

-   **Recall (Attrition)** -- primary metric
-   Precision, F1-score
-   ROC-AUC
-   Precision--Recall AUC
-   Cost-sensitive evaluation (False Negatives \> False Positives)

### ✅ Best Model

**Logistic Regression** was selected due to: - Higher recall for
attrition - Competitive ROC-AUC (\~0.80) - Strong interpretability for
HR stakeholders

------------------------------------------------------------------------

## 🔎 Explainability (SHAP)

SHAP was used to explain model predictions: - Identified key drivers of
attrition: - Overtime - Monthly income - Years since last promotion -
Job role - Work-life balance - Enabled both global and individual-level
explanations

This helps HR teams understand *why* employees are flagged as high risk.

------------------------------------------------------------------------

## ⚖️ Fairness Analysis

Model predictions were analyzed across: - Gender - Age groups -
Departments

No severe bias was observed, but fairness monitoring is recommended
before deployment.

Suggested mitigation strategies: - Regular bias audits -
Human-in-the-loop decision review - Threshold adjustments if needed

------------------------------------------------------------------------
------------------------------------------------------------------------

## 🛠️ Detailed Report

- The detailed report is present in the file ml_attrition.pdf.

------------------------------------------------------------------------

## 📌 Key Takeaways

-   Employee attrition is driven by workload, compensation, and career
    stagnation
-   Recall-focused models are more suitable for HR use cases
-   Interpretability is as important as accuracy in people analytics
-   Logistic Regression provides the best balance of performance and
    transparency

------------------------------------------------------------------------

## 👤 Author

Developed by **Naik J**
