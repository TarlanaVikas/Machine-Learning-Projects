
# 📊 Student Performance Prediction

## 📌 Project Overview
This project focuses on predicting the **final grade (G3)** of students based on various demographic, social, and academic factors.  
The goal is to build a regression model that can accurately forecast student performance, potentially aiding in **early intervention strategies**.

---

## 📂 Data Source
The dataset used is **student-mat.csv**, which contains information about students from a Portuguese secondary school.  
It includes attributes such as:

- **Demographic information:** `sex`, `age`, `address`, `famsize`, `Pstatus`  
- **Parental information:** `Medu`, `Fedu` (mother's and father's education), `Mjob`, `Fjob` (mother's and father's job), `guardian`  
- **School-related features:** `traveltime`, `studytime`, `failures`, `schoolsup`, `famsup`, `paid`, `activities`, `nursery`, `higher`, `internet`, `romantic`  
- **Health and lifestyle:** `famrel`, `freetime`, `goout`, `Dalc` (weekday alcohol consumption), `Walc` (weekend alcohol consumption), `health`, `absences`  
- **Grades:** `G1` (first period grade), `G2` (second period grade), `G3` (final grade — target variable)

---

## ⚙️ Data Preprocessing & Feature Engineering
Steps performed to prepare the data for modeling:

1. **Loading Data:** Loaded into a pandas DataFrame.  
2. **Initial Exploration:** Used `data.head()` and `data['G3'].describe()` to understand the dataset and target distribution.  
3. **Missing Values Check:** Verified with `data.isnull().any()` and `data.isnull().sum()` — no missing values found.  
4. **Feature Correlation:** Found that `G1` and `G2` are highly correlated with `G3`.  
5. **Feature Engineering:** Created a new feature:  
   ```python
   data['GradeAvg'] = (data['G1'] + data['G2'] + data['G3']) / 3
   ```  
6. **Feature Selection:** Dropped `school` and `age` columns.  
7. **Categorical Encoding:**  
   - Binary categorical features mapped to `0/1`.  
   - Multi-category nominal features (`Mjob`, `Fjob`, `reason`, `guardian`) mapped to integer categories.  

---

## 🤖 Model Training
- **Data Splitting:** Divided into features (`X`) and target (`y = G3`).  
  Used `train_test_split` with `test_size=0.2` and `random_state=44`.  
- **Model Selection:** Chose `LinearRegression` from `sklearn.linear_model`.  
- **Model Fitting:** Trained on `X_train` and `y_train`.  

---

## 📈 Results
- The model achieved an **R² score of 1.0** on the test set.  

⚠️ **Note on Results:**  
A perfect score strongly suggests **data leakage**. Since `G1`, `G2`, and `GradeAvg` (which includes `G3`) were used as features, the model had direct access to the target variable.  
For realistic prediction, **remove G1, G2, and GradeAvg** if the goal is to predict G3 before these grades are known.

---

## 🚀 How to Use / Reproduce
1. Install required libraries:
   ```bash
   pip install pandas numpy scikit-learn seaborn matplotlib
   ```
2. **Clone the Repository:**  
   Download the project files to your local machine.  
3. **Place Data:**  
   Ensure `student-mat.csv` is in the `/content/` directory or update the path in the code.  
4. **Run the Notebook:**  
   Execute the cells in the Jupyter/Colab notebook sequentially to reproduce preprocessing, model training, and evaluation steps.  

---

## 📌 Future Improvements
- Avoid data leakage by removing `G1`, `G2`, and `GradeAvg` when predicting `G3`.  
- Experiment with other regression models (e.g., Random Forest, Gradient Boosting).  
- Perform feature importance analysis to identify key predictors.  
- Use cross-validation for more robust evaluation.  

---
```

