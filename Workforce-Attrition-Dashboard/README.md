# Workforce Attrition Dashboard – Power BI

## 🔍 Overview
This **Power BI dashboard** explores employee attrition across multiple dimensions including **tenure, job roles, satisfaction levels, and demographics**.  
**Purpose:** To help HR teams **identify top attrition drivers and focus retention efforts on high-risk employees**.

---

## 📊 Dashboard Contents

**KPI Cards**
- **Total Employees**
- **Average Salary**
- **Attrition Rate:** 16.12%
- **Average Tenure:** 7.01 months

**Visuals**
- **Area Chart:** Attrition by Tenure
- **Vertical Bar Chart:** Attrition by Job Satisfaction Level
- **Horizontal Bar Chart:** Attrition Rate by Job Role (**top 3 high-attrition roles highlighted in red**)
- **Horizontal Bar Chart:** Attrition by Gender

**Filters & Interactivity**
- **Page-level slicer:** Department
- **Visual-level filtering:** Clicking on charts dynamically updates related visuals

---

## ⚙️ Tools & Features Used

**Power BI Desktop**
- KPI Cards, Interactive Charts, Conditional Formatting, Scrollable Visuals
- **DAX Measures:** CALCULATE, FILTER, DIVIDE, COUNTROWS, DISTINCTCOUNT, SWITCH (used to calculate tenure bands, average salary, attrition metrics, and role-specific insights)

**Python (Pandas)**
- Data cleaning: Removed redundant and constant columns to ensure accurate metrics

**Other Features**
- Custom measures for KPIs
- Tooltips and data labels for clarity
- Optimized layout for fast insights

---

## 💡 Key Insights & Impact
- Dashboard highlights **top 3 high-attrition roles**, allowing HR to **prioritize retention actions**.  
- **Top 1 high-attrition role:** Sales Representative — mostly males with **low job satisfaction** and **low tenure**.  
- Provides department-wise and role-wise trends to **identify drivers of attrition** such as tenure, satisfaction, and job role.  
- Helps HR teams **quickly spot patterns** by gender, tenure, and satisfaction levels for **data-driven decision-making**.

---

## 📂 Files Included
- `WorkforceAttritionDashboard.pbix` – Power BI file
- `screenshots/` – Preview images of dashboard pages
- `README.md` – This file

---

## 📌 Dataset Note
- The dataset is a **realistic HR sample** including fields like **Job Role, Tenure, Salary, Job Satisfaction, Attrition status, Department, Gender**, and other employee demographic attributes.
