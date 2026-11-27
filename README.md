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
| H7 | Gender and education make little difference (control) | **No difference found, as expected** |

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
notebooks/   EMPLOYEE_ATTRITION_PREDICTION.ipynb   the analysis
figures/     charts exported by the notebook, used in the report and slides
To_Delete/   superseded files, kept until the team confirms they can be removed
requirements.txt
```

## 6. How to run
1. Click the **Open in Colab** badge above.
2. Runtime → Run all. The data loads from this repository automatically.
3. Local alternative: `pip install -r requirements.txt`, then open the notebook in Jupyter and run all cells from the repository root.

## 7. Method
1. **Data quality:** missing values, duplicates (ignoring the ID), value ranges and categories, constant columns, and which column measures pay. Four columns are dropped (three constant, one ID).
2. **Exploratory analysis, one hypothesis at a time:** each group's **attrition rate** (% who left) is compared with the overall 16.1%. A chi-square test (categories) or Mann-Whitney U test (numbers) checks whether a difference could be chance (p < 0.05).

## 8. Results
From the exploratory analysis (details in the hypothesis table above and in the notebook, section 4.10). Leaving is concentrated in three groups:
1. **Early career:** employees in their first 2 years (29.8% left), aged 18–25 (35.8%) or at job level 1 (26.3%), often Sales Representatives (39.8%) or Laboratory Technicians (23.9%).
2. **Workload:** overtime (30.5% vs 10.4%) and frequent travel (24.9% vs 8.0%), each about 3 times the rate.
3. **Dissatisfaction:** a bottom score (1) on job satisfaction, environment or work-life balance (22.8–31.2%).

Pay matters mainly at entry level. Gender and education make no difference.

## 9. Recommendations
From the exploratory analysis, for HR managers:
1. **Focus on the first two years** (H3, H6): onboarding, mentoring and early career conversations, starting with Sales Representatives and Laboratory Technicians.
2. **Manage workload** (H1, H5): monitor regular overtime and spread business travel more evenly.
3. **Act on low survey scores** (H4): follow up quickly with anyone who scores 1 on job satisfaction, environment or work-life balance.
4. **Review entry-level pay and promotion, not pay across the board** (H2).

## 10. Limitations
- **Units are not documented, and the data is fictional, so results are compared in relative terms.** No currency is given for income and no unit for distance from home, so findings are stated as percentages or ratios (e.g. "leavers earn X% less"), never in dollars.
- **Associations, not causes.** For example, overtime goes with leaving, but the data cannot show that overtime causes it.
- **A snapshot, not a rate over time.** The 16.1% is the share of leavers in the data, not an annual turnover rate.
- **Some groups are small.** For example, only 5 leavers at job level 4, 52 HR staff and 80 employees with work-life balance 1, so those figures are less reliable.
- **Many tests.** 14 tests were run at the 5% level, so about one could look significant by chance; every result relied on has p below 0.001 (department: 0.0045).

## 11. Links and sources
- Medium report: <link>
- Slides: <link>
- Sources used: <every notebook/article consulted, with links>
