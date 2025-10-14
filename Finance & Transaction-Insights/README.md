# Finance & Transaction Insights Dashboard – Python, SQL, Power BI

## 🔍 Overview
This **dashboard uncovers actionable insights** from **13M financial transactions** totaling **$706.87M**, highlighting trends, customer behavior, card usage, and fraud patterns.  
Built with **Python, SQL, and Power BI**, it combines data preparation, aggregation, and **DAX-driven visualization** for a full end-to-end analytics workflow.  

**Purpose:** Enables finance teams to **monitor transaction trends, detect fraud, and make data-driven decisions**.

---

## 📊 Dashboard Contents

**KPI Cards**
- **Total Transactions:** 13M  
- **Total Customers:** 1,219  
- **Total Cards:** 4,071  
- **Total Transaction Amount:** $706.87M  
- **Average Credit Limit**  
- **Fraudulent Transactions %:** 0.1%

**Visuals**
- **Trend Analysis:** Yearly transaction trends  
- **Transaction Type Comparison:** Swipe (7M), Chip (5M), Online (2M)  
- **Customer Insights:** Age groups, card types, credit score vs. debt-to-income ratio  
- **Fraud Insights:** MCC and region-wise fraudulent transactions (**top MCC:** Cruise Lines 35.55%, **top region:** Tuvalu 100%)  

**Filters & Interactivity**
- **Page-level slicers:** Year, Transaction Type, Region  
- **Visual-level filtering:** Clicking on charts dynamically updates related visuals  

---

## ⚙️ Tools & Features Used

**Power BI Desktop**
- KPI Cards, Interactive Charts, Conditional Formatting, Scrollable Visuals  
- **DAX Measures:** CALCULATE, FILTER, DIVIDE, COUNTROWS, DISTINCTCOUNT, SWITCH (used for aggregated KPIs, trends, and fraud analysis)  

**Python (Pandas)**
- Data cleaning and feature engineering for accurate metrics  

**MySQL**
- Aggregations and table joins to create enriched datasets for faster insights  

---

## 💡 Key Insights & Impact
- **Fraud Analysis:** Only 0.1% of transactions are fraudulent; top MCC: Cruise Lines (35.55% of flagged transactions), top region: Tuvalu (100%).  
- **Customer Behavior:** Most active age group **45–54**; credit cards dominate across all age groups.  
- **Financial Health:** Higher-value transactions mostly come from credit and debit cardholders.  
- Provides finance teams with **quick monitoring of transaction trends** and **data-driven insights for risk management and operational strategy**.

---

## 📂 Files Included
- `screenshots/` – Preview images of the dashboard  
- `PBIX file` – [Download here](https://drive.google.com/drive/folders/1OsLVGbyhEhYopRQ7VWE_OR1Q_L5DQrpu?usp=sharing)   

---

## 📌 Dataset Note
- The datasets include **user.csv, card.csv, transaction.csv, fraud_labels.json, mcc.json**, representing **customer, card, transaction, and fraud mapping data**.



