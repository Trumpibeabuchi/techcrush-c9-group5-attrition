# Changelog

Changes made to the team notebook after it was copied from the team leader's Colab
(`EMPLOYEE ATTRITION PREDICTION .ipynb`, last edited 2026-11-24) into this repository.
Newest first.

## 2026-11-25: Restructured sections 1–3

- Every subsection now follows one pattern: a one-sentence intro (what we check and
  why), the code, then a **Finding**.
- Section 2 (Data Loading) now only loads and describes the data. `df.info()` and the
  two `describe()` cells moved to section 3, where they belong.
- Section 3 is split into 3.1 types and missing values, 3.2 duplicates, 3.3 value
  ranges and categories, 3.4 constant and ID columns, 3.5 which column measures pay,
  and 3.6 summary and cleaning decisions.
- **Duplicate check fixed:** `df.duplicated()` could never find duplicates because
  every row has a unique `EmployeeNumber`; the check now ignores the ID.
- Removed the 35-row `nunique()` table (its useful parts are covered by the
  constant-columns check and `describe(include="object")`).
- Added category listing and a year-consistency check (3.3) to rule out disguised
  missing values and impossible values.
- **New 3.5:** correlation heatmap showing that only `MonthlyIncome` behaves like pay
  (0.95 with `JobLevel`); the three Rate columns relate to nothing. H2 will use
  `MonthlyIncome` only.
- **Cleaning:** `EmployeeCount`, `Over18`, `StandardHours` (constant) and
  `EmployeeNumber` (ID) are dropped; the result is `df_clean` (1,470 × 31), used from
  section 4 onwards.
- Replaced the outdated findings text with a summary table (3.6).

## 2026-11-25: Removed repeated overview cells

- Removed the column-name list: `df.info()` lists every column with its type and
  non-null count.
- Replaced the two-print dimensions cell with one readable sentence
  ("The dataset has 1,470 rows (employees) and 35 columns.").
- Replaced the 35-row missing-values table with a one-line total
  (`df.isnull().sum().sum()` → 0), because `df.info()` already shows 1,470 non-null
  values in every column.

## 2026-11-25: Shorter notebook introduction

- Replaced the long introduction (old sections 1–7: introduction, problem statement,
  objectives, scope, machine-learning approach, library descriptions, column list) with
  a short header: title, research question, dataset, link to this README, the
  hypotheses H1–H7, and the note on units.
  - **Why:** the notebook should hold the analysis and the notes that explain decisions
    and findings. Background and context belong in the README and the Medium report.
  - The removed text is still in this repository's git history (commit `d6d3110`) and
    can be reused for the Medium report's introduction.
- Renumbered the sections: 1 Setup, 2 Data loading, 3 Data Quality Assessment,
  4 Exploratory Data Analysis (4.1, 4.2, …).
- Added to the README limitations: *"Units are not documented, and the data is
  fictional, so results are compared in relative terms."*

## 2026-11-25: Moved to this repository and made it run end to end

- **Data loading:** the notebook now reads the CSV from `data/` in this repository
  instead of `files.upload()`. The upload cell had failed (`TypeError: 'NoneType' object
  is not subscriptable`), so no cell after the imports had run.
- Added the dataset to `data/WA_Fn-UseC_-HR-Employee-Attrition.csv` (1,470 rows × 35
  columns, 237 leavers).
- Colab badge points to this repository; removed an empty code cell.
- Sub-headings for 4.1 and 4.2 made real Markdown headings (they were plain text).
- Charts are saved to `figures/`.
- Executed from start to finish with no errors; outputs are included.
