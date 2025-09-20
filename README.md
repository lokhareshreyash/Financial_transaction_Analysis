# Financial_transaction_Analysis
End-to-end analysis of financial transactions with KPI extraction, anomaly detection, clustering, and classification using Python, SQL, and machine learning.

# Financial Transaction Analysis and Anomaly Detection

![Status](https://img.shields.io/badge/Status-Complete-green) ![Python](https://img.shields.io/badge/Language-Python-blue) ![Machine Learning](https://img.shields.io/badge/ML-KMeans%2C%20RandomForest-orange)

---

## Project Overview

This project analyzes **financial transaction data** to extract key insights, detect anomalies, cluster transaction patterns, and classify transaction types. It combines **data cleaning**, **SQL-based KPI extraction**, **visualizations**, **unsupervised clustering**, and **supervised machine learning** to provide actionable insights for financial institutions.

**Goals:**  
- Detect suspicious or high-value transactions (potential fraud).  
- Analyze transaction trends over hours, days, and merchants.  
- Classify transactions accurately by type.  
- Provide insights for **risk management**, **fraud detection**, and **business optimization**.

---

## Dataset

The dataset (`financial_anomaly_data.csv`) includes:

| Column Name      | Description |
|-----------------|-------------|
| Timestamp        | Date and time of the transaction |
| Amount           | Transaction amount |
| AccountID        | Customer or account identifier |
| Merchant         | Merchant name |
| TransactionType  | Type of transaction (e.g., Purchase, Refund) |
| Location         | Location of transaction |

---

## Project Workflow


### 1. Data Cleaning & Feature Engineering
- Convert timestamps to `datetime` format.  
- Extract features: `Hour`, `DayOfWeek`, `IsWeekend`.  
- Encode categorical variables: `Merchant_enc`, `TransactionType_enc`, `Location_enc`.

### 2. SQL-based KPI Analysis
- Total transaction volume  
- Average spend per transaction  
- Top 5 accounts by spend  
- Revenue concentration among top 10 merchants  
- Peak hour activity

### 3. Data Visualization
- **Heatmaps:** Transaction counts by hour and day  
- **Scatterplots:** Transaction amount vs hour  
- **Barplots:** Revenue by merchant  
- **Countplots:** Transaction distribution by hour and type

### 4. Anomaly Detection
- **Statistical Rule:** Transactions with `Amount > mean + 2*std` flagged as high-value anomalies  
- **Clustering:** KMeans clustering used to detect distance-based anomalies  
- Top 5% of transactions flagged as unusual  

### 5. Transaction Type Classification
- **Model:** Random Forest classifier  
- **Features:** `Amount`, `Hour`, `DayOfWeek`, `Merchant_enc`, `Location_enc`  
- **Accuracy:** ~87%

**Example Code:**
```python
clf = RandomForestClassifier(n_estimators=100, random_state=42)
clf.fit(X_train, y_train)


