# global-cancer-trends-2015-2024 📈🩺

> **Exploratory Data Analysis & Baseline Modeling**

---

## 🚀 Project Summary

A polished, reproducible analysis of global cancer patient data (2015–2024). This project performs thorough EDA, statistical testing, visualization, and baseline predictive modeling to investigate relationships between risk factors, treatment costs, cancer stages, and survival outcomes.

This README was generated after carefully reviewing the `Cancer_Data_Analysis.ipynb` notebook and includes a clear roadmap to reproduce and extend the work.

---

## 📁 Repository Structure

```
global-cancer-trends-2015-2024/
├── Cancer_Data_Analysis.ipynb     # Main Jupyter notebook
├── global_cancer_patients_2015_2024.csv  # Primary dataset
├── assets/                         # (suggested) images & plots exported from notebook
├── requirements.txt                # Suggested Python dependencies
└── README.md                       # This file
```

---

## ✨ Highlights (from the notebook)

* Cleaned and explored a global dataset of cancer patients (2015–2024).
* Visualized distributions (age, gender, country, cancer type, stage) and trends by year.
* Examined correlations between **treatment cost** and **survival years** (Pearson & Spearman tests).
* Assessed **early-stage diagnosis proportions** across cancer types (Stage 0 + Stage I).
* Fitted **interaction models** (e.g., `Target_Severity_Score ~ Genetic_Risk * Smoking`) to test whether genetic risk amplifies smoking effects.
* Built baseline predictive models:

  * Random Forest to predict **Target\_Severity\_Score** (feature importance and diagnostics included).
  * Random Forest with **GridSearchCV** for **Survival\_Years**. (Best parameters and evaluation metrics are shown in the notebook.)

---

## 📌 Key Reproducible Results (from the notebook)

* `GridSearchCV` best parameters for Survival Years prediction (example found in notebook):

  ```text
  {'max_depth': 5, 'min_samples_leaf': 2, 'min_samples_split': 5, 'n_estimators': 200}
  ```

  Observed R² (example run): train ≈ 0.0090, test ≈ -0.0003 — indicates the model struggles to explain survival variance and needs improvements/feature engineering.

> Full model outputs, coefficients, p-values (stat tests), and plots are available inline in `Cancer_Data_Analysis.ipynb`.

---

## 🧭 How to run locally

1. Clone the repo

```bash
git clone <your-repo-url>
cd global-cancer-trends-2015-2024
```

2. Create venv & install packages

```bash
python -m venv venv
source venv/bin/activate   # macOS / Linux
venv\Scripts\activate     # Windows
pip install -r requirements.txt
```

If `requirements.txt` is missing, install the common packages used in the notebook:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy statsmodels jupyterlab plotly
```

3. Open the notebook

```bash
jupyter lab
# then open Cancer_Data_Analysis.ipynb
```

---

## 🧪 Notebook Walkthrough (recommended order)

1. **01\_data\_overview** — load dataset, inspect shape, nulls, dtypes, duplicates.
2. **02\_univariate\_analysis** — distributions: Age, Gender, Country, Cancer\_Type, Cancer\_Stage.
3. **03\_bivariate\_analysis** — scatterplots, correlation matrix, cost vs survival tests (Pearson/Spearman).
4. **04\_stage\_analysis** — proportions of early-stage (Stage 0 + Stage I) per cancer type with bar charts.
5. **05\_stat\_tests** — normality checks (Shapiro), Kruskal/ANOVA as appropriate, and interpretation.
6. **06\_interaction\_models** — OLS regressions with interactions (Genetic\_Risk × Smoking) and summaries.
7. **07\_models** — baseline RandomForest regressors with feature importance, and hyperparameter tuning (GridSearchCV) for survival.
8. **08\_conclusions** — practical takeaways, limitations, and suggested next steps.

---

## 🔬 Suggested Improvements & Next Steps

* Improve target modeling:

  * More feature engineering (e.g., comorbidity counts, treatment-type encoding, time-to-treatment).
  * Try gradient boosting (XGBoost / LightGBM) and proper hyperparameter tuning with nested CV.
  * Use survival-specific models (Cox proportional hazards, random survival forests) for survival-time analysis.

* Address imbalance/skew:

  * Log-transform targets when skewed (`np.log1p`) or use quantile regressors.

* Explainability:

  * Use SHAP values for model interpretability and publish plots in `assets/`.

* Packaging:

  * Move pipeline steps to `src/` scripts and add unit tests (`pytest`).
  * Add a small Streamlit or Dash app to showcase interactive charts.

---

## 📷 Visualization tips for README (optional)

* Export key plots from the notebook to `assets/` and embed them in this README for an attractive GitHub landing page. Examples:

```markdown
![Survival Distribution](assets/survival_distribution.png)
![Early Stage Proportion by Cancer Type](assets/early_stage_by_type.png)
```

---

## 📎 Files to add (recommended)

* `requirements.txt` — pin package versions.
* `.gitignore` — ignore `.venv`, `__pycache__`, `.ipynb_checkpoints`, large raw data if needed.
* `assets/` — exported static images from notebook.
* `LICENSE` — e.g., MIT license if you want open reuse.

---

## 🤝 Want me to polish further?

I can also:

* Export and embed the top 6 plots into `assets/` and update the README with badges and images.
* Convert the notebook sections into separate scripts under `src/`.
* Produce a short `presentation.md` or `slides` summary for interviews.

Tell me which of these you want next and I will update the repo files accordingly.

---

*Made with care — your notebook reviewed and a beautiful README generated.*
