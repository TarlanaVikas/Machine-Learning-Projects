# Machine-Learning-Projects

## 📂 Projects

### 1. Student Grade Prediction
- **Folder:** `Student Grade Prediction`
- **Description:** Predicts student final grades based on demographic, social, and academic features.
- **Dataset:** `student-mat.csv`
- **Notebook:** `Student_Grade_Prediction.ipynb`
- **Highlights:**
  - Data cleaning and feature engineering
  - Regression models (Linear Regression, Random Forest)
  - Performance evaluation using RMSE and R²

---

### 2. COVID-19 Analysis
- **Folder:** `COVID-19 Analysis`
- **Description:** Analyzes COVID-19 case trends and predicts future spread using time-series and ML models.
- **Dataset:** `covid_data.csv`
- **Notebook:** `COVID19_Analysis.ipynb`
- **Highlights:**
  - Exploratory data analysis with visualizations
  - Time-series forecasting (ARIMA, Prophet)
  - Trend analysis and prediction accuracy

---

### 3. Income Prediction using Random Forest
* **Folder:** `Income Prediction`
* **Description:** Predicts whether an individual's income exceeds $50K per year based on demographic and employment-related attributes.
* **Dataset:** `data.csv`
* **Notebook:** `Income_Prediction_RandomForest.ipynb`
* **Highlights:**
  - Data preprocessing with imputation and one-hot encoding
  - Random Forest Classifier with balanced class weights
  - Model evaluation using Accuracy, Precision, Recall, and F1-score
  - Confusion matrix visualization
  - Feature importance analysis (top 15 predictors)

---

### 4. Customer Segmentation using K-Means
* **Folder:** `Customer Clustering`
* **Description:** Groups customers into distinct clusters based on credit and interaction behavior to identify patterns and support targeted strategies.
* **Dataset:** `data.csv`
* **Script/Notebook:** `Customer_Clustering.py` (or `Customer Clustering.ipynb` if run in Colab)
* **Highlights:**
  - Data preprocessing with feature selection and standard scaling  
  - Optimal cluster determination using **Elbow Method** and **Silhouette Analysis**  
  - K-Means clustering with configurable number of clusters  
  - PCA-based 2D visualization of customer clusters  
  - Cluster-level statistics showing mean values of key features  

---

### 5. Revenue Prediction using Linear Regression
* **Folder:** `Revenue Prediction`  
* **Description:** Predicts company revenue based on financial and operational features such as marketing spend, R&D investment, administrative costs, workforce size, and region. Supports scenario-based forecasting to aid strategic decision-making.  
* **Dataset:** `data.csv`  
* **Script/Notebook:** `revenue_prediction.py` (or `Revenue Prediction using Linear Regression.ipynb` if run in Colab)  
* **Highlights:**  
  - Data preprocessing with **StandardScaler** for numerical features and **OneHotEncoder** for categorical features  
  - Linear Regression model wrapped in a **scikit-learn Pipeline** for clean workflow  
  - Model evaluation using **MAE**, **RMSE**, and **R² Score**  
  - Scenario-based revenue predictions for different business cases  
  - Modular functions for loading data, training, evaluation, and prediction  

---

### 6. Loan Approval using Logistic Regression
* **Folder:** `Loan Approval`  
* **Description:** Predicts loan approval status (`loan_status`) based on applicant demographics, financial attributes, and loan details. Provides interpretable coefficients to understand factors influencing approval or rejection.  
* **Dataset:** `data.csv`  
* **Script/Notebook:** `loan_approval.py` (or `Loan Approval using Logistic Regression.ipynb` if run in Colab)  
* **Highlights:**  
  - Data preprocessing with **SimpleImputer** (median for numeric, most frequent for categorical)  
  - **StandardScaler** for numerical features and **OneHotEncoder** for categorical features  
  - Logistic Regression model wrapped in a **scikit-learn Pipeline** for streamlined workflow  
  - Model evaluation using **Accuracy**, **Classification Report**, and **Confusion Matrix**  
  - Feature importance analysis using logistic regression coefficients to identify top approval/rejection factors  
  - Modular functions for loading data, training, evaluation, and feature importance display  

