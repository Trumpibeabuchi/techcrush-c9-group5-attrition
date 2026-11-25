# Predicting Employee Attrition — Techcrush Cohort 9, Group 5_C9

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Trumpibeabuchi/techcrush-c9-group5-attrition/blob/main/notebooks/EMPLOYEE_ATTRITION_PREDICTION.ipynb)

Capstone project for the Techcrush Data Science Bootcamp, Cohort 9 — Case 2: Employee Attrition (classification).

## 1. Problem
Which employees are likely to leave, and what is linked to leaving?
**Who will use this:** HR managers deciding where to focus retention effort.

## 2. Hypotheses (written before analysis)
| # | Hypothesis | Result |
|---|---|---|
| H1 | Employees who work overtime leave more | **Supported**: 30.5% vs 10.4%, about 3× |
| H2 | Lower monthly income is linked to more leaving | **Partly supported**: gap mostly reflects seniority; within level 1, leavers earn ~10% less |
| H3 | Employees in their first 2 years, and younger staff, leave more | **Supported**: 0–2 years 29.8%, age 18–25 35.8% |
| H4 | Low satisfaction / poor work-life balance is linked to more leaving | **Supported**: mainly at the lowest score (up to 31.2%) |
| H5 | Frequent business travel is linked to more leaving | **Supported**: 24.9% vs 8.0% for non-travel |
| H6 | Attrition differs strongly by job role | **Supported**: Sales Representatives 39.8% vs Research Directors 2.5% |
| H7 | Gender and education make little difference (control) | **Supported**: no significant difference |

## 3. Dataset
- **Source:** [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset) (Kaggle)
- **File:** [`data/WA_Fn-UseC_-HR-Employee-Attrition.csv`](data/WA_Fn-UseC_-HR-Employee-Attrition.csv) — the notebook loads it directly from this repository, so no upload is needed.
- **Size:** 1,470 employees × 35 columns; 237 (16.1%) left.
- **Note:** fictional data created by IBM data scientists, so findings illustrate the method, not a real company. The 16% is the share of leavers in a snapshot, not an annual turnover rate.

## 4. Team
| Name | GitHub | Role |
|---|---|---|
| <name> | @<handle> | Lead, integration, submission |
| Trump Ibeabuchi | [Trumpibeabuchi](https://github.com/Trumpibeabuchi) | Exploratory data analysis |
| <name> | @<handle> | Modelling |
| <name> | @<handle> | Report & slides |

## 5. Repository structure
```
data/        raw dataset (CSV)
notebooks/   EMPLOYEE_ATTRITION_PREDICTION.ipynb          full analysis
             EMPLOYEE_ATTRITION_PREDICTION_simple.ipynb   same analysis, simpler EDA and plain-language findings
figures/     charts exported by the notebook, used in the report and slides
requirements.txt
```

## 6. How to run
1. Click the **Open in Colab** badge above.
2. Runtime → Run all. The data loads from this repository automatically.
3. Local alternative: `pip install -r requirements.txt`, then open the notebook in Jupyter and run all cells from the repository root.

## 7. Method
Train/test split (80/20, stratified) · 5-fold cross-validation · Logistic Regression vs Random Forest · metrics: precision, recall, F1, confusion matrix, ROC-AUC (accuracy alone is misleading with only 16% leavers).

## 8. Results
TBD — table comparing models; top factors chart.

## 9. Recommendations
TBD — at least 3, written for HR managers, each linked to a confirmed hypothesis.

## 10. Limitations
- **Units are not documented, and the data is fictional, so results are compared in relative terms.** No currency is given for income and no unit for distance from home, so findings are stated as percentages or ratios (e.g. "leavers earn X% less"), never in dollars.
- TBD (e.g. small number of leavers, associations not causes).

## 11. Links and sources
- Medium report: <link>
- Slides: <link>
- Sources used: <every notebook/article consulted, with links>
