# Machine-Learning-Projects

A curated collection of applied machine learning projects showcasing skills in data preprocessing, model building, evaluation, and visualization. Each project demonstrates practical use cases with clear workflows and reproducible results.

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-yellow?style=flat&logo=scikitlearn)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=flat&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical-013243?style=flat&logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c?style=flat&logo=plotly)
![Seaborn](https://img.shields.io/badge/Seaborn-EDA-9cf?style=flat)

---

## 📂 Projects

### 1. Student Grade Prediction
- **Folder:** `Student Grade Prediction`
- **Description:** Predicts student final grades based on demographic, social, and academic features.
- **Dataset:** `student-mat.csv`
- **Notebook:** `Student_Grade_Prediction.ipynb`
- **Highlights:**
  - Comprehensive **data cleaning** (handling missing values, encoding categorical features).
  - **Feature engineering**: parental education, study time, absences, and social factors.
  - Regression models: **Linear Regression** and **Random Forest Regressor**.
  - Performance evaluation using **RMSE** and **R²**.
  - Insights into which factors most strongly influence academic performance.

---

### 2. COVID-19 Analysis
- **Folder:** `COVID-19 Analysis`
- **Description:** Analyzes COVID-19 case trends and predicts future spread using time-series and ML models.
- **Dataset:** `covid_data.csv`
- **Notebook:** `COVID19_Analysis.ipynb`
- **Highlights:**
  - Exploratory data analysis with **trend visualizations** and correlation heatmaps.
  - Time-series forecasting using **ARIMA** and **Facebook Prophet**.
  - Rolling averages and growth rate analysis for better interpretability.
  - Prediction accuracy compared across models.
  - Clear communication of pandemic progression and potential future scenarios.

---

### 3. Income Prediction using Random Forest
- **Folder:** `Income Prediction`
- **Description:** Predicts whether an individual's income exceeds $50K per year based on demographic and employment-related attributes.
- **Dataset:** `data.csv`
- **Notebook:** `Income_Prediction_RandomForest.ipynb`
- **Highlights:**
  - **Data preprocessing**: imputation, one-hot encoding, scaling.
  - **Random Forest Classifier** with balanced class weights for fairness.
  - Model evaluation using **Accuracy, Precision, Recall, F1-score**.
  - Confusion matrix visualization for classification clarity.
  - **Feature importance analysis** highlighting top predictors (education, occupation, hours worked).

---

### 4. Customer Segmentation using K-Means
- **Folder:** `Customer Clustering`
- **Description:** Groups customers into distinct clusters based on credit and interaction behavior to identify patterns and support targeted strategies.
- **Dataset:** `data.csv`
- **Notebook/Script:** `Customer_Clustering.py` or `Customer Clustering.ipynb`
- **Highlights:**
  - Preprocessing with **feature selection** and **standard scaling**.
  - Optimal cluster determination using **Elbow Method** and **Silhouette Score**.
  - **K-Means clustering** with configurable cluster sizes.
  - PCA-based 2D visualization of customer clusters.
  - Cluster-level statistics summarizing behavioral differences.

---

### 5. Revenue Prediction using Linear Regression
- **Folder:** `Revenue Prediction`
- **Description:** Predicts company revenue based on financial and operational features such as marketing spend, R&D investment, administrative costs, workforce size, and region.
- **Dataset:** `data.csv`
- **Notebook/Script:** `revenue_prediction.py` or `Revenue Prediction using Linear Regression.ipynb`
- **Highlights:**
  - Preprocessing with **StandardScaler** and **OneHotEncoder**.
  - Linear Regression model wrapped in a **scikit-learn Pipeline**.
  - Evaluation using **MAE, RMSE, R² Score**.
  - Scenario-based forecasting for strategic decision-making.
  - Modular functions for reproducibility and clarity.

---

### 6. Loan Approval using Logistic Regression
- **Folder:** `Loan Approval`
- **Description:** Predicts loan approval status (`loan_status`) using applicant demographics, financial attributes, and loan details.
- **Dataset:** `data.csv`
- **Notebook/Script:** `loan_approval.py` or `Loan Approval using Logistic Regression.ipynb`
- **Highlights:**
  - Preprocessing with **SimpleImputer**, **StandardScaler**, and **OneHotEncoder**.
  - Logistic Regression pipeline for streamlined workflow.
  - Evaluation using **Accuracy, Classification Report, Confusion Matrix**.
  - Feature importance analysis via regression coefficients.
  - Clear identification of factors influencing approval/rejection.

---

### 7. Loan Approval using Decision Trees
- **Folder:** `Loan Approval`
- **Description:** Predicts loan approval status (`loan_status`) using a **Decision Tree Classifier** with interpretable decision paths.
- **Dataset:** `data.csv`
- **Notebook/Script:** `loan_approval.py` or `Loan Approval using Decision Trees.ipynb`
- **Highlights:**
  - Preprocessing with **SimpleImputer** and **OneHotEncoder**.
  - Decision Tree pipeline for modularity.
  - Evaluation using **Accuracy, Classification Report, Confusion Matrix**.
  - Tree visualization with `plot_tree` for interpretability.
  - Example applicant prediction included for real-world demonstration.

---

## 🛠️ Skills Showcased

### 🔢 Data Handling & Preprocessing
- Data cleaning, imputation, encoding, scaling, and pipeline construction.

### 📊 Machine Learning Algorithms
- Regression (Linear Regression, Random Forest), Classification (Logistic Regression, Decision Trees), Clustering (K-Means), Time-Series (ARIMA, Prophet).

### 📈 Model Interpretation & Insights
- Feature importance, decision path visualization, cluster profiling, scenario forecasting.

### 🎨 Visualization & Communication
- EDA with **matplotlib** and **seaborn**, confusion matrices, PCA plots, forecasting charts.

### 🧑‍💻 Software Engineering Practices
- Modular code design, reproducibility, documentation, version control.

### 🌐 Professional & Applied Skills
- Business applications (revenue forecasting, loan approval automation, customer segmentation).
- Education/social impact (student grade prediction, COVID-19 analysis).
- Recruiter-friendly presentation with clear highlights and modular workflows.

---

**🚀 This repository demonstrates end-to-end ML workflows — from raw data preprocessing to model deployment-ready pipelines — with emphasis on clarity, interpretability, and real-world impact.**
