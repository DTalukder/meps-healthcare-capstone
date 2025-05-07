# MEPS Healthcare Cost Prediction – Capstone Project

This capstone project explores patterns in U.S. healthcare spending using the 2022 Full-Year Consolidated Data File (HC-243) from the Medical Expenditure Panel Survey (MEPS). 

The goal is to **predict total healthcare expenditure** (`TOTEXP22`) and **identify key cost drivers** such as insurance types, income level, and demographics.

## Project Overview

- **Problem**: Unpredictable and rising healthcare costs in the U.S.
- **Objective**: Predict `TOTEXP22` (Total Expenditure) using machine learning and extract insights on what drives high healthcare spending.
- **Dataset**: MEPS HC-243 (22,431 rows × 1,420 features)

## Project Steps

| Step | Description |
|------|-------------|
| 1. [Project Proposal](https://github.com/DTalukder/meps-healthcare-capstone/blob/main/Docs/Project%20Proposal.pdf) | Defined the problem and approach |
| 2. [Literature Review](https://github.com/DTalukder/meps-healthcare-capstone/blob/main/Docs/Literature%20Review.pdf) | Summarized 6+ peer-reviewed studies |
| 3. [Dataset Description](https://github.com/DTalukder/meps-healthcare-capstone/blob/main/Docs/Data_Description_Presentation.pdf) | Provided breakdown of MEPS HC-243 |
| 4. [EDA](https://github.com/DTalukder/meps-healthcare-capstone/blob/main/Code/EDA.ipynb) | Cleaned, explored, and visualized the data |
| 5. Feature Engineering | Selected key predictors, handled skewed values |
| 6. [Modeling](https://github.com/DTalukder/meps-healthcare-capstone/blob/main/Code/modeling_notebook.ipynb) | Trained and evaluated multiple ML models |
| 7. Interpretation | Used feature importances to explain predictions |
| 8. GitHub Deployment | Uploaded code, data, and project structure |
| 9. [Poster](https://github.com/DTalukder/meps-healthcare-capstone/blob/main/Docs/Capstone_MEPS_CostPrediction_Poster_2025.pdf) | Designed and published final project poster (PDF) |


## Modeling Results

| Model               | MAE     | RMSE     | R²     |
|--------------------|---------|----------|--------|
| Linear Regression  | 204.33  | 1,438.71 | 0.9943 |
| Decision Tree      | 988.88  | 9,211.89 | 0.7648 |
| Random Forest      | 661.07  | 4,248.95 | 0.9500 |
| Gradient Boosting  | 749.48  | 3,838.15 | 0.9592 |
| XGBoost            | 948.92  | 7,949.97 | 0.8249 |

>  **Best model**: Gradient Boosting (balanced performance + interpretation)

---

## Feature Importances (Gradient Boosting)

The top predictors of healthcare costs included:
- **TOTPTR22**: Total private third-party payments
- **TOTMCR22**: Medicare payments
- **TOTMCD22**: Medicaid payments
- **TOTPRV22**: Total private insurance
- **TOTSLF22**: Out-of-pocket/self-pay


##  Files in this Repository

| File | Description |
|------|-------------|
| `eda.ipynb` | Full Exploratory Data Analysis |
| `modeling_notebook.ipynb` | Full pipeline: Exploratory Data Analysis, Feature Engineering, and Predictive Modeling |
| `meps_cleaned.csv` | Cleaned dataset (used in modeling) |
| `README.md` | This file |
| `.gitignore` | Git tracking exclusions |



## Dataset Source

- [MEPS HC-243 Dataset (2022)](https://meps.ahrq.gov/mepsweb/data_stats/download_data_files_detail.jsp?cboPufNumber=HC-243)


## Dataset Access (External Link)

Due to file size limits, key datasets are hosted externally:

- [MEPS Raw Excel File – h243.xlsx](https://docs.google.com/spreadsheets/d/1BaL_Yar9wivzIVNd3rmeIjbbtC5-UOLV/edit?usp=drive_link&ouid=103669975884075903926&rtpof=true&sd=true)
- [Cleaned Modeling Dataset – meps_cleaned.csv](https://drive.google.com/file/d/1VvTNsor0S2T5yTib-2lbY-c0VyzySp19/view?usp=drive_link)

---

**Course**: CS668 - Capstone Project | Spring 2025

**Author**: DTalukder
