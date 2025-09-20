# 💰 Financial Transaction Analysis & Anomaly Detection

[![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python&logoColor=white)](https://www.python.org/)
[![SQLite](https://img.shields.io/badge/Database-SQLite-lightgrey?logo=sqlite&logoColor=white)](https://www.sqlite.org/index.html)
[![Scikit-learn](https://img.shields.io/badge/ML-Scikit--learn-orange?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

**End-to-end financial transaction analysis with KPI extraction, anomaly detection, clustering, and classification using Python, SQL, and machine learning.**

---

## 🚀 Project Overview

This project analyzes **financial transaction data** to extract insights, detect anomalies, cluster patterns, and classify transaction types.  

It combines:
- **Data Cleaning & Feature Engineering**  
- **SQL-based KPI Extraction**  
- **Data Visualization**  
- **Unsupervised Clustering (KMeans)**  
- **Supervised Machine Learning (Random Forest)**  

**Goals:**  
- Detect suspicious or high-value transactions (potential fraud) 🕵️‍♂️  
- Analyze transaction trends over hours, days, and merchants 📊  
- Classify transactions accurately by type 🤖  
- Provide actionable insights for **risk management** and **business optimization** 💡

---

## 📂 Dataset

The dataset (`financial_anomaly_data.csv`) contains:

| Column Name      | Description |
|-----------------|-------------|
| `Timestamp`        | Date and time of the transaction |
| `Amount`           | Transaction amount |
| `AccountID`        | Customer or account identifier |
| `Merchant`         | Merchant name |
| `TransactionType`  | Type of transaction (e.g., Purchase, Refund) |
| `Location`         | Location of transaction |

---

## 🛠️ Project Workflow

### 1️⃣ Data Cleaning & Feature Engineering
- Convert timestamps to `datetime`.  
- Extract features: `Hour`, `DayOfWeek`, `IsWeekend`.  
- Encode categorical variables: `Merchant_enc`, `TransactionType_enc`, `Location_enc`.  

### 2️⃣ SQL-based KPI Analysis
- Total transaction volume 💵  
- Average spend per transaction 💳  
- Top 5 accounts by spend 🏆  
- Revenue concentration among top 10 merchants 🏬  
- Peak hour activity ⏰

### 3️⃣ Data Visualization
- **Heatmaps:** Transaction counts by hour & day 🔥  
- **Scatterplots:** Transaction amount vs hour 📈  
- **Barplots:** Revenue by merchant 💰  
- **Countplots:** Transaction distribution by hour & type 🧮

### 4️⃣ Anomaly Detection
- **Statistical Rule:** `Amount > mean + 2*std` flagged as anomalies ⚠️  
- **Clustering:** KMeans detects distance-based anomalies  
- Top 5% of transactions flagged as unusual 🕵️‍♀️  

### 5️⃣ Transaction Type Classification
- **Model:** Random Forest Classifier 🌲  
- **Features:** `Amount`, `Hour`, `DayOfWeek`, `Merchant_enc`, `Location_enc`  
- **Accuracy:** ~87% ✅

## 📊 Key Findings

- **Anomalies Detected:** Top 5% transactions flagged as unusual ⚠️  
- **High-Risk Accounts:** Accounts with repeated high-value anomalies identified 🔝  
- **Peak Hours:** Most transactions occur between 8 AM – 3 PM ⏱️  
- **Revenue Concentration:** Few merchants contribute the majority of revenue 💵  
- **Classification Performance:** Random Forest achieved high precision, recall & F1-score 🏅  

## 💡 Use Cases

- **Fraud Detection & Prevention** – Quickly identify suspicious transactions 🛡️  
- **Customer Behavior Analysis** – Understand transaction patterns and peak hours 👥  
- **Merchant Performance Evaluation** – Identify high-revenue merchants 📊  
- **Risk Management & Operational Planning** – Make data-driven decisions 📈
