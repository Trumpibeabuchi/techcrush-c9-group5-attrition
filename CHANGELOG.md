# Changelog

Changes made to the team notebook after it was copied from the team leader's Colab
(`EMPLOYEE ATTRITION PREDICTION .ipynb`, last edited 2026-11-24) into this repository.
Newest first.

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
