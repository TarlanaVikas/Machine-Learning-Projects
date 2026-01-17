# 📘 Loan Approval Prediction using Logistic Regression

## 📌 Overview
This project demonstrates how to build a **loan approval prediction model** using **Logistic Regression**. The notebook walks through data preprocessing, model training, evaluation, and feature importance analysis.  

The goal is to predict whether a loan application will be **approved or rejected** based on applicant and loan-related features.

---

## ⚙️ Project Workflow
1. **Data Loading & Preprocessing**
   - Reads the dataset (`data.csv`).
   - Separates features (`X`) and target (`y` → `loan_status`).
   - Handles missing values:
     - Numerical features → median imputation + scaling.
     - Categorical features → most frequent imputation + one-hot encoding.
   - Combines preprocessing steps using `ColumnTransformer`.

2. **Model Training**
   - Logistic Regression classifier (`sklearn.linear_model.LogisticRegression`) with `max_iter=1000`.
   - Wrapped in a `Pipeline` to ensure preprocessing and classification are applied consistently.

3. **Model Evaluation**
   - Accuracy score.
   - Classification report (precision, recall, F1-score).
   - Confusion matrix.

4. **Feature Importance**
   - Extracts coefficients from the logistic regression model.
   - Displays top features contributing to loan approval and rejection.

---

## 📂 Dataset
- **File:** `data.csv`
- **Target Column:** `loan_status`  
- **Features:** Applicant demographics, financial details, loan attributes, credit history, etc.  
- Example features:
  - `person_age`, `person_income`, `loan_amnt`, `loan_int_rate`, `credit_score`
  - `person_home_ownership`, `loan_intent`, `previous_loan_defaults_on_file`

---

## 🛠️ Dependencies
Ensure the following Python libraries are installed:

```bash
pip install pandas numpy scikit-learn
```

- **pandas** → Data manipulation  
- **numpy** → Numerical operations  
- **scikit-learn** → ML model, preprocessing, evaluation  

---

## 🚀 Usage
1. Clone or download the repository.
2. Place your dataset (`data.csv`) in the working directory.
3. Run the notebook in **Google Colab** or locally:
   ```bash
   python loan_approval.py
   ```
4. The script will:
   - Train the model
   - Print evaluation metrics
   - Show top factors influencing loan approval/rejection

---

## 📊 Example Output
- **Accuracy:** ~90%  
- **Confusion Matrix:**  
  ```
  [[6600  400]
   [ 506 1494]]
  ```
- **Top Factors Increasing Approval:**
  - No previous loan defaults
  - Higher loan percent income
  - Lower interest rate
  - Renting home ownership

- **Top Factors Leading to Rejection:**
  - Previous loan defaults on file
  - Venture/Education loan intent
  - Mortgage/Own home ownership
  - Lower credit score

---

## 🔑 Key Insights
- **Credit history** and **previous loan defaults** are the strongest predictors of rejection.  
- **Income-to-loan ratio** and **lower interest rates** increase chances of approval.  
- Logistic Regression provides interpretable coefficients, making it suitable for financial decision-making.

---

## 📌 Future Improvements
- Try advanced models (Random Forest, XGBoost).
- Perform hyperparameter tuning.
- Add cross-validation for robust evaluation.
- Visualize feature importance with bar plots.

---
