# Credit Risk Prediction – Home Credit Application Data

## Overview
This project focuses on building an interpretable credit risk model to support loan approval decisions. Using real-world loan application data from Home Credit, the objective is to predict whether an applicant is likely to default, based only on information available at the time of application.

The project follows a structured data science workflow, from data exploration and preprocessing to model training, evaluation, and explainability.

---

## Business Problem
Financial institutions must assess the risk of loan applicants before granting credit. Approving high-risk applicants can lead to financial losses, while rejecting low-risk applicants can reduce potential revenue.

This project aims to support credit decision-making by estimating default risk and identifying the key factors that influence loan repayment behavior.

---

## Dataset
- **Source:** Home Credit Default Risk (Kaggle)
- **Data used:** `application_train.csv`
- Each row represents a loan application
- Target variable:
  - `0` – Loan repaid
  - `1` – Loan defaulted

Only application-time information is used to avoid data leakage.

---

## Methodology
The project follows these steps:

1. Data understanding and exploratory data analysis (EDA)
2. Data preprocessing and handling of missing values
3. Feature engineering with a focus on affordability ratios
4. Baseline modeling using Logistic Regression
5. Advanced modeling using Random Forest for comparison
6. Model evaluation using risk-aware metrics
7. Model explainability and interpretation of risk drivers

---

## Models Used
- **Logistic Regression**
  - Chosen as a baseline due to its interpretability and common use in credit risk modeling
- **Random Forest**
  - Used to capture non-linear relationships and feature interactions

---

## Evaluation Metrics
Due to class imbalance and the high cost of misclassifying defaulters, model performance is evaluated using:
- ROC-AUC
- Precision and Recall
- Confusion Matrix

Recall for defaulters is prioritised to reduce the risk of approving high-risk applicants.

---

## Key Insights
- Affordability-related features (credit-to-income and annuity-to-income ratios) are strong drivers of default risk
- Indicators of financial stability, such as asset ownership, are associated with lower default risk
- More complex models can improve performance, but interpretability remains a key consideration in financial applications

---

## Limitations
- Only application-level data was used
- No historical payment or transaction data
- Macroeconomic factors were not included
- The model supports decisions but does not replace human judgment

---

## Next Steps
- Incorporate additional Home Credit tables (e.g. bureau data)
- Explore threshold optimisation based on business costs
- Apply explainability techniques such as SHAP for individual-level explanations

---

## Data Access

The dataset used in this project is not included in the repository due to size and licensing restrictions.

To run the notebook locally:

1. Visit the Home Credit Default Risk dataset on Kaggle:  
   https://www.kaggle.com/c/home-credit-default-risk/data

2. Download the file:
   - `application_train.csv`

3. Create a folder named `data` in the project root directory.

4. Place the downloaded file inside the `data` folder:

## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook
