# 📘 Loan Approval Prediction using Decision Tree

## 📌 Overview
This project demonstrates how to build a **Decision Tree Classifier** to predict loan approval status based on applicant and loan details. It uses **scikit-learn pipelines** for preprocessing, model training, evaluation, and visualization.  

The workflow includes:
- Data preprocessing (handling missing values, encoding categorical features).
- Training a Decision Tree model.
- Evaluating performance with accuracy, classification report, and confusion matrix.
- Visualizing the decision tree.
- Making predictions for new applicants.

---

## ⚙️ Requirements
Ensure you have the following installed:

- Python 3.7+
- Libraries:
  ```bash
  pip install pandas numpy scikit-learn matplotlib
  ```

---

## 📂 Dataset
The dataset should be a CSV file named `data.csv` with the following columns:

- **Applicant Information**
  - `person_age` (int): Age of applicant  
  - `person_gender` (object): Gender (e.g., male/female)  
  - `person_education` (object): Education level (e.g., Bachelor, Master)  
  - `person_income` (float): Annual income  
  - `person_emp_exp` (int): Employment experience in years  
  - `person_home_ownership` (object): Home ownership status (RENT, OWN, MORTGAGE)  

- **Loan Information**
  - `loan_amnt` (float): Loan amount requested  
  - `loan_intent` (object): Purpose of loan (e.g., PERSONAL, EDUCATION, MEDICAL)  
  - `loan_int_rate` (float): Interest rate (%)  
  - `loan_percent_income` (float): Loan amount as a fraction of income  

- **Credit History**
  - `cb_person_cred_hist_length` (int): Length of credit history in years  
  - `credit_score` (int): Applicant’s credit score  
  - `previous_loan_defaults_on_file` (object): Whether applicant has defaulted before (Yes/No)  

- **Target Variable**
  - `loan_status` (int): 1 = Approved, 0 = Rejected  

---

## 🚀 How It Works

### 1. **Load & Preprocess Data**
- Missing values in numerical columns are imputed with the **median**.
- Missing values in categorical columns are imputed with the **most frequent value**.
- Categorical features are encoded using **OneHotEncoder**.

### 2. **Train Model**
- A **Decision Tree Classifier** is trained with:
  - Criterion: `gini`
  - Max depth: `5`
  - Random state: `42` (for reproducibility)

### 3. **Evaluate Model**
- Prints:
  - Accuracy score
  - Classification report (precision, recall, F1-score)
  - Confusion matrix

### 4. **Visualize Decision Tree**
- Displays a tree diagram with feature splits and class labels.

### 5. **Predict Loan Status**
- Accepts a dictionary of applicant details.
- Returns `"Approved"` or `"Rejected"`.

---

## 🖥️ Usage

### Run the Program
```bash
python loan_approval.py
```

### Example Output
```
Accuracy: 0.82

Classification Report:
              precision    recall  f1-score   support
Rejected         0.80      0.85      0.82        100
Approved         0.84      0.79      0.81        100

Confusion Matrix:
[[85 15]
 [21 79]]

Sample Applicant Loan Decision: Approved
```

---

## 📊 Visualization
The decision tree is plotted using `matplotlib`. Example:

- Nodes show feature splits (e.g., `credit_score <= 650`).
- Leaves show predicted class (`Approved` or `Rejected`).
- Colors indicate majority class at each node.

---

## 🧑‍💻 Example Prediction
```python
sample_applicant = {
    "person_age": 30,
    "person_gender": "male",
    "person_education": "Bachelor",
    "person_income": 60000,
    "person_emp_exp": 5,
    "person_home_ownership": "RENT",
    "loan_amnt": 15000,
    "loan_intent": "PERSONAL",
    "loan_int_rate": 12.5,
    "loan_percent_income": 0.25,
    "cb_person_cred_hist_length": 6,
    "credit_score": 680,
    "previous_loan_defaults_on_file": "No"
}

result = predict_loan_status(model, sample_applicant)
print("Loan Decision:", result)
```

Output:
```
Loan Decision: Approved
```

---

## 📌 Project Structure
```
loan_approval.py       # Main script
data.csv               # Dataset file (must be provided)
README.md              # Documentation
```

---

## 🔮 Future Improvements
- Hyperparameter tuning with GridSearchCV.
- Cross-validation for robust evaluation.
- Feature importance analysis.
- Deployment as a web app using Flask/Django.

---