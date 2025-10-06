# Apple Quality Prediction (R/Python)

## Overview
Supervised learning project to **predict and classify apple quality** from measurable traits (e.g., Size, Weight, Sweetness, Crunchiness, Juiciness, Ripeness, Acidity). Includes EDA, feature engineering, baselines (linear/logistic) and tree-based models, plus explainability and evaluation artifacts. ~**87% accuracy** with Sweetness & Crunchiness among top predictors.

## Repo Structure
```
apple-quality/
├─ data/                # raw/cleaned CSVs (not tracked)
├─ notebooks/           # EDA + modeling notebooks (Rmd/ipynb)
├─ src/                 # reusable R/Python scripts
├─ reports/             # figures, tables, final PDF
└─ README.md
```

## Getting Started
**R**
```r
install.packages(c("tidyverse","caret","randomForest","pROC","vip"))
rmarkdown::render("notebooks/Apple_Quality_Report.Rmd")
```
**Python**
```bash
pip install -r requirements.txt
jupyter lab
```

## Key Steps
- **EDA:** distributions, outliers, bivariate relationships  
- **Preprocessing:** imputation, scaling (where needed), factor encoding  
- **Models:** Logistic/Linear, Random Forest; hyperparameter tuning  
- **Evaluation:** accuracy/F1 (classification), RMSE/R² (regression), ROC-AUC, confusion matrix  
- **Explainability:** permutation/GINI importance; partial dependence snapshots

## Results
- **Top signals:** Sweetness, Crunchiness (consistently highest importance)  
- **Performance:** ~87% classification accuracy across held-out folds (details in `reports/`)

## Reproduce
- Place input CSVs in `data/` (see schema in the report).  
- Run the R Markdown (preferred) or Python notebook to regenerate figures and tables.

## Ethics & Notes
- Documented feature definitions and grading thresholds; checked for label leakage and class imbalance.  
- Results are illustrative; do not use for human-health or food-safety decisions without validation.

