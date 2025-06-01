# 📊 Consumer Report Global Dashboard – Power BI Project

## Overview

The **Consumer Report Global Dashboard** is a comprehensive Power BI report designed to provide actionable insights into global consumer sales performance. This interactive reporting solution enables stakeholders to monitor key performance indicators (KPIs), product metrics, and return trends across multiple dimensions—such as time, geography, and product hierarchies.

> Engineered for data-driven decision-making, the report seamlessly integrates analytical depth with visual clarity.

---

## 🧱 Data Model Schema

The data model follows a **snowflake schema**, emphasizing normalized dimension tables for modularity and clarity. It establishes **one-to-many relationships** between fact and dimension tables to support dynamic slicing, filtering, and detailed analysis.

### 🔹 Fact Tables

- **Sales Data**  
  Captures transaction-level details, including:
  - Order Date
  - Quantity
  - Retail Price
  - Product Key

- **Returns Data**  
  Records return metrics by:
  - Quantity Returned
  - Return Date
  - Product and Region

### 🔹 Dimension Tables

- **Calendar Lookup** – Enables date-based analysis (day, month, year).
- **Customer Lookup** – Contains customer attributes and priority levels.
- **Territory Lookup** – Maps regions and countries.
- **Product Lookup** – Contains detailed metadata (color, price, model).
- **Product Subcategories Lookup** – Defines subcategory relationships.
- **Product Categories Lookup** – Top-level product classification.

### 🔹 Measure Table

A centralized **"Sales" folder** contains all DAX measures, ensuring consistency, maintainability, and performance optimization.

> **Design Note:** This centralization supports modular development and simplifies debugging and auditing of KPIs.

---

## ⚙️ Storage Mode

- **Mode:** Import  
- **Engine:** Power BI VertiPaq (in-memory)  
- **Performance:** Optimized for fast querying and offline use

> **Dataset Limitations:**  
Power BI Desktop & Pro: ≤ 1 GB  
Power BI Premium: Recommended for larger datasets or frequent refreshes.

---

## 📏 DAX Measures

A robust suite of DAX measures supports rolling analytics, comparisons, performance targets, and trends.

### Key Measures (Located in `Measure Table > Sales`):

- `% All Returns`
- `10 Day Rolling Revenue`
- `90 Day Rolling Profit`
- `All Returns`
- `Avg Retail Price`
- `Avg Revenue Per Customer`
- `Bike Return Rate`
- `Bike Returns`
- `Bike Sales`
- `Bulk Orders`
- `High Ticket Orders`
- `Order Quantity`
- `Order Target`
- `Order Target Gap`
- `Overall Average Price`
- `Previous Month Orders`
- `Previous Month Profit`
- `Previous Month Returns`
- `Previous Month Revenue`
- `Profit Target`
- `Profit Target Gap`
- `Quantity Return`
- `Quantity Sold`
- `Revenue Target Gap`

---

## 📈 Report Features

### Top KPIs

- Revenue
- Quantity Sold
- Average Price
- Unique Product Count

### Filters & Slicers

- Country
- Region
- Category
- Subcategory
- Year / Month

### Visualizations

- 📍 **Revenue by Country** – Interactive Map  
- 📉 **Monthly Revenue Trend** – Line Chart  
- 📊 **Top/Bottom 10 Products** – Bar Chart  
- 🍩 **Category Distribution** – Donut Chart  
- 📦 **Quantity by Subcategory** – Bar Chart  
- 📈 **Rolling Revenue/Profit** – Line Chart  
- 📌 **Order Target vs Actuals** – Combined Bar + Line Chart

---

## 📂 Files

| File Name                              | Description                           |
|---------------------------------------|---------------------------------------|
| `Consumer_Remort_Global_Dashboard.pbix` | Primary Power BI report file           |
| `README.md`                           | Project documentation                  |
| `Consumer_Remort_Global_Dashboard.pdf`| Static visual reference of report layout |
| `Sales_Schema.png`                    | Data model diagram                     |

---

## 🚀 How to Use

1. Open `Consumer_Remort_Global_Dashboard.pbix` in **Power BI Desktop**.
2. Load or refresh with your **own data source**.
3. Explore using **filters and visuals** for insights.
4. Optionally, publish to **Power BI Service** to:
   - Share with stakeholders
   - Set up scheduled data refreshes

---

## 📌 Notes

- **Schema**: Snowflake
- **Storage Mode**: Import
- **DAX Centralization**: All measures are housed under `Measure Table > Sales`
- **Design Philosophy**:  
  Focused on **performance**, **scalability**, and **user-friendly accessibility**.

---

## 👤 Author
**Laxman**  
🔗 [LinkedIn](https://www.linkedin.com/in/laxman-c/)
