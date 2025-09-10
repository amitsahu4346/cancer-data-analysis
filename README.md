🩺 Cancer Data Analysis (2015–2024)

This project analyzes global cancer patient data (2015–2024) to explore risk factors, treatment costs, cancer stages, and survival outcomes using Machine Learning & Statistical Analysis.
Notebook: Cancer_Data_Analysis.ipynb
Dataset: global_cancer_patients_2015_2024.csv

📊 Dataset

Source: Global cancer dataset (2015–2024)
Features include:

Patient ID

Gender

Country/Region

Cancer Type

Cancer Stage

Age at Diagnosis

Genetic Risk

Smoking, Alcohol Use, Obesity Level, Air Pollution Exposure

Treatment Cost (USD)

Survival Years

Target Severity Score (derived target)

🔎 Project Workflow
🔹 Data Preprocessing

Handled missing values & duplicates

Encoded categorical features (Gender, Country, Cancer_Type, Cancer_Stage)

Normality check with Shapiro-Wilk test

🔹 Exploratory Data Analysis (EDA)

Distribution of Age, Gender, Cancer Types, Stages

Country/Region-wise case counts

Correlation tests: Treatment Cost vs Survival Years (Pearson & Spearman)

Early Stage Diagnosis proportions (Stage 0 + Stage I) by Cancer Type

Interaction Models: Examined if Genetic Risk × Smoking increases severity

🔹 Model Building

Random Forest Regressor for Target Severity Score prediction

Random Forest + GridSearchCV for Survival Years prediction

Feature importance visualization

🔹 Evaluation

Metrics used:

R² Score (Train/Test)

Residual analysis

Observed that baseline Random Forest had low R² → scope for better models (XGBoost, Survival Analysis)

📈 Results

Early-stage diagnosis rates:

Lung Cancer ≈ 38% diagnosed at Stage 0/I

Leukemia ≈ 39% diagnosed at Stage 0/I

Treatment cost vs survival years: Weak correlation (both Pearson & Spearman)

Interaction (Genetic Risk × Smoking): Positive & significant, meaning smoking has a stronger negative effect for high-risk individuals

Model Performance:

Random Forest (Severity Prediction): R² ≈ low but feature importance useful

Random Forest + GridSearchCV (Survival Years): Best params found, but still poor generalization (Test R² < 0)

⚙️ Requirements

Install dependencies using:

pip install -r requirements.txt


Example requirements.txt:

pandas  
numpy  
matplotlib  
seaborn  
scikit-learn  
scipy  
statsmodels  
jupyterlab  
plotly  

▶️ How to Run

Clone the repository:

git clone https://github.com/your-username/global-cancer-trends-2015-2024.git
cd global-cancer-trends-2015-2024


Open the notebook:

jupyter notebook Cancer_Data_Analysis.ipynb


Run all cells step by step to reproduce results.

👨‍💻 Author: Amit Sahu

LinkedIn: linkedin.com/in/your-link

GitHub: github.com/amitsahu4346

Kaggle: kaggle.com/amitsahu

✅ अब तुम बस इसे copy-paste करके अपने GitHub repo के README.md में डाल दो।

👉 चाहो तो मैं तुम्हारे लिए एक requirements.txt और .gitignore भी बना दूँ क्या?

You said:
IS TYPE SE DO COPY EDIT DOWNLOAD 
ChatGPT said:

समझ गया भाई 👍
तुम्हें ऐसे ही आकर्षक README चाहिए जिसमें ऊपर Project name + emoji + Copy | Edit | Download style हो।

मैं तुम्हारे लिए वैसा ही तैयार करता हूँ:

🩺 global-cancer-trends-2015-2024 📊

Exploratory Data Analysis & Baseline Modeling

🚀 Project Summary

A polished, reproducible analysis of global cancer patient data (2015–2024).
This project performs:

Thorough EDA

Statistical testing & visualization

Predictive modeling (Random Forest, Regression, Correlation tests)

It investigates relationships between:

Risk factors (Smoking, Obesity, Genetic Risk, Pollution)

Treatment costs

Cancer stages

Survival outcomes

📂 Notebook → Cancer_Data_Analysis.ipynb
📂 Dataset → global_cancer_patients_2015_2024.csv

📊 Dataset Features

Patient demographics (Age, Gender, Country/Region)

Cancer type & stage

Lifestyle risks (Smoking, Alcohol, Obesity, Pollution)

Genetic risk

Treatment cost (USD)

Survival years

Derived target: Severity Score

🔎 Workflow
🧹 Data Preprocessing

✔ Handle missing values & duplicates
✔ Encode categorical features
✔ Normality check (Shapiro-Wilk test)

📈 Exploratory Data Analysis (EDA)

✔ Distribution of Cancer Types, Stages, Age
✔ Correlation → Treatment Cost vs Survival (Pearson & Spearman)
✔ Early-stage diagnosis rates
✔ Interaction models → Genetic Risk × Smoking

🤖 Modeling

Random Forest Regressor → Severity Score

Random Forest + GridSearchCV → Survival Prediction

Feature Importance Visualization

📉 Evaluation

Metrics: R², MAE, Residuals

Found weak predictive power → suggests exploring XGBoost, Survival Models

📈 Key Insights

Early diagnosis: ~38% of Lung Cancer & ~39% of Leukemia cases detected at Stage 0/I

Weak correlation between Treatment Cost & Survival Years

Strong interaction effect: Smoking worsens severity more for high genetic risk patients

Random Forest gave insights but low R² → need advanced models

⚙️ Requirements

Install dependencies:

pip install -r requirements.txt


requirements.txt

pandas  
numpy  
matplotlib  
seaborn  
scikit-learn  
scipy  
statsmodels  
jupyterlab  
plotly  

▶️ Run the Project

Clone repo:

git clone https://github.com/your-username/global-cancer-trends-2015-2024.git
cd global-cancer-trends-2015-2024


Open Jupyter Notebook:

jupyter notebook Cancer_Data_Analysis.ipynb


Run all cells sequentially.

👨‍💻 Author

Amit Sahu

🌐 LinkedIn

🐙 GitHub

📊 Kaggle
