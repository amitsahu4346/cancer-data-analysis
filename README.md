# 🧬 Cancer Data Analysis (2015–2024)

This project presents an **end-to-end data analysis and machine learning study** on **global cancer patients (2015–2024)**.  
It covers **descriptive statistics, visualization, statistical hypothesis testing, and predictive modeling** to uncover trends in cancer severity, survival, risk factors, and economic burden.

---

📂 Project Structure
├── Cancer_Data_Analysis.ipynb   # Main Jupyter Notebook
├── global_cancer_patients_2015_2024.csv   # Dataset
└── README.md   # Documentation



---

## 🚀 Key Features
- ✅ **Data Preprocessing & Cleaning** (missing values, duplicates, encoding)  
- ✅ **Exploratory Data Analysis (EDA)**:  
  - Age distribution (histograms, KDE plots)  
  - Gender, Country/Region, Cancer Type & Stage analysis  
  - Treatment cost distribution  
- ✅ **Risk Factors Analysis**: Smoking, Alcohol, Obesity, Air Pollution, Genetic Risk  
- ✅ **Statistical Testing**:  
  - Pearson & Spearman correlation  
  - Shapiro-Wilk (normality)  
  - Kruskal-Wallis test (non-parametric ANOVA)  
  - OLS Regression with Interaction Terms  
- ✅ **Predictive Modeling**:  
  - Random Forest Regressor (Severity Score)  
  - Random Forest with GridSearchCV (Survival Years)  
  - Feature importance analysis  
- ✅ **Healthcare Economics**:  
  - Treatment costs by Country, Gender, Age Group  
  - Heatmaps for economic burden  
- ✅ **Insights**:  
  - Early-stage diagnosis proportions  
  - Impact of stage on cost & survival  
  - Relationship between treatment cost and survival  

---

## 📊 Dataset
- **File:** `global_cancer_patients_2015_2024.csv`  
- **Size:** 50,000+ records  
- **Attributes include:**  
  - Patient demographics (Age, Gender, Country/Region)  
  - Cancer details (Type, Stage, Severity Score)  
  - Risk factors (Genetic Risk, Smoking, Alcohol, Obesity, Air Pollution)  
  - Treatment cost (USD)  
  - Survival years  

---

## ⚙️ Installation & Requirements

Clone this repo:
```bash
git clone https://github.com/your-username/cancer-data-analysis.git
cd cancer-data-analysis

Install dependencies:

pip install -r requirements.txt

🛠 Requirements

numpy
pandas
seaborn
matplotlib
scipy
scikit-learn
statsmodels
jupyter

Open Notebook:

jupyter notebook Cancer_Data_Analysis.ipynb

📈 Sample Visualizations

Age & Gender distribution
Country-wise cancer incidence (Pie Chart)
Cancer types & stages (Bar Plots)
Risk factors vs Severity (Regression plots)
Treatment costs across countries (Heatmaps)
Feature importance from Random Forest