---

### 7. Loan Approval using Decision Trees
* **Folder:** `Loan Approval`  
* **Description:** Predicts loan approval status (`loan_status`) based on applicant demographics, financial attributes, and loan details using a **Decision Tree Classifier**. Provides a visual representation of decision rules for interpretability.  
* **Dataset:** `data.csv`  
* **Script/Notebook:** `loan_approval.py` (or `Loan Approval using Decision Trees.ipynb` if run in Colab)  
* **Highlights:**  
  - Data preprocessing with **SimpleImputer** (median for numeric, most frequent for categorical)  
  - **OneHotEncoder** for categorical features  
  - Decision Tree Classifier wrapped in a **scikit-learn Pipeline** for streamlined workflow  
  - Model evaluation using **Accuracy**, **Classification Report**, and **Confusion Matrix**  
  - Tree visualization with **matplotlib** and `plot_tree` for interpretable decision paths  
  - Modular functions for loading data, training, evaluation, visualization, and prediction  
  - Example applicant prediction included for demonstration of real-world usage  

---


## 🛠️ Skills Showcased

### 🔢 Data Handling & Preprocessing
* **Data Cleaning & Imputation:** Handling missing values with strategies like median (numeric) and most frequent (categorical).  
* **Feature Engineering:** Creating meaningful features from raw data (e.g., student demographics, loan attributes).  
* **Encoding Techniques:** OneHotEncoding for categorical variables; Label Encoding where appropriate.  
* **Scaling & Normalization:** StandardScaler for numerical features to improve model performance.  
* **Pipeline Construction:** Building modular, reusable pipelines with `scikit-learn` for preprocessing + modeling.  

---

### 📊 Machine Learning Algorithms
* **Regression Models:** Linear Regression for continuous predictions (grades, revenue).  
* **Classification Models:** Logistic Regression, Random Forest, Decision Trees for categorical outcomes (income, loan approval).  
* **Clustering Models:** K-Means for unsupervised customer segmentation.  
* **Time-Series Forecasting:** ARIMA and Prophet for COVID-19 trend prediction.  
* **Model Evaluation:** Accuracy, Precision, Recall, F1-score, RMSE, MAE, R² — applied across regression, classification, and clustering tasks.  

---

### 📈 Model Interpretation & Insights
* **Feature Importance Analysis:** Identifying top predictors in Random Forest, Logistic Regression coefficients, and Decision Tree splits.  
* **Decision Path Visualization:** Using `plot_tree` to interpret loan approval rules.  
* **Cluster Profiling:** Summarizing customer clusters with PCA visualization and mean feature statistics.  
* **Scenario Forecasting:** Revenue prediction under different business cases.  

---

### 🎨 Visualization & Communication
* **Exploratory Data Analysis (EDA):** Visualizing distributions, correlations, and trends with `matplotlib` and `seaborn`.  
* **Tree & Cluster Visualizations:** Interpretable decision paths and PCA-based cluster plots.  
* **Trend Analysis:** COVID-19 case progression and forecasting visualizations.  
* **Confusion Matrix & Reports:** Clear communication of classification performance.  

---

### 🧑‍💻 Software Engineering Practices
* **Modular Code Design:** Functions for loading data, training, evaluation, prediction, and visualization.  
* **Reproducibility:** Fixed random states for consistent results.  
* **Documentation:** README files with project descriptions, highlights, and usage instructions.  
* **Version Control:** Organized project folders and scripts for GitHub repositories.  

---

### 🌐 Professional & Applied Skills
* **Business Applications:** Revenue forecasting, loan approval automation, customer segmentation for targeted strategies.  
* **Education & Social Impact:** Student grade prediction and COVID-19 spread analysis.  
* **Recruiter-Friendly Presentation:** Clear project summaries, highlights, and modular workflows for portfolio visibility.  
* **Interpretability & Transparency:** Models chosen not only for accuracy but also for explainability (Logistic Regression coefficients, Decision Tree visualization).  

---
