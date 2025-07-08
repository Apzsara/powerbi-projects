# Workforce Attrition Dashboard – Power BI

## 🔍 Overview
This Power BI dashboard explores employee attrition data across multiple dimensions including tenure, job roles, satisfaction levels, and demographics. The goal is to provide straightforward insights using clean visuals and meaningful metrics.

---

## 📊 Dashboard Contents

### KPI Cards
- Total Employees  
- Average Salary  
- Attrition Rate  
- Average Tenure  

### Visuals
- Area Chart: Attrition by Tenure  
- Vertical Bar Chart: Attrition by Job Satisfaction Level  
- Horizontal Bar Chart: Attrition Rate by Job Role (with conditional formatting)  
- Horizontal Bar Chart: Attrition by Gender  

### Filters
- **Page-level slicer**: Department  
- **Visual-level filtering**: Enabled through interactions (e.g., clicking a bar updates related charts)

---

## ⚙️ Tools & Features Used
- **Power BI Desktop**
- **Python (Pandas)** – Used for basic data cleaning  
- **DAX Measures**  
  - Examples: `CALCULATE`, `FILTER`, `DIVIDE`, `SUMX`  
- Conditional formatting (bar chart)  
- Custom measures for KPIs  
- Basic layout optimization  
- Tooltips and data labels where needed

---

## 📂 Files Included
- `WorkforceAttritionDashboard.pbix` – Power BI file  
- `screenshots/` – Preview images  
- `README.md` – This file  

---

## 📌 Note
The dataset used is sample HR data containing fields such as Job Role, Tenure, Salary, Job Satisfaction, and Attrition status.
