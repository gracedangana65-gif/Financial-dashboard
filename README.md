# 📊 Financial Sales Performance Analysis Dashboard

**Tools:** Power BI | Power Query | DAX  
**Project Type:** Financial Data Analysis & Business Intelligence

This project analyzes financial sales data to uncover insights about **revenue performance, product profitability, and sales trends**.  
The dashboard transforms raw sales data into **actionable insights that support business decision-making**.

---

# 🎯 Project Objectives

The objective of this project is to:

- Evaluate overall financial performance
- Identify revenue-generating products
- Understand profit distribution across products
- Analyze sales trends over time
- Provide insights to support data-driven decisions

---

# 🗂 Dataset Overview

The dataset contains financial sales records including:

| Column | Description |
|------|-------------|
| Sales | Total value of sales transactions |
| Sales Price | Price per product unit |
| Units Sold | Number of units sold |
| Profit | Profit generated |
| Product | Product name |
| Category | Product group |
| Date | Transaction date |

Since revenue was not directly included in the dataset, it was calculated using **Sales Price × Units Sold**.

---

# 🧮 Key Calculations

### Revenue

```DAX
Revenue = SUMX('Sales Data', 'Sales Data'[Sales Price] * 'Sales Data'[Units Sold])
```

### Total Sales

```DAX
Total Sales = SUM('Sales Data'[Sales])
```

### Total Profit

```DAX
Total Profit = SUM('Sales Data'[Profit])
```

### Total Units Sold

```DAX
Total Units Sold = SUM('Sales Data'[Units Sold])
```

### Profit Margin

```DAX
Profit Margin = DIVIDE([Total Profit], [Revenue], 0)
```

---

# 📊 Business Questions Answered

## 1️⃣ What is the overall financial performance of the business?

### Metrics Used
- Total Revenue
- Total Sales
- Total Profit
- Total Units Sold

### Insight

The KPI summary provides a snapshot of overall business performance and shows how much revenue and profit the company generates.

### Visualization

KPI Cards showing key financial metrics.

---

## 2️⃣ How have sales changed over time?

### Analysis

Sales were analyzed using a time-series visualization to observe trends across months and years.

### Insight

This helps identify:

- Sales growth patterns
- Seasonal trends
- Periods of high or low performance

### Visualization

Line chart showing sales or revenue over time.

---

## 3️⃣ Which products generate the most revenue?

### Analysis

Products were ranked by revenue contribution.

### Insight

A small number of products generate a significant portion of total revenue, indicating strong product concentration.

### Visualization

Bar chart showing top products by revenue.

---

## 4️⃣ Which products generate the highest profit?

### Analysis

Profit was analyzed at the product level.

### Insight

Some products produce strong revenue but lower profit margins, while others generate higher profitability despite lower sales volume.

### Visualization

Bar chart comparing profit across products.

---

## 5️⃣ Which product categories contribute most to revenue?

### Analysis

Sales and profit were evaluated across product categories.

### Insight

Certain categories dominate total revenue while others contribute more to profit margins.

### Visualization

Column chart or pie chart showing category contribution.

---

## 6️⃣ How efficiently does the company convert revenue into profit?

### Metric Used

Profit Margin

### Insight

Profit margin indicates how efficiently revenue is converted into profit and highlights potential pricing or cost issues.

### Visualization

Profit margin comparison across products or categories.

---

# ⚠ Challenges Faced

## Missing Revenue Column

The dataset did not contain a direct revenue field.

**Solution**

Revenue was calculated using:

Sales Price × Units Sold.

---

## Data Cleaning Issues

The dataset contained:

- Missing values
- Duplicate records
- Inconsistent formatting

**Solution**

Power Query was used to clean and standardize the dataset.

---

# 📈 Key Insights

- Revenue is driven by a small number of products.
- High sales volume does not always result in high profitability.
- Pricing plays a significant role in overall revenue.
- Product categories contribute differently to sales and profit.

---

# 💡 Business Recommendations

Based on the analysis:

1. Focus on marketing and promoting high-profit products.
2. Review pricing strategies for low-margin products.
3. Optimize inventory for high-demand products.
4. Use dashboards to continuously monitor financial performance.

---

# 🛠 Tools Used

- **Power BI** – Dashboard creation
- **Power Query** – Data cleaning and transformation
- **DAX** – Financial calculations and metrics

---

# 📁 Project Files

```
Financial-Sales-Dashboard/
│
├── Financial Dashboard.pbix
├── Dashboard Screenshots
└── README.md
```


# 🚀 Future Improvements

Future enhancements could include:

- Sales forecasting
- Customer segmentation analysis
- Regional sales performance
- Real-time database integration
