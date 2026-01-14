# Income Prediction using Random Forest

## 📌 Project Overview
This project builds a machine learning pipeline to predict whether an individual's income exceeds **$50K per year** based on demographic and employment-related attributes. The dataset used (`data.csv`) contains both categorical and numerical features.

The notebook leverages **scikit-learn pipelines** for preprocessing and classification, ensuring reproducibility and modularity.

---

## ⚙️ Features

### 🔧 Data Preprocessing
- Handles missing values (`?` replaced with `NaN`).
- Median imputation for numerical features.
- Most frequent imputation + One-Hot Encoding for categorical features.

### 🤖 Model Training
- Random Forest Classifier with:
  - `n_estimators=200`
  - `class_weight="balanced"`
  - `random_state=42`
  - Parallel training (`n_jobs=-1`)

### 📈 Evaluation
- Accuracy score  
- Classification report (precision, recall, F1-score)  
- Confusion matrix  

### 🌟 Feature Importance
- Extracts and displays top 15 most important features.

---

## 📂 Project Structure
```
Code
├── Untitled0.ipynb        # Main notebook
├── sample_data/           # Default Colab sample data
└── data.csv               # Input dataset
```

---

## 🚀 How to Run
1. Open the notebook in **Google Colab**.  
2. Upload `data.csv` or place it in the working directory.  
3. Run all cells sequentially:
   - Data loading & preprocessing  
   - Train-test split  
   - Model training  
   - Evaluation & feature importance  

---

## 🧑‍💻 Code Workflow

### Load & Preprocess Data
```python
X, y, preprocessor = load_and_preprocess("data.csv")
```

### Train Model
```python
model = train_model(X_train, y_train, preprocessor)
```

### Evaluate Model
```python
evaluate_model(model, X_test, y_test)
```

### Feature Importance
```python
display_feature_importance(model, all_feature_names)
```

---

## 📊 Results

- **Accuracy:** ~85%  

### Confusion Matrix
```
[[4597  348]
 [ 620  948]]
```

### Top Features
- Age  
- Final weight (`fnlwgt`)  
- Marital status (Married-civ-spouse, Never-married)  
- Hours per week  
- Capital gain  
- Education level  
- Relationship (Husband, Wife, Own-child)  
- Occupation (Exec-managerial)  
- Sex (Male)  

---

## 🔮 Future Improvements
- Hyperparameter tuning with **GridSearchCV**  
- Try alternative models (**XGBoost, Logistic Regression**)  
- Feature engineering (e.g., grouping education levels)  
- Cross-validation for robust performance metrics  

---
