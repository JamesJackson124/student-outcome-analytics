# Notebooks Overview

This folder contains all Jupyter notebooks used in the **Student Outcome Analysis Project**. The workflow follows a structured pipeline, starting from data preparation and progressing through exploratory analysis, feature diagnostics, modelling, and dashboard prototyping.

---

## 1. data-prep.ipynb
- Loads 4 key OULAD tables: `studentInfo`, `studentAssessment`, `assessments`, `studentVle`.
- Performs SQL + pandas cleaning.
- Handles missing values (replace, preserve, or drop depending on context).
- Aggregates assessment scores and VLE clicks per student.
- Produces **master-table.csv**: one row per student per module-presentation.

## 2. eda.ipynb
- Generates grouped counts and outcome percentages by categorical features (e.g., gender, region, disability, age band).
- Exports these as structured Excel tables for further review.
- Provides descriptive statistics for numeric features.

## 3. eda-visuals.ipynb
- Custom-styled visualisations using Matplotlib/Seaborn:
  - Stacked bar charts (outcome by category).
  - Scatter plots with regression and R² values.
  - Histograms and boxplots for numeric variables segmented by outcomes.
- Includes outlier handling (e.g., capping total_clicks at 99th percentile).

## 4. correlation-heatmap.ipynb
- Creates a correlation matrix between numeric features and the binary pass/fail target.
- Adds custom formatting for readability.
- Helps identify which features to prioritise for modelling.

## 5. regression-analysis.ipynb
- Quantifies feature importance via regression diagnostics:
  - Numeric variables → linear regression on binned groups, R² as strength indicator.
  - Categorical variables → pass rate comparisons across groups.
- Identifies strongest predictors (avg_score, studied_credits, imd_band, etc.).

## 6. modelling.ipynb
- Prepares features with one-hot encoding and scaling.
- Defines binary target (Pass vs. Fail/Withdraw).
- Splits dataset into train/test with stratified sampling.
- Trains **logistic regression** model.
- Evaluates with accuracy, F1, ROC AUC, confusion matrix, ROC curve.

## 7. dashboard-prototype.ipynb
- Builds interactive predictor using **ipywidgets**.
- Accepts user inputs for demographics & engagement variables.
- Outputs predicted pass probability from the trained model.
- Validates feature column alignment to prevent mismatch errors.

---

## Usage Notes
- Run notebooks sequentially for reproducibility.
- Outputs (CSV, Excel, PNG) are stored in the relevant `/data/`, `/tables/`, and `/visualisations/` folders.
- The modelling notebook must be executed before using the dashboard prototype.

---

**Author:** James Jackson
