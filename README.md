# Predicting Employee Attrition — Techcrush Cohort 9, Group 5_C9

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Trumpibeabuchi/techcrush-c9-group5-attrition/blob/main/notebooks/EMPLOYEE_ATTRITION_PREDICTION.ipynb)

Capstone project for the Techcrush Data Science Bootcamp, Cohort 9 — Case 2: Employee Attrition (classification).

## 1. Problem
Which employees are likely to leave, and what is linked to leaving?
**Who will use this:** HR managers deciding where to focus retention effort.

## 2. Hypotheses (written before analysis)
| # | Hypothesis | Result |
|---|---|---|
| H1 | Employees who work overtime leave more | TBD |
| H2 | Lower monthly income is linked to more leaving | TBD |
| H3 | Employees in their first 2 years, and younger staff, leave more | TBD |
| H4 | Low satisfaction / poor work-life balance is linked to more leaving | TBD |
| H5 | Frequent business travel is linked to more leaving | TBD |
| H6 | Attrition differs strongly by job role | TBD |
| H7 | Gender and education make little difference (control) | TBD |

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
notebooks/   EMPLOYEE_ATTRITION_PREDICTION.ipynb
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
TBD (e.g. fictional data, small number of leavers, associations not causes).

## 11. Links and sources
- Medium report: <link>
- Slides: <link>
- Sources used: <every notebook/article consulted, with links>
