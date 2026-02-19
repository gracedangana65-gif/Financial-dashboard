# 📊 Financial Performance Analysis Dashboard

## 📌 Project Overview

This project analyzes financial data to evaluate company performance, revenue trends, cost behavior, and profitability over time. The objective is to transform raw financial data into actionable insights that support strategic business decisions.

The dashboard was built using **Power BI**, with data cleaning performed in **Power Query** and calculations implemented using **DAX**.

---

## 🎯 Business Objectives

- Analyze revenue growth trends
- Evaluate gross and net profit margins
- Identify high-performing regions and products
- Detect cost inefficiencies
- Provide data-driven financial recommendations

---

## 🗂 Dataset Description

The dataset includes transaction-level financial data with the following key fields:

- Revenue
- Cost of Goods Sold (COGS)
- Operating Expenses
- Gross Profit
- Net Profit
- Product Category
- Region
- Date (Year, Quarter, Month)

Time Period Covered: *(Insert Time Range)*

---

## 🛠 Tools & Technologies

- **Power BI Desktop** – Data modeling & dashboard development
- **Power Query** – Data cleaning & transformation
- **DAX (Data Analysis Expressions)** – KPI and financial calculations
- **Excel / SQL** – Data preparation (if applicable)

---

## 🏗 Data Modeling

A **Star Schema** was implemented for optimal performance:

- **Fact Table:** Financial Transactions  
- **Dimension Tables:**
  - Date
  - Product
  - Region

This structure improved report performance and ensured accurate filter propagation.

---

## 📐 Key DAX Measures

```DAX
Total Revenue = SUM(Financials[Revenue])

Total COGS = SUM(Financials[COGS])

Gross Profit = [Total Revenue] - [Total COGS]

Gross Profit Margin =
DIVIDE([Gross Profit], [Total Revenue], 0)

Net Profit Margin =
DIVIDE([Net Profit], [Total Revenue], 0)

Year-to-Date Revenue =
TOTALYTD([Total Revenue], 'Date'[Date])
