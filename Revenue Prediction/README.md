# 📊 Revenue Prediction using Linear Regression

## 📌 Overview
This project demonstrates how to build a **Revenue Prediction Model** using **Linear Regression** in Python.  
It leverages **scikit-learn pipelines** for preprocessing and modeling, ensuring clean, modular, and reproducible workflows.

The model predicts company revenue based on:
- Marketing Spend  
- R&D Spend  
- Administration Costs  
- Number of Employees  
- Region (categorical feature)

---

## ⚙️ Features
- **Data Preprocessing**  
  - Standardization of numerical features  
  - One-hot encoding of categorical features  
- **Model Training**  
  - Linear Regression wrapped in a pipeline  
- **Evaluation Metrics**  
  - Mean Absolute Error (MAE)  
  - Root Mean Squared Error (RMSE)  
  - R² Score  
- **Scenario Testing**  
  - Predicts revenue for custom business cases  

---

## 📂 Project Structure
```
RevenuePrediction/
│
├── data.csv                # Input dataset (must contain 'Revenue' column)
├── revenue_prediction.py   # Main script with all functions
├── README.md               # Documentation (this file)
└── requirements.txt        # Python dependencies
```

---

## 📊 Dataset Requirements
The dataset (`data.csv`) must include the following columns:

| Column Name            | Type      | Description                                |
|------------------------|-----------|--------------------------------------------|
| Marketing_Spend        | Numeric   | Amount spent on marketing                  |
| R&D_Spend              | Numeric   | Research & development expenditure         |
| Administration_Costs   | Numeric   | Administrative expenses                    |
| Number_of_Employees    | Numeric   | Workforce size                             |
| Region                 | Categorical | Business region (e.g., North America, Europe, Asia) |
| Revenue                | Numeric   | Target variable (company revenue)          |

---

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/revenue-prediction.git
   cd revenue-prediction
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### requirements.txt
```
pandas
numpy
scikit-learn
```

---

## 🚀 Usage

Run the script:
```bash
python revenue_prediction.py
```

### Example Output
```
Model Evaluation Metrics
------------------------
MAE  : 12000.45
RMSE : 15000.78
R²   : 0.8923

Revenue Prediction Scenarios

Scenario 1
Estimated Revenue: 250000.32

Scenario 2
Estimated Revenue: 145000.87

Scenario 3
Estimated Revenue: 400000.56
```

---

## 📈 Workflow Explanation

1. **Load & Preprocess Data**  
   - Reads `data.csv`  
   - Splits features (`X`) and target (`y`)  
   - Applies scaling and encoding  

2. **Train Model**  
   - Fits a Linear Regression model using a pipeline  

3. **Evaluate Model**  
   - Prints MAE, RMSE, and R² metrics  

4. **Predict Revenue**  
   - Runs predictions on predefined scenarios  

---

## 🔮 Custom Predictions
You can add your own scenarios in the `main()` function:

```python
scenarios = [
    {
        "Marketing_Spend": 60000,
        "R&D_Spend": 70000,
        "Administration_Costs": 18000,
        "Number_of_Employees": 40,
        "Region": "Europe"
    }
]
```

---

## 📌 Key Learnings
- How to use **ColumnTransformer** for mixed data types  
- Building **pipelines** for clean ML workflows  
- Evaluating regression models with multiple metrics  
- Making **business-oriented predictions**  

---
