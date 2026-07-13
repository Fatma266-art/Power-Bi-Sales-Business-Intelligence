# 📊 Sales & Business Intelligence Dashboard

> Multi-page Power BI report — AdventureWorks 2022

---

## 📌 Project Overview

An end-to-end Business Intelligence report built in Power BI, analyzing sales performance, customer behavior, product trends, and regional territories using the AdventureWorks 2022 dataset.

**Type:** Independent / Portfolio Project  
**Tool:** Microsoft Power BI Desktop  
**Faculty:** Artificial Intelligence, Menoufia University

---

## 📁 Project Structure

```
Power BI/
├── Sales & Business Intelligence.pbix    # Main Power BI report file
└── [screenshots].jpeg                    # Dashboard preview images
```

---

## 📋 Report Pages

| Page | Focus |
|------|-------|
| 1 | Executive Summary — top-level KPIs |
| 2 | Sales Analysis — revenue trends, YoY comparison |
| 3 | Customer Analysis — segments, top customers, RFM behavior |
| 4 | Product Analysis — top performers, category breakdown |
| 5 | Territory Analysis — regional map, geographic performance |

---

## 🗃️ Dataset — AdventureWorks 2022

A Microsoft sample database simulating a bicycle manufacturing company.

| Table | Description |
|-------|-------------|
| Sales | Order transactions with dates, quantities, amounts |
| Customers | Demographics, location, purchase history |
| Products | Categories, subcategories, pricing |
| Territories | Regions, countries, sales zones |
| Calendar | Date dimension for time intelligence |

---

## 🔧 Data Modeling

- **Schema type:** Star Schema
- **Relationships:** Fact table (Sales) linked to dimension tables via foreign keys
- **Date table:** Custom Calendar table for time intelligence functions

---

## 📐 Key DAX Measures

```dax
-- Total Revenue
Total Revenue = SUMX(Sales, Sales[OrderQty] * Sales[UnitPrice])

-- YoY Growth
YoY Growth % = DIVIDE([Total Revenue] - [Revenue LY], [Revenue LY])

-- Revenue Last Year
Revenue LY = CALCULATE([Total Revenue], SAMEPERIODLASTYEAR('Calendar'[Date]))

-- Customer Count
Active Customers = DISTINCTCOUNT(Sales[CustomerID])

-- Average Order Value
Avg Order Value = DIVIDE([Total Revenue], COUNTROWS(Sales))
```

---

## 📊 Visualizations Used

- KPI cards (revenue, orders, customers, profit margin)
- Line charts (monthly/yearly trends)
- Bar & clustered column charts (product/category comparisons)
- Map visual (territory performance)
- Matrix table (product × region breakdown)
- Donut charts (category distribution)
- Slicers (year, region, product category)

---

## ▶️ How to Open

1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Open `Sales & Business Intelligence.pbix`
3. Use slicers to filter by year, region, or product category

---

## 🛠️ Tech Stack

`Power BI Desktop` · `DAX` · `Star Schema Data Modeling` · `AdventureWorks 2022`
