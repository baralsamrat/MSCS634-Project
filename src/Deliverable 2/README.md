# MSCS 634 — Project Deliverable 2: Regression Modeling and Performance Evaluation

**Author:** Samrat Baral
**Course:** MSCS634 - Advanced Big Data and Data Mining
**Deliverable:** 2 — Regression Modeling and Performance Evaluation
**Repository:** [https://github.com/baralsamrat/MSCS634-Project](https://github.com/baralsamrat/MSCS634-Project)
**Date:** November 16, 2025

---

## Dataset Used

* **Title:** Organ Donation and Transplantation Dataset
* **Source:** Kaggle — [https://www.kaggle.com/datasets/iamsouravbanerjee/organ-donation-and-transplantation](https://www.kaggle.com/datasets/iamsouravbanerjee/organ-donation-and-transplantation)
* **Granularity:** One row ≈ one transplant event (recipient, donor, organ, metadata, waiting time, outcome)
* **Suggested filename:** `organ_donation_cleaned.csv` or `organ_donation.csv` in `../data/`
* **Why appropriate for regression:**

  * Contains **continuous target variable** → `Wait_Time_Days`
  * Includes rich numerical and categorical predictors (age, gender, organ type, blood type)
  * Suitable for **feature engineering**, **multiple regression**, **regularization**, **cross-validation**, and **performance comparison**.

---

## What This Deliverable Includes

### 📘 Jupyter Notebook

`Deliverable2_Regression.ipynb` includes:

* **Feature Engineering**

  * Age difference (`Age_Diff`)
  * Gender match (`Same_Gender`)
  * Adult recipient indicator (`Is_Adult_Recipient`)
  * Date-based features (`Transplant_Year`, `Transplant_Month`)
  * Optional log-transformed target (`Wait_Time_Log1p`)

* **Regression Models Built**

  * **Linear Regression (baseline)**
  * **Ridge Regression** (L2 regularization)
  * **Lasso Regression** (L1 regularization)

* **Evaluation Metrics**

  * R-squared (R²)
  * Mean Squared Error (MSE)
  * Root Mean Squared Error (RMSE)

* **Cross-Validation (k=5)**

  * CV-R² and CV-RMSE
  * Stability and generalization assessment

* **Visualizations**

  * Predicted vs Actual Scatter Plot
  * Residual Distribution Plot
  * Saved automatically to `figures/`

* **Rubric Summary**

  * Automatically printed in the notebook
  * Also saved to:
    `reports/Deliverable2_Rubric_Summary.txt`

### 📂 Folder Structure Used

```
src/Deliverable 2/
│
├── Deliverable2_Regression.ipynb
├── README.md
│
├── data/
├── figures/
├── models/
└── reports/
```

### 📄 Supporting Files

* **`requirements.txt`** (shared across deliverables)
* **`.gitignore`** (Python + Jupyter patterns)

---

## How to Run

```bash
cd MSCS634-Project/src/"Deliverable 2"

python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate

pip install -r ../../requirements.txt
jupyter lab   # or jupyter notebook
```

Open:
`Deliverable2_Regression.ipynb`
and run the cells in order.

---

## Key Steps (for Your Instructor Submission)

### ✓ Notebook

* Perform feature engineering and clearly explain why each feature is useful.
* Run **multiple regression models** and **compare them using R², MSE, RMSE**.
* Include **cross-validation results** to show model generalization.
* Ensure plots are labeled and saved into `figures/`.
* Summarize which model performed best and **why**.

### ✓ README

* Summarize dataset
* Describe models built
* Explain metrics used
* Highlight best-performing model
* Mention any challenges (e.g., handling categorical variables, overfitting, limited signal)

### ✓ Repository

* Make sure this deliverable is inside:
  `src/Deliverable 2/`
* Commit your notebook, README, figures, and reports.

---

If you want, I can now also generate:

✅ **Deliverable 3 README**
✅ **Deliverable 3 notebook template**
or
I can integrate Deliverable 1 + 2 into a single clean GitHub-ready package.

Just tell me **“Next Deliverable 3”** and I’ll generate everything.
