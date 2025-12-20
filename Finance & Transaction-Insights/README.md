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

**1. Fraud Rate by Transaction Amount**  
Transactions $300+ show the highest fraud rate (0.60%) and drive **42% ($54K)** of total fraud loss

**2. Fraud Rate vs Fraud Loss by Card Type**  
Credit cards have the highest fraud rate (0.16%), while Debit cards generate **$66K** in fraud losses

**3. Customer Risk Matrix**  
Scatter plot of customers by Debt-to-Income ratio vs Credit Score, highlighting **442 high-risk customers** in the critical risk zone

**4. Top Fraud Loss by Merchant Category**  
Department Stores lead with **$26K (20% of total)**; top 3 categories (Dept Stores, Furniture, Gardening Supplies) contribute **38% of total fraud**

---

## Key Insights

- Top 3 merchant categories drive **38% of fraud losses**
- **17% of customers** fall into a critical risk segment (high DTI + low credit score)
- Highest fraud rate does not equal highest financial impact (Credit **0.16%** vs Debit **$66K** loss)
- Transactions **$300+** represent the highest fraud exposure (**0.60% rate**)

---

## Recommended Actions

- **Prioritize Department Stores:** $26K loss (20% of total fraud)
- **Flag $300+ transactions:** 42% of fraud loss ($54K) with 0.60% fraud rate
- **Monitor 442 high-risk customers:** Proactive reviews for high DTI + low credit score segment
- **Reallocate resources to Debit cards:** $66K loss despite lower fraud rate than Credit

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
- Custom formatting with `FORMAT`

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
