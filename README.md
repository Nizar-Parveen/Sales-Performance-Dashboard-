# Sales-Performance-Dashboard
Analyze company sales data to track monthly revenue, top products, and region-wise performance (Excel + SQL)

## 🔹 Project Overview

This project analyzes a large-scale sales dataset (~10,000 records) to generate meaningful business insights. The goal is to track **monthly revenue, top-performing products, and regional performance** using SQL and Excel.

An interactive Excel dashboard is built to help stakeholders make data-driven decisions.

---

## 🎯 Objectives

* Analyze sales data to identify trends and patterns
* Track monthly revenue performance
* Identify top-selling products
* Compare sales across different regions and categories
* Build an interactive business dashboard

---

## 🛠 Tools & Technologies

* **Microsoft Excel** (Data Cleaning, Pivot Tables, Dashboard)
* **MySQL Workbench** (Data Storage & Querying)
* **CSV Dataset** (~10,000 rows)

---

## 📂 Dataset Description

The dataset contains the following fields:

* OrderID
* OrderDate
* Product
* Category
* Region
* Quantity
* UnitPrice
* TotalSales
* Month

---

## 🧹 Data Cleaning (Excel)

* Removed duplicate records using OrderID
* Handled missing values (Quantity, UnitPrice)
* Standardized date format
* Created calculated columns:

  * **TotalSales = Quantity × UnitPrice**
  * **Month = TEXT(OrderDate, "mmm-yyyy")**

---

## 🗄 Data Processing (MySQL)

* Imported cleaned CSV into MySQL database
* Created structured table for analysis
* Performed SQL queries to extract insights

### Key SQL Queries

#### 📅 Monthly Revenue

```sql
SELECT Month,
       SUM(TotalSales) AS MonthlyRevenue
FROM sales
GROUP BY Month
ORDER BY Month;
```

#### 🏆 Top Products

```sql
SELECT Product,
       SUM(TotalSales) AS Revenue
FROM sales
GROUP BY Product
ORDER BY Revenue DESC
LIMIT 10;
```

#### 🌍 Region-wise Sales

```sql
SELECT Region,
       SUM(TotalSales) AS Revenue
FROM sales
GROUP BY Region;
```

#### 📦 Category Performance

```sql
SELECT Category,
       SUM(TotalSales) AS Revenue
FROM sales
GROUP BY Category;
```

---

## 📊 Dashboard Features (Excel)

* 📈 Monthly Revenue Trend (Line Chart)
* 📊 Top Products (Column Chart)
* 🥧 Region-wise Distribution (Pie Chart)
* 🎛 Interactive Slicers:

  * Region
  * Month
  * Product

---

## 💡 Key Insights

* Identified high-performing products contributing maximum revenue
* Analyzed monthly sales trends for business planning
* Compared regional performance to support strategic decisions

---

## 🏆 Outcome

* Built a **business-ready interactive dashboard**
* Improved data analysis skills using **Excel + SQL**
* Gained hands-on experience with real-world dataset

---

## 📌 How to Use

1. Open the Excel dashboard file
2. Use slicers to filter by Region, Month, or Product
3. Analyze charts for insights

---

## 🚀 Future Improvements

* Add KPI cards (Total Revenue, Best Product, Best Region)
* Automate data refresh using Power Query
* Build dashboard in Power BI for advanced visualization

---


---
