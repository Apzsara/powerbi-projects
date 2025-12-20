# Fraud Risk & Transaction Health Dashboard

**Tools:** Python, SQL (MySQL), Power BI  
**Domain:** Financial Transactions & Fraud Analytics

---

## Overview
This project analyzes **13M financial transactions ($706.87M)** from **2010–2019** to identify fraud patterns, high-risk customer segments, and merchant categories driving fraud losses.

The dashboard defaults to the **latest available year (2019)**, reflecting real-world reporting practices.  
All KPIs and insights referenced below are based on the **2019 view**, while the full dataset is retained for historical analysis.

The focus is on **loss-based fraud prioritization**, rather than relying on fraud rate alone.

---

## Business Objectives
- Identify where fraud is concentrated across customers, merchants, and transaction types  
- Highlight high-risk customer segments for proactive monitoring  
- Support data-driven allocation of fraud prevention resources  

---

## Dashboard Highlights

### Key KPIs (2019 View)
KPI cards dynamically respond to Card Type and Transaction Type selections.

- **Total Transaction Value:** $61.16M  
- **Fraud Rate:** 0.12% (↑ 0.01% YoY)  
- **Fraud Loss:** $128K (↑ 10% YoY)  
- **High-Risk Customers:** 442 (~37% of 2019 customer base)  
- **Avg Fraud Transaction:** $94 (1.8× normal transaction)

---

## Core Visuals

### Fraud Rate by Transaction Amount
- Transactions **$300+** show the highest fraud rate (**0.60%**)  
- This segment drives **42% of total fraud loss ($54K)**

### Fraud Rate vs Fraud Loss by Card Type
- **Credit cards** have the highest fraud rate (**0.16%**)  
- **Debit cards** generate higher total fraud losses (**$66K**), despite a lower fraud rate

### Customer Risk Matrix
- Scatter plot of customers by **Debt-to-Income ratio vs Credit Score**
- Highlights **442 high-risk customers** clustered in the critical risk zone

### Top Fraud Loss by Merchant Category
- **Department Stores** lead with **$26K (20%)** of total fraud loss  
- Top three categories contribute **38% of total fraud losses**

---

## Key Insights
- Fraud losses are highly concentrated, with **38% driven by three merchant categories**
- **37% of customers in 2019** fall into a critical risk segment
- Highest fraud rate does not equate to highest financial impact
- **$300+ transactions** represent the highest fraud exposure

---

## Recommended Actions
- Prioritize monitoring for **Department Stores** ($26K loss, 20% of total)
- Flag **$300+ transactions** (42% of fraud loss, 0.60% fraud rate)
- Proactively review **442 high-risk customers** (high DTI + low credit score)
- Reallocate fraud prevention focus from **Credit to Debit cards** based on loss volume

---

## Technical Workflow

### Python (Pandas)
- Data cleaning and validation across core datasets  
- Merged fraud labels and merchant category mappings  
- Feature engineering focused on:
  - Debt-to-Income ratio  
  - Transaction type classification (debit, refund)
  - Transaction date attributes (year, month)

### SQL (MySQL)
- Joined customer, card, and transaction tables into a single enriched dataset (13M+ rows)
- Resolved merchant location data quality issues
- Created aggregated views for Power BI performance optimization

### Power BI & DAX
- Dynamic KPIs using `SWITCH` for amount bucketing and metric logic
- Year-over-Year analysis using `SAMEPERIODLASTYEAR`
- Risk segmentation using `CALCULATE` and `FILTER`
- Percentage calculations using `DIVIDE`

---

## Files Included
- `screenshots/` — Dashboard preview images  
- **PBIX File:** [Download here](https://drive.google.com/file/d/1x7qqMFZzxFh84mV8_W4GOmnB9DRVPFxs/view?usp=drive_link)

> Note: The PBIX file is hosted externally due to file size constraints.

---

## Dataset Notes
- `user.csv` — customer attributes  
- `card.csv` — card-level details  
- `transaction.csv` — transaction-level data  
- `fraud_labels.json` — fraud indicators  
- `mcc.json` — merchant category mappings  

All datasets were cleaned, validated, and enriched prior to analysis.
