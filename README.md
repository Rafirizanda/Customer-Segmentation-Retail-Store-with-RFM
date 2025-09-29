# 🛍️ Customer Segmentation – Online Retail

This project focuses on **customer segmentation** using the **Online Retail Dataset** from [Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset).  
The main objective is to group customers based on their **Recency, Frequency, and Monetary (RFM) behavior** to better understand their purchasing preferences and revenue contribution.

---

## 📌 Problem Statement
The challenge is to **identify and segment customers** in order to:  
- Understand purchasing behavior.  
- Identify high-value and at-risk customers.  
- Provide insights for targeted marketing strategies.  

---

## 🗂️ Dataset Overview
- **Source:** [Online Retail Dataset – Kaggle](https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset)  
- **Size:** ~500k rows  
- **Features:** CustomerID, InvoiceNo, StockCode, Quantity, UnitPrice, InvoiceDate, Country  

---

## ⚙️ Data Preprocessing
Steps performed:
1. **Handling missing values** → Removed rows with null `CustomerID`.  
2. **Duplicate removal** → Dropped duplicate transactions.  
3. **Filtering transactions** → Removed canceled orders and negative quantities.  
4. **Feature engineering** → Calculated RFM metrics:  
   - **Recency:** Days since last purchase  
   - **Frequency:** Number of transactions  
   - **Monetary:** Total revenue  

---

## 📊 RFM Analysis
- Generated **RFM table** for each customer.  
- Applied **K-Means clustering** to group customers into 4 segments.  

### RFM Segments Identified
- **Cluster 0 – Medium Value Customers:**  
  Average spending is moderate, consistent purchase frequency. (~3876 customers)  
- **Cluster 1 – At Risk Customers:**  
  Customers with long inactivity and low engagement. (~1998 customers)  
- **Cluster 2 – High Value Customers:**  
  Loyal customers with very high spending and frequent purchases. (very small segment)  
- **Cluster 3 – Active Customers with High Frequency:**  
  Recently active customers with high purchase frequency. (~35 customers)  

---

## 📈 Visualization & Insights
- **Barplot:** Distribution of customers per cluster.  
- **Boxplots:** Showed differences in Recency, Frequency, and Monetary values by segment.  
- **Heatmap (Z-score):** Compared cluster behavior against the average population.  
- **Pie Chart:** Customer distribution across segments (65.9% Medium Value, 34% At Risk, 0.1% Low Value).  

---

## ✅ Business Insights
1. **High Value Customers** should be rewarded with loyalty programs or exclusive offers.  
2. **At Risk Customers** need re-engagement campaigns (e.g., discounts, personalized offers).  
3. **Medium Value Customers** represent the majority – strategies should aim to **increase frequency** of purchases.  
4. **Low Value Customers** are negligible in count and revenue impact.  

---

## 📦 Tech Stack
- **Python**  
- **Pandas, NumPy** – Data cleaning & preprocessing  
- **Matplotlib, Seaborn** – Data visualization  
- **Scikit-learn** – K-Means clustering  
- **Jupyter Notebook** – Development  
