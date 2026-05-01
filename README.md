# DevelopersHub Corporation — Data Science & Analytics Internship Tasks

This repository contains my work for the **DevelopersHub Corporation — Data Science & Analytics Internship**.  
Each task is implemented in a **clean, reproducible, ML-dev style** using **Python**, **pandas**, **seaborn/matplotlib**, and **scikit-learn**.

**Internship Requirement:** Complete at least **3 out of 5** tasks  
**Completed:** **Task 1, Task 2, Task 3, Task 4** ✅ (4/5)

---
``` text
## Table of Contents
- [Repository Structure](#repository-structure)
- [Tech Stack](#tech-stack)
- [Setup (How to Run)](#setup-how-to-run)
- [Completed Tasks](#completed-tasks)
  - [Task 1 — Iris Dataset EDA](#task-1--iris-dataset-eda)
  - [Task 2 — Credit Risk Prediction](#task-2--credit-risk-prediction)
  - [Task 3 — Customer Churn Prediction](#task-3--customer-churn-prediction)
  - [Task 4 — Insurance Charges Prediction (Regression)](#task-4--insurance-charges-prediction-regression)
- [Submission Notes](#submission-notes)
```
---

## Repository Structure


DevelopersHub-DS-Internship-Tasks/
├─ notebooks/
│  ├─ Task1_Iris_EDA.ipynb
│  ├─ Task2_Credit_Risk.ipynb
│  ├─ Task3_Churn.ipynb
│  ├─ Task4_Insurance_Regression.ipynb
│  └─ Task5_Personal_Loan.ipynb          # (optional / if completed)
│
├─ outputs/
│  ├─ task1_figures/                      # saved charts (optional)
│  ├─ task2_figures/                      # EDA + confusion matrix
│  ├─ task3_figures/                      # EDA + feature importance
│  ├─ task4_figures/                      # EDA + residual diagnostics
│  └─ task5_figures/                      # (if completed)
│
├─ data/                                  # datasets (NOT pushed to GitHub)
├─ README.md
└─ .gitignore

## Tech Stack
- ython
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

## Setup (How to Run)
1) Create a virtual environment (recommended)

```bash
python -m venv .venv
# Windows PowerShell:
.venv\Scripts\Activate.ps1
# Mac/Linux:
source .venv/bin/activate
```

2) Install dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3) Run notebooks
Open notebooks in Jupyter / VS Code / Colab and run cells top-to-bottom (recommended: Run All).


## Completed Tasks
## Task 1 — Iris Dataset EDA
### Objective
Load the Iris dataset and perform basic exploration and visualization.

### Dataset
- Iris dataset (loaded using seaborn.load_dataset("iris") or a local CSV)

## Notebook
- notebooks/Task1_Iris_EDA.ipynb

### Checklist (Requirements Covered)
- Data loading and inspection using pandas
   - .shape, .columns, .head()

- Basic summarization
   - .info(), .describe()
   - Missing values and duplicates check

- Required Visualizations
   - Scatter plot (relationships)
   - Histogram (distribution)
   - Box plot (outliers/spread)

- Optional (extra EDA for quality)
   - Correlation heatmap
   - Pairplot


### Outputs
- outputs/task1_figures/ (if figure saving is enabled)

### Conclusion
The notebook includes a short conclusion summarizing patterns observed in plots (species separation, distribution, and spread/outliers).


## Task 2 — Credit Risk Prediction
### Objective
Predict whether a loan applicant is likely to default / whether a loan will be approved (depending on dataset target).

### Dataset
- Kaggle Loan Prediction Dataset
  Place file at: data/loan_prediction.csv

### Notebook
- notebooks/Task2_Credit_Risk.ipynb

### Checklist (Requirements Covered)

- Missing value handling
   - SimpleImputer for numeric + categorical features

- EDA
   - Visualizations for key features (e.g., loan amount, education, income)

- Model Training
   - Baseline: Logistic Regression
   - Production-style preprocessing using Pipeline + ColumnTransformer

- Evaluation
   - Accuracy
   - Confusion Matrix
   - (Extra) Classification report, ROC-AUC (if available), Cross-validation

### Outputs
- outputs/task2_figures/ (EDA charts + confusion matrix)

### Results
- Test Accuracy: 0.8537
- ROC-AUC (if computed): 0.8375


## Task 3 — Customer Churn Prediction
### Objective
Identify customers who are likely to leave the bank (churn).

### Dataset
- Churn Modelling Dataset
Place file at: data/Churn_Modelling.csv

### Notebook
- notebooks/Task3_Churn.ipynb

### Checklist (Requirements Covered)
- Cleaning & preparation
  - Drop ID-like columns (if present)
  - Missing value checks

- Encoding categorical features
  - One-Hot Encoding (Geography, Gender, etc.)

- Model Training
  - Baseline: RandomForestClassifier
  - Clean preprocessing via Pipeline + ColumnTransformer

- Evaluation
  - Accuracy
  - Confusion Matrix
  - (Extra) Classification report, Cross-validation

- Feature Importance
  - Extracts feature names after encoding and shows top churn drivers

### Outputs
- outputs/task3_figures/ (EDA plots, confusion matrix, feature importance plot)

### Results
- Test Accuracy: 0.8615
- CV Accuracy mean: 0.8595 | std: 0.0065


## Task 4 — Insurance Charges Prediction (Regression)
### Objective
Estimate medical insurance charges based on personal data.

### Dataset
- Medical Cost Personal Dataset (commonly insurance.csv)
  - Expected columns typically include: age, bmi, smoker, charges
- Note: If a wrong local CSV is present (e.g., only age and bought_insurance), the notebook uses an auto-fix approach by downloading the correct public dataset (if internet is available).

### Notebook
- notebooks/Task4_Insurance_Regression.ipynb

### Checklist (Requirements Covered)
- Model
  - Linear Regression with preprocessing pipeline

- Required EDA
  - Visualize impact of BMI, age, and smoker on charges

- Evaluation
  - MAE
  - RMSE
  - (Extra) R² + residual diagnostics for better reporting

### Outputs
- outputs/task4_figures/ (EDA + residual plots)

### Results
- MAE: 4181.19
- RMSE: 5796.28
- R²: 0.7836


## Task 5 — Personal Loan Acceptance Prediction (Bank Marketing)
### Objective
Predict which customers are likely to accept a personal loan offer.

### Dataset
- Bank Marketing Dataset (UCI Machine Learning Repository)
Common file names: bank.csv, bank-full.csv
Place file inside: data/

### Notebook
- notebooks/Task5_Personal_Loan.ipynb

### Checklist (Requirements Covered)
- Basic data exploration
  - EDA for key features such as age, job, and marital

- Model Training
  - Baseline: Logistic Regression (or Decision Tree if used)
  - Preprocessing: SimpleImputer + OneHotEncoder using Pipeline + ColumnTransformer

- Evaluation
  - Accuracy
  - Confusion Matrix
  - (Extra) ROC-AUC / cross-validation (optional)

- Business Insights
  - Identify which customer groups are more likely to accept the offer (acceptance rate tables + plots)

### Outputs
- outputs/task5_figures/ (EDA plots + confusion matrix + coefficient plots, if enabled)

### Results (fill after running)
- Test Accuracy: 0.8183
- ROC-AUC (if computed): 0.8923
- CV Accuracy mean: 0.814 | std: 0.0054


## Submission Notes
- Code is organized and documented with Markdown sections inside notebooks.
- Datasets are not uploaded to GitHub (kept in data/ locally).
- Repository link is submitted on Google Classroom.
