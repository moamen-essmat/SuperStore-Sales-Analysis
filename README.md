# SuperStore Global Sales Analytics Dashboard 🛒📊

An enterprise-grade, interactive Power BI dashboard engineered to monitor, analyze, and optimize global retail sales performance. This project models complex business data to extract key performance indicators (KPIs), track regional distributions, evaluate sub-category profitability, and implement advanced dynamic user-centric filters.

🔗 **[Live Interactive Report Link]** *(Optional: Add your Power BI Service Publish to Web link here if available)*

---

## 🚀 Business Value & Key Insights
* **High-Level Financials:** Generated **$11.17M** in total revenue from **5.009K orders**, maintaining a stable profit margin of **2.57%** ($286.40K total profit).
* **Return Rate Warning:** Tracked **296 returned orders**. (*Pro Tip: This can be utilized to build a risk mitigation strategy for low-performing product segments*).
* **Product Segment Dominance:** The **Consumer segment** is the primary driver of revenue, contributing **$5.7M**, followed by Corporate ($3.4M) and Home Office ($2.1M).
* **Regional Performance:** The **West Region** leads company sales with **$3.50M**, closely followed by the East ($3.28M), while South requires strategic marketing focus ($1.98M).
* **Sub-Category Champions:** `Chairs` and `Phones` are the highest revenue-generating sub-categories, both crossing the $1M+ mark.

---

## 🛠️ Technical Implementation & Architecture

### 1. Advanced DAX & Dynamic Context
* **Dynamic Formatting Cards:** Implemented dynamic KPI cards at the top that react instantly to combinations of Year (`2016-2019`), Month, and Category selections.
* **User & Security Context:** Integrated user environment tracking metrics (`DESKTOP-BVV10T0\Admin`) via DAX security functions to lay groundwork for Row-Level Security (RLS) by region/manager.
* **Conditional Error Handling:** Utilized `HASONEVALUE()` inside DAX measures to prevent card breakages (e.g., handling the "Multiple Categories" fallback gracefully when no single filter context is active).

### 2. Relational Data Modeling (Star Schema)
The architecture follows a clean Star Schema utilizing:
* **Fact Table:** `Orders` (Containing price, quantities, discounts, and core financial attributes).
* **Dimension Tables:** `DateTable` (Time-Intelligence), `People` (Regional Managers), and `Returns` (Product Return flags).

---

## 📸 Dashboard Previews

### 1. Executive Summary Page
*A unified operational view highlighting chronological sales growth trends (2016 to 2019), geographical breakdown, ship mode analysis, and a real-time customer leaderboard by revenue.*
![Executive Summary](images/executive_summary.png)

### 2. Dynamic Performance & RLS Audit Page
*An analytical deep-dive built to test filter boundaries, measure cross-filtering across regions, and manage active directory domain user logging attributes.*
![Dynamic Insights](images/dynamic_insights.png)

---

## 💡 Professional Enhancements Added (Best Practices)
* **Granular Drill-Downs:** Enabled continuous trend analysis on the "Sum of Amount by Year" chart, showing the exponential jump from $2.32M (2017) to $3.48M (2019).
* **Data Profiling:** Applied Power Query best practices to eliminate null values, fix zip/postal code data types, and cleanly merge dimensional boundaries.

---

## ⚙️ How to Explore This Project
1. Clone this repository.
2. Open `SuperStore_Sales_Dashboard.pbix` using Power BI Desktop.
3. Inspect the `Data` pane to see the structured measure folders and calculated date dimensions.

---
💡 *Developed as part of my Data Analytics portfolio. Connect with me on [LinkedIn](https://linkedin.com/in/moamenessmat).*
