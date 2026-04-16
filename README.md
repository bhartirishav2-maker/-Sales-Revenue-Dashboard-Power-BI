# 📊 Sales & Revenue Dashboard — Power BI

> An end-to-end Sales & Revenue Analytics Dashboard built in Power BI, featuring 3,000+ transaction records across regions, categories, sales reps, and channels for FY 2023–2024
---

## 📌 Project Overview

This project demonstrates a complete business intelligence workflow — from synthetic data generation to an interactive, multi-visual Power BI dashboard — designed to surface actionable sales insights for stakeholders.

**Domain:** Retail / Sales Analytics  
**Tool:** Microsoft Power BI Desktop  
**Dataset:** Synthetic (3,000 rows | 21 columns)  
**Period:** January 2023 – December 2024  

---

## 🎯 Key KPIs Tracked

| Metric | Value |
|---|---|
| Total Net Sales | ₹286.45M |
| Gross Profit | ₹113.53M |
| Profit Margin % | 40.6% |
| Target Achievement % | 96.8% |
| Total Orders | 3,000 |

---

## 📊 Visuals Included

- **KPI Cards** — Net Sales, Gross Profit, Profit Margin, Target Achievement, Total Orders
- **Line + Area Chart** — Monthly Revenue vs Target (Jan 2023 – Dec 2024)
- **Donut Chart** — Sales by Category (Electronics, Furniture, Clothing, F&B, Sports)
- **Horizontal Bar Chart** — Sales by Region (North, South, East, West, Central)
- **Table Visual** — Top Sales Reps with Target Achievement %
- **100% Stacked Bar** — Channel Mix by Category (Online, Retail, Wholesale, Direct)

---

## 🗂️ Dataset Columns

| Column | Description |
|---|---|
| Order_ID, Order_Date | Transaction identity & date |
| Month, Quarter, Year | Time intelligence fields |
| Region, City | Geographic breakdown |
| Sales_Rep | Individual rep performance |
| Category, Sub_Category | Product hierarchy (2 levels) |
| Channel, Payment_Mode | Sales channel & payment split |
| Unit_Price, Quantity | Volume & pricing data |
| Discount_%, Discount_Amount | Discount impact tracking |
| Net_Sales, COGS, Gross_Profit | Core P&L metrics |
| Sales_Target | Actual vs target comparison |

---

## 🔧 DAX Measures Used

```dax
-- Total Net Sales
Total Net Sales = SUM(Sales_Data[Net_Sales])

-- Gross Profit Margin
Profit Margin % = DIVIDE(SUM(Sales_Data[Gross_Profit]), SUM(Sales_Data[Net_Sales]))

-- YoY Growth
YoY Growth % = 
VAR CurrentYear = SUM(Sales_Data[Net_Sales])
VAR LastYear = CALCULATE(SUM(Sales_Data[Net_Sales]), SAMEPERIODLASTYEAR(Sales_Data[Order_Date]))
RETURN DIVIDE(CurrentYear - LastYear, LastYear)

-- Target Achievement
Target Achievement % = DIVIDE(SUM(Sales_Data[Net_Sales]), SUM(Sales_Data[Sales_Target]))

-- Channel Contribution %
Channel % = DIVIDE(SUM(Sales_Data[Net_Sales]), CALCULATE(SUM(Sales_Data[Net_Sales]), ALL(Sales_Data[Channel])))
```

---

## 📁 Files in This Repository

```
📦 sales-revenue-dashboard-powerbi
 ┣ 📊 Sales_Revenue_Dataset.xlsx     ← Raw dataset (3,000 rows)
 ┣ 📄 Sales_Revenue_Dashboard.pbix   ← Power BI dashboard file
 ┣ 🖼️ dashboard_preview.png          ← Dashboard screenshot
 ┗ 📝 README.md

---

## 🛠️ Tools & Skills

`Power BI Desktop` `DAX` `Data Modelling` `Excel` `Data Visualization` `Business Intelligence`

---

## 👤 Author

**Rishav Bharti**  
Aspiring Data Analyst | IIT Roorkee Certified  
📍 Gurugram, Haryana, India  
🔗 [LinkedIn](https://www.linkedin.com/in/rishav-bharti-2b2630245/)

---

## ⭐ If you found this useful, consider starring the repo!
