# 📊 Customer Lifetime Value (LTV) Prediction Model

## 📌 Project Overview
Customer Lifetime Value (LTV) is a key business metric that estimates the total revenue a business can expect from a customer over the entire relationship.  
This project builds a **machine learning regression model** to predict customer LTV based on historical purchase behavior and segments customers for targeted marketing strategies.

---

## 🎯 Objective
- Predict **Customer Lifetime Value (LTV)** using transaction history  
- Engineer meaningful customer features (Recency, Frequency, AOV)  
- Train and evaluate regression models  
- Segment customers based on predicted LTV  
- Generate a final LTV prediction dataset for business use  

---

## 🧰 Tools & Technologies
- **Platform:** Google Colab  
- **Programming Language:** Python  
- **Libraries:**  
  - pandas  
  - numpy  
  - scikit-learn  
  - xgboost  
  - matplotlib  
  - seaborn  

---

## 📂 Dataset
- **Source:** Kaggle  
- **Recommended Dataset:** Online Retail II (UCI)  
- **Description:**  
  Transaction-level e-commerce data containing customer purchases, order dates, quantities, and prices.

### Key Columns Used
- `CustomerID`
- `OrderID / InvoiceNo`
- `OrderDate / InvoiceDate`
- `OrderValue` (derived from Quantity × Price)

---

## 🔁 Project Workflow

### 1️⃣ Data Preprocessing
- Load transaction data  
- Handle missing values and invalid records  
- Convert date columns to datetime format  
- Remove canceled or negative-value transactions  

---

### 2️⃣ Feature Engineering
Customer-level features are created using **RFM methodology**:
- **Recency:** Days since last purchase  
- **Frequency:** Number of purchases  
- **AOV (Average Order Value):** Average spend per order  
- **Total Spend:** Historical customer value  

---

### 3️⃣ Target Variable
- **LTV:** Historical total spend per customer  
  (Used as a proxy for customer lifetime value)

---

### 4️⃣ Model Building
- Split data into training and testing sets  
- Train regression models:
  - XGBoost Regressor  
  - Random Forest Regressor (optional)  

---

### 5️⃣ Model Evaluation
Performance is evaluated using:
- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**

---

### 6️⃣ LTV Prediction
- Predict LTV for all customers  
- Store predictions in a structured dataset  

---

### 7️⃣ Customer Segmentation
Customers are segmented based on predicted LTV:
- **Low Value**
- **Mid Value**
- **High Value**
- **VIP Customers**

These segments support targeted marketing and retention strategies.

---

## 📊 Visualizations
- LTV distribution  
- Customer segment comparison  
- Boxplots for predicted LTV across segments  

---

## 📁 Deliverables
- 📓 Google Colab Notebook (`.ipynb`)  
- 📈 Model evaluation metrics & visualizations  
- 📄 Final LTV prediction dataset (`Final_LTV_Predictions.csv`)  

---

## 📌 Business Use Cases
- Personalized marketing campaigns  
- Customer retention strategies  
- Loyalty program optimization  
- Revenue forecasting  

---

## 🚀 How to Run the Project

1. Open **Google Colab**
2. Upload the dataset or connect Kaggle API
3. Install required libraries:
   ```bash
   pip install xgboost
