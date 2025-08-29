# Student Outcome Analysis Project

## 1. Project Overview
This project investigates student performance and dropout risk using the **Open University Learning Analytics Dataset (OULAD)**.  
The goal is to understand factors influencing outcomes and build predictive tools to support student success.  

The workflow includes:
- Data preparation & cleaning (SQL + pandas)  
- Exploratory Data Analysis (EDA)  
- Feature importance & regression diagnostics  
- Predictive modelling with scikit-learn  
- Interactive dashboard prototyping  
- Deployment via a portfolio website (Dash → Docker → Fly.io)  

---

## 2. Data Source
The project uses the **OULAD dataset**, which contains anonymised information on 32,000+ students across 7 tables.  
For this analysis, we focused on 4 key tables:
- `studentInfo` – demographic information (age, gender, region, disability, etc.)  
- `studentAssessment` – individual assessment scores and submissions  
- `assessments` – metadata for each assessment (weight, deadline, type)  
- `studentVle` – engagement data (total clicks on the online learning environment)  

These were merged into a **master student table**, exported as `master-table.csv`, forming the basis for all further analysis.

---

## 3. Tools and Technologies
The project was developed in Python, using both **SQL (SQLite)** and **pandas** for data preparation.  
Key libraries include:
- **Data processing:** `pandas`, `numpy`, `sqlalchemy`  
- **Visualisation:** `matplotlib`, `seaborn`  
- **Modelling:** `scikit-learn`  
- **Interactivity:** `ipywidgets`, `dash`  
- **Deployment:** `docker`, `flyctl`  

A complete list of dependencies is available in **requirements.txt**.

---

## 4. Repository Structure
```
├── data/                # Cleaned datasets (e.g. master-table.csv)
├── notebooks/           # Jupyter notebooks (prep, EDA, modelling, dashboard)
├── tables/              # Exported Excel summary tables (categorical breakdowns)
├── visualisations/      # Saved plots (EDA, regression, heatmaps)
├── app/                 # Dash web application (multi-page structure)
├── requirements.txt     # Python dependencies
└── README.md            # This file
```

> 📌 *Each folder contains its own `README.md` for detailed documentation.*

---

## 5. Notebook Pipeline
The main analytical process is captured in a series of Jupyter notebooks:
1. **data-prep.ipynb** – Import OULAD tables, SQL + pandas cleaning, build `master-table.csv`  
2. **eda.ipynb** – Exploratory data analysis, outcome breakdowns, categorical tables  
3. **eda-visuals.ipynb** – Stacked bar charts, scatter plots with R², histograms & boxplots  
4. **correlation-heatmap.ipynb** – Numeric feature correlation with pass/fail target  
5. **regression-analysis.ipynb** – R² diagnostics for numeric features, categorical pass rate comparisons  
6. **modelling.ipynb** – Logistic regression model (scikit-learn) with performance metrics  
7. **dashboard-prototype.ipynb** – Interactive pass probability predictor (ipywidgets)  

---

## 6. Outputs
- **master-table.csv** – Clean, merged dataset ready for analysis  
- **Excel Tables:** Categorical outcome breakdowns (e.g., by gender, disability, age band)  
- **Plots:** Stacked bars, scatterplots, histograms, boxplots, correlation heatmap  
- **Model Results:** Logistic regression with accuracy, F1, ROC AUC, confusion matrix  
- **Dashboard Prototype:** Interactive predictor (ipywidgets)  
- **Portfolio Website:** Multi-page Dash app with student outcomes predictor page  

---

## 7. Contact
**Author:** James Jackson  
📧 Email: jamesneiljackson@gmail.com  

---
