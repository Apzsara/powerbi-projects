# Fraud Risk & Transaction Health Dashboard

**Tools:** Python, SQL (MySQL), Power BI  
**Domain:** Financial Transactions & Fraud Analytics

---

## Overview

This project analyzes **13M financial transactions ($706.87M)** from **2010–2019** to identify fraud patterns, high-risk customer segments, and merchant categories driving fraud losses.

The dashboard supports fraud and risk teams by enabling loss-based prioritization instead of relying on fraud rate alone.

---

## Business Objective

- Identify where fraud is concentrated across customers, merchants, and transaction types  
- Highlight high-risk customer segments for proactive monitoring  
- Support data-driven allocation of fraud prevention resources  

---

## Dashboard Highlights

### Key KPIs

KPI cards dynamically switch context based on **Card Type** or **Transaction Type** selection:

- Total Transaction Value: $61.16M (2019 view)
- Fraud Rate: 0.12% (↑ 0.01% YoY)
- Fraud Loss: $128K (↑ 10% YoY)
- High-Risk Customers: 442 (17% of customer base)
- Avg Fraud Transaction: $94 (1.8x normal)

---

### Core Visuals

**Fraud Rate by Transaction Amount**  
$100–$200 range shows the highest fraud concentration (~5x vs sub-$100)

**Fraud Rate vs Fraud Loss by Card Type**  
Credit cards have the highest fraud rate, while Debit cards generate 3.6x higher fraud losses

**Customer Risk Matrix**  
Scatter plot of customers by Debt-to-Income ratio vs Credit Score, highlighting 442 high-risk customers

**Top Fraud Loss by Merchant Category**  
Department Stores account for $24K in fraud losses; top 3 categories contribute 38% of total fraud

---

## Key Insights

- 38% of fraud losses come from just 3 merchant categories
- 17% of customers fall into a critical risk segment
- Highest fraud rate does not equal highest financial impact
- $100–$200 transactions present elevated fraud exposure

---

## Recommended Actions

- Prioritize fraud monitoring for Department Stores ($24K loss, 38% of total fraud)
- Apply step-up verification for Debit card transactions in the $100–$200 range
- Flag 442 high-risk customers (high DTI + low credit score) for proactive reviews
- Reallocate fraud prevention resources from Credit to Debit cards based on loss volume

---

## Technical Workflow

### Python (Pandas)

- Data cleaning and validation across 3 core CSV files
- Merged `fraud_labels.json` and `mcc.json` into transaction data
- Feature engineering:
  - Debt-to-Income ratio
  - Customer retirement status flag (`already_retired`)
  - Transaction date features (year, month)
  - Transaction type classification (debit, refund) derived from amount sign

---

### SQL (MySQL)

- Joined customer, card, and transaction tables into a single enriched dataset (13M+ rows)
- Resolved data quality issue where merchant location fields mixed U.S. abbreviations with country names
- Created aggregated views for Power BI performance optimization

---

### Power BI & DAX

- Dynamic KPIs using `SWITCH` for parameter-based card/transaction type switching
- Year-over-Year analysis using `SAMEPERIODLASTYEAR`
- Risk segmentation with `CALCULATE` and `FILTER`
- Safe percentage calculations using `DIVIDE`

---

## Files Included

- `screenshots/` — Dashboard preview images
- `Fraud_Risk_Dashboard.pbix` — Power BI file

---

## Dataset Notes

- `user.csv` — customer attributes
- `card.csv` — card-level details
- `transaction.csv` — transaction-level data
- `fraud_labels.json` — fraud indicators
- `mcc.json` — merchant category mappings

All datasets were cleaned, validated, and enriched prior to analysis.
