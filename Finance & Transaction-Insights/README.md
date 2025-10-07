# Finance & Transaction-Insights

## Overview
This dashboard uncovers actionable insights from **13M financial transactions**, highlighting trends, customer behavior, card usage, and fraud patterns. Built with **Python**, **SQL**, and **Power BI**, it combines data preparation, aggregation, and DAX-driven visualization for a full end-to-end analytics workflow.

## Data Sources
- `user.csv` – user/customer dataset  
- `card.csv` – card dataset  
- `transaction.csv` – transaction dataset  
- `fraud_labels.json` – mapping of transaction IDs to fraud status  
- `mcc.json` – mapping of MCC codes to descriptions  

## Key Insights
- **Transaction Volume:** 13M transactions, total amount transacted \$706.87M  
- **Transaction Type:** Swipe (7M) > Chip (5M) > Online (2M)  
- **Fraud Patterns:** Only 0.1% of transactions are fraudulent; top MCC: Computer & Peripherals, top region: Tuvalu  
- **Customer Behavior:** Most active age group: 45–54; credit cards dominate across all age groups  
- **Financial Health:** Credit score vs. debt-to-income ratio shows higher-value transactions mostly from credit and debit cardholders  

## Features
- **Trend Analysis:** Yearly transaction trends  
- **Transaction Type Comparison:** Swipe, Chip, Online  
- **Customer Insights:** Age groups, card types, credit score vs. debt-to-income ratio  
- **Fraud Insights:** MCC and region-wise fraudulent transactions  
- **KPI Overview:** Total transactions, total customers, total cards, total transaction amount, average credit limit, fraud %  

## Tech Stack
- **Python:** Data handling and feature engineering  
- **MySQL:** Aggregations and table joins  
- **Power BI:** Interactive visualizations and DAX calculations  

## How It Works
1. **Prepare Data:** Use CSVs and JSONs (`user.csv`, `card.csv`, `transaction.csv`, `fraud_labels.json`, `mcc.json`)  
2. **SQL Aggregation:** Import datasets into MySQL, create enriched tables  
3. **Power BI:** Connect to enriched tables, create KPIs, charts, slicers, and dashboards
