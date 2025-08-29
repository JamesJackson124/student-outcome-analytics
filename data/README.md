# Data Overview

This folder contains all datasets used in the **Student Outcome Analysis Project**.  
The data comes from the **Open University Learning Analytics Dataset (OULAD)**, which contains anonymised information on over 32,000 students across multiple modules and presentations.

---

## Folder Structure

```
data/
├── raw/
│   ├── assessments.csv
│   ├── courses.csv
│   ├── studentAssessment.csv
│   ├── studentInfo.csv
│   ├── studentRegistration.csv
│   ├── studentVle.csv
│   └── vle.csv
└── master-table.csv
```

---

## Raw Data (in `raw/`)

- **assessments.csv**  
  Metadata for each assessment (weight, type, deadline).

- **courses.csv**  
  Details about each course (module code, length, start date).

- **studentAssessment.csv**  
  Individual student submissions and scores for assessments.

- **studentInfo.csv**  
  Demographic data (age band, gender, region, IMD band, disability, highest education, etc.).

- **studentRegistration.csv**  
  Student registration and withdrawal data.

- **studentVle.csv**  
  Student engagement with the virtual learning environment (VLE), measured as clicks.

- **vle.csv**  
  Metadata for each VLE resource (type, week available, etc.).

---

## Processed Data

- **master-table.csv**  
  The final cleaned and merged dataset.  
  - One row per student per module-presentation.  
  - Contains aggregated features such as:  
    - Average assessment score.  
    - Number of assessments submitted.  
    - Total VLE clicks.  
  - Includes demographic features from `studentInfo`.  
  - Used as the input dataset for EDA and modelling.

---

## Notes
- Intermediate cleaned versions (e.g., aggregated `studentAssessment` or `studentVle`) are not stored here to keep the repository light.  
- All transformations are documented in **`notebooks/data-prep.ipynb`**.  

---

**Author:** James Jackson
