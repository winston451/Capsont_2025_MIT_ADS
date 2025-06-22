# Loan Default Prediction Model

![Python](https://img.shields.io/badge/Python-3.10-blue.svg) ![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3.2-orange.svg) ![Pandas](https://img.shields.io/badge/Pandas-2.1.1-yellow.svg) ![NumPy](https://img.shields.io/badge/NumPy-1.26.2-lightgreen.svg) ![Docker](https://img.shields.io/badge/Docker-Containerization-2496ED.svg)

## Project Overview
This project develops a machine learning model to predict loan defaults using the HMEQ dataset. The goal is to enable lenders to:
- Identify high‑risk borrowers
- Minimize loan defaults
- Optimize lending decisions

---

## Objective
- Build an accurate, interpretable model for loan default prediction
- Identify key risk factors impacting loan defaults
- Enable seamless deployment via REST APIs and containerization

---

## Dataset
- **Source**: HMEQ Loan Dataset
- **Rows**: 5,960
- **Original Features**: 13
- **Final Features after One‑Hot Encoding**: 18
- **Target Variable**: `BAD` (1 = Default, 0 = No Default)

---

## Methodology
### 1. EDA & Insights
- Identified class imbalance (~20% default rate).
- Analyzed key predictors (`DEBTINC`, `CLAGE`, `LOAN`, `MORTDUE`).

### 2. Data Pre-Processing
- Imputed missing values (median for numeric, mode for categorical).
- One‑hot encoded `REASON` and `JOB`.
- Created a clean, numerical dataset for modeling.

### 3. Model Development
- Logistic Regression
- Decision Tree
- Random Forest
- Final Model: **Tuned Random Forest** (Best Performance)

---

## Results
| Model                | Accuracy | Recall (BAD=1) | F1 Score | ROC‑AUC |
|----------------------|----------|----------------|----------|---------|
| Logistic Regression  | 81%      | 11%            | 0.19     | 0.675   |
| Decision Tree        | 83%      | 58%            | 0.58     | 0.739   |
| Random Forest        | 89%      | 62%            | 0.70     | 0.951   |
| **Tuned Random Forest** | **90%**  | **64%**        | **0.71** | **0.954** |

---

## Deployment
- Framework: REST APIs using **Flask** or **FastAPI**
- Containerization: Model and app packaged with **Docker** for reproducibility
- Enables batch or real‑time prediction for loan assessments

---

## Business Impact
- Enables precise identification of high‑risk loan applicants
- Reduces loan defaults by an estimated 30–40%
  








