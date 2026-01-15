# Customer Segmentation using K-Means

## 📌 Overview
This project demonstrates **customer segmentation** using the **K-Means clustering algorithm**. By analyzing customer behavior and credit-related features, we group customers into distinct clusters to better understand their profiles.  

The workflow includes:
- Data preprocessing  
- Feature scaling  
- Determining optimal clusters (Elbow & Silhouette methods)  
- Applying K-Means clustering  
- Visualizing clusters with PCA  
- Displaying cluster-level statistics  

---

## ⚙️ Requirements
Install the following dependencies before running the project:

```bash
pip install pandas numpy scikit-learn matplotlib
```

---

## 📂 Dataset
The project expects a CSV file named `data.csv` with the following columns:

- `Avg_Credit_Limit` – Average credit limit of the customer  
- `Total_Credit_Cards` – Number of credit cards held  
- `Total_visits_bank` – Number of visits to the bank  
- `Total_visits_online` – Number of online visits  
- `Total_calls_made` – Number of calls made  

> Ensure the dataset is clean and contains no missing values for these features.

---

## 🚀 How to Run
1. Place your dataset in the project directory as `data.csv`.  
2. Run the script:

```bash
python main.py
```

3. The program will:
   - Preprocess and scale the data  
   - Show **Elbow Method** and **Silhouette Analysis** plots  
   - Apply K-Means clustering (default: 3 clusters)  
   - Visualize clusters in 2D using PCA  
   - Print cluster-level statistics  

---

## 📊 Workflow Explanation

### 1. **Preprocessing**
- Selects relevant features from the dataset.  
- Applies **StandardScaler** to normalize values.  

### 2. **Optimal Cluster Determination**
- **Elbow Method**: Plots inertia vs. number of clusters.  
- **Silhouette Analysis**: Evaluates cluster quality.  

### 3. **K-Means Clustering**
- Groups customers into clusters.  
- Default cluster count = 3 (modifiable).  

### 4. **Visualization**
- Uses **PCA** to reduce dimensions to 2D.  
- Scatter plot shows customer distribution across clusters.  

### 5. **Cluster Statistics**
- Prints mean values of features per cluster.  
- Helps interpret customer behavior patterns.  

---

## 📈 Example Output

### Elbow Method
Shows the optimal number of clusters where inertia starts to flatten.  

### Silhouette Analysis
Indicates how well-separated clusters are.  

### Cluster Visualization
Scatter plot of PCA-reduced data with labeled clusters.  

### Cluster Statistics
```
Cluster Characteristics:

         Avg_Credit_Limit  Total_Credit_Cards  Total_visits_bank  Total_visits_online  Total_calls_made
Cluster                                                                                                
0                 50000.0                 3.2                2.1                  4.5               10.2
1                 15000.0                 1.5                5.3                  2.0                7.8
2                 30000.0                 2.7                3.0                  3.8                9.0
```

---

## 🛠️ Customization
- Change dataset path in `main()`:
  ```python
  file_path = "data.csv"
  ```
- Modify number of clusters:
  ```python
  optimal_clusters = 3
  ```

---

## 📌 Applications
- Customer segmentation for targeted marketing  
- Identifying high-value customers  
- Understanding customer behavior patterns  
- Optimizing resource allocation  

---

## 📜 License
This project is open-source and available under the MIT License.

---
