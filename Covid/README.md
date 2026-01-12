# COVID-19 Data Analysis: Trends, Comparisons, and Prediction

## 📌 Project Overview
This project aims to analyze global and country-specific COVID-19 data to:
- Identify key trends in case numbers and testing.
- Compare the progression of the pandemic across different regions.
- Explore prediction models for future case numbers.

---

## 📊 Dataset Description: `covid.csv`
The dataset contains global COVID-19 statistics, aggregated by country and date. It provides a comprehensive view of the pandemic’s impact and contributing factors.

### Key COVID-19 Metrics
- **Cases & Deaths:** `total_cases`, `new_cases`, `total_deaths`, `new_deaths`
- **Normalized Metrics:** `total_cases_per_million`, `new_cases_per_million`, `total_deaths_per_million`, `new_deaths_per_million`
- **Testing Data:** `total_tests`, `new_tests`, `total_tests_per_thousand`, `new_tests_per_thousand`, `new_tests_smoothed`, `new_tests_smoothed_per_thousand`
- **Government Response:** `stringency_index`

### Demographic & Health Features
- **Population Data:** `population`, `population_density`, `median_age`
- **Age Distribution:** `aged_65_older`, `aged_70_older`
- **Economic Indicators:** `gdp_per_capita`, `extreme_poverty`
- **Health Indicators:** `cvd_death_rate`, `diabetes_prevalence`, `female_smokers`, `male_smokers`
- **Infrastructure:** `handwashing_facilities`, `hospital_beds_per_100k`

This rich dataset enables analysis of COVID-19 trends in relation to socio-economic, demographic, and health system characteristics.

---

## 🔍 Data Exploration Steps
1. **Loading the Dataset:**  
   `covid.csv` was loaded into a pandas DataFrame using `pd.read_csv('covid.csv')`.

2. **Initial Overview:**  
   - `covid.head()` → Preview first 5 rows.  
   - `covid.shape` → Dataset size: **19496 rows × 32 columns**.  
   - `covid.columns` → List of all features.

3. **Missing Values:**  
   - `covid.isna().any()` → Identify columns with missing data.  
   - `covid.isna().sum()` → Quantify missing values (e.g., `total_tests`, `handwashing_facilities`).

4. **Filtering by Country/Region:**  
   - India → `india_case`  
   - Brazil → `brazil_case`  
   - India, China, Japan → `india_japan_china`  
   - Germany, Spain → `germany_spain`

---

## 📈 Data Visualizations
### Time-Series Plots (India)
- **Total Cases Over Time:** Line plots showing cumulative growth of cases.  
- **Total Tests Over Time:** Line plots illustrating testing capacity and efforts.  
- **Zoomed Views:** Focused plots for the last 5 days of data.

### Comparative Bar Plots
- **India, China, Japan:** Comparison of total cases across Asian countries.  
- **Germany, Spain:** Comparison of total cases across European countries.

### Top 5 Countries (May 24, 2020)
- Bar plot of countries with the highest total cases (excluding "World").

---

## 🤖 Machine Learning Analysis
A **Linear Regression model** was applied to India’s total cases.

### Preprocessing
- Converted `date` column to datetime objects → then to ordinal numbers.  
- Features: `date` (ordinal) → Independent variable (X).  
- Target: `total_cases` → Dependent variable (y).

### Model Training
- Train-test split: **70% training, 30% testing**.  
- Model: `LinearRegression()` from `sklearn.linear_model`.  
- Training performed on reshaped arrays (`.reshape(-1,1)`).

### Prediction & Evaluation
- Predictions generated for test set.  
- **Metrics:**
  - Mean Squared Error (MSE) → Measures prediction accuracy.  
  - R-squared Score → Proportion of variance explained by the model.  

### Example Future Prediction
```python
lr.predict(np.array([[737573]]))
```
Forecasts total cases for a given future date (ordinal format).

---

## 🛠️ Libraries Used
- **pandas** (data manipulation)  
- **numpy** (numerical operations)  
- **seaborn** (statistical visualization)  
- **matplotlib.pyplot** (plotting)  
- **datetime** (date handling)  
- **sklearn.model_selection** (train-test split)  
- **sklearn.linear_model** (linear regression)  
- **sklearn.metrics** (model evaluation)

---

## ▶️ Instructions to Run
1. Ensure Python is installed (preferably in a virtual environment).  
2. Install required libraries:
   ```bash
   pip install pandas numpy seaborn matplotlib scikit-learn
   ```
3. Place `covid.csv` in the same directory as the notebook.  
4. Open the notebook in **Jupyter Lab**, **Jupyter Notebook**, or **Google Colab**.  
5. Run all cells sequentially to reproduce the analysis and visualizations.

---

## 📌 Key Findings
- India’s total cases showed a continuous upward trend through May 2020.  
- Testing capacity increased steadily but varied in pace.  
- Comparative analysis highlighted differences in case progression across countries.  
- Linear regression provided a baseline predictive model, though limited in capturing non-linear trends.

---

## 🚀 Next Steps
- Apply advanced time-series models (e.g., **ARIMA**, **Prophet**) for improved forecasting.  
- Explore correlations between demographic/health features (e.g., `hospital_beds_per_100k`, `aged_65_older`) and COVID-19 outcomes.  
- Extend analysis to vaccination data and post-2020 trends.

---
