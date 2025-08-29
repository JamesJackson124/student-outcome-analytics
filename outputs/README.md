# Outputs Overview

This folder contains all generated outputs from the **Student Outcome Analysis Project**.  
These outputs include visualisations created during EDA, regression analysis, and modelling, as well as summary Excel tables that guided the analysis.

---

## Folder Structure

```
├── outputs/     # All plots and charts generated during analysis
│   ├── distributions/
│   ├── categorical_vs_outcome/
│   ├── feature_relationships/
│   ├── numeric_feature_analysis/
│   ├── r_squared_analysis/
│   ├── model_diagnostics/
│   └── regression_coefficients/
│   └── excel/

---

## Visualisations

### `distributions/`
- Outcome distributions (simple pass/fail; full pass/fail/distinction/withdrawn).
- Histograms and countplots for numeric features (avg_score, total_clicks, studied_credits, previous_attempts).

### `categorical_vs_outcome/`
- Stacked bar charts comparing outcome breakdowns across categorical features.
- Includes gender, age_band, imd_band, disability, region, and others.

### `feature_relationships/`
- Pair plot exploring relationships between multiple features.
- Correlation heatmap showing numeric feature correlations with binary target.

### `numeric_feature_analysis/`
- Boxplots of key numeric variables (avg_score, num_assessments, studied_credits, total_clicks) segmented by outcome.

### `r_squared_analysis/`
- Scatter + regression line plots of binned numeric variables vs pass rate.
- R² scores used to quantify predictive strength of features.

### `model_diagnostics/`
- Confusion matrix of logistic regression predictions vs actual outcomes.
- ROC curve with AUC score.

### `regression_coefficients/`
- Horizontal coefficient plots from logistic regression.
- Includes regional dummy variables and other demographic/academic factors.

---

## Tables

### `excel/`
- **summary_tables.xlsx** (or equivalent):  
  Contains grouped counts and percentages of student outcomes (Pass, Fail, Withdrawn, Distinction) across key categorical features:
  - Region  
  - Gender  
  - Disability  
  - Age band  
  - IMD band  
  - Previous attempts  
- These tables were exported directly from EDA notebooks and used to guide visualisation and modelling decisions.

---

## Notes
- All visualisations were created in **Matplotlib** or **Seaborn** (EDA, regression) and saved as `.png`.
- Tables were generated using **pandas** and exported to Excel for structured review.
- Outputs are for interpretability and reproducibility — not used as model inputs (those come from `/data/master-table.csv`).

---

**Author:** James Jackson
