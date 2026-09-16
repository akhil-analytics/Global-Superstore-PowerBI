# Global Superstore Sales & Profit Analysis — Power BI

## 📊 Project Overview

This project is an interactive **Power BI dashboard built using the Global Superstore dataset**.  
The objective is to analyze sales performance, profitability, customer segments, markets, regions, countries, product categories, order status, and customer purchasing patterns.

The dashboard combines **data transformation, DAX calculations, interactive slicers, KPI cards, maps, charts, tables, and drill-down analysis** to convert raw transactional data into business insights.

---

## 🎯 Business Objectives

The dashboard was designed to answer questions such as:

- How are total sales and profit performing?
- How has sales changed from 2016 to 2019?
- Which months and quarters generate the highest sales?
- Which markets and regions contribute the most revenue?
- Which countries have higher sales and profitability?
- How does performance differ across Consumer, Corporate, and Home Office segments?
- Which product categories and sub-categories have higher costs?
- What proportion of orders are delayed versus on-time?
- How do customer age groups and gender/average-buying behavior vary across regions?
- How does actual sales compare with the defined monthly sales target?

---

## 🗂️ Dataset

The supplied Excel workbook contains four main tables:

### Orders
The primary transactional table containing fields such as:

- Order ID
- Order Date
- Ship Date
- Ship Mode
- Customer ID
- Segment
- City
- State
- Country
- Market
- Region
- Product ID
- Category
- Sub-Category
- Product Name
- Sales
- Quantity
- Discount
- Profit
- Shipping Cost
- Order Priority

### People
Contains regional information associated with people/sales representatives.

### Returns
Contains returned order information and market details.

### Customer
Contains customer-level information including:

- Customer ID
- Customer Name
- Date of Birth
- Marital Status
- Date of First Purchase
- Gender
- Yearly Income

---

## 🛠️ Tools & Technologies

- **Power BI Desktop**
- **Power Query** — data cleaning and transformation
- **DAX** — calculated measures and KPI calculations
- **Microsoft Excel** — source data
- **Power BI Visualizations**
  - KPI Cards
  - Bar/Column Charts
  - Line Charts
  - Combo Charts
  - Pie/Donut Charts
  - Maps
  - Tables/Matrix
  - Gauge
  - Slicers
  - Q&A visual

---

# 📑 Dashboard Pages

## 1. Geographic & Regional Analysis

This page focuses on the geographical distribution of sales and profit.

### Visuals included

- **Sum of Profit by Country — Map**
  - Shows the geographical distribution of profit.
  - Bubble size helps identify countries with comparatively higher profit contribution.

- **Sum of Sales by Country — Map**
  - Provides a geographical view of sales performance.

- **Sales & Profit by Region**
  - Compares sales and profit across different regions.

- **Sales by Country and Year**
  - Allows comparison of country-level sales across 2016, 2017, 2018, and 2019.

- **Order Status**
  - Displays the distribution of delayed and on-time orders.

- **Q&A Visual**
  - Enables natural-language questions about the dataset.

---

## 2. Country, Cost & Target Analysis

This page provides more detailed country-level and product-cost analysis.

### Visuals included

- **Sales & Profit by Country and Year**
  - Breaks down country performance across individual years.
  - Helps identify changes in sales and profitability over time.

- **Average Cost Price by Category/Sub-Category**
  - Matrix-style analysis of average cost price.
  - Supports comparison between categories such as Furniture and Office Supplies and their sub-categories.

- **Sales Target KPI**
  - Displays sales for a selected date period against a defined desired/target sales value.

---

## 3. Customer & Segment Analysis

This page focuses on customer behavior and segment-level performance.

### Visuals included

- **Customer/Buying Preference Matrix**
  - Compares buying behavior across regions, categories/sub-categories, gender, and above/below-average purchasing groups.

- **High-Value Orders by Region**
  - Shows high-value order counts and their percentage contribution by region.

- **Customer Count by Age Group**
  - Segments customers into groups such as Young, Adult, Old Adult, Old, and Teen.

- **Sales & Profit by Segment**
  - Compares Consumer, Corporate, and Home Office segments.

This page provides a customer-oriented view in addition to the traditional sales analysis.

---

## 4. Global Superstore Executive Dashboard

The main executive-style dashboard brings the most important KPIs and trends together in a single view.

### KPI Cards

- **Total Sales:** approximately **$12.64M**
- **Total Profit:** approximately **$1.47M**
- **Total Orders:** approximately **25K unique orders**
- **Customer Records:** approximately **51K records** in the transactional dataset

### Additional visuals

- **Sales by Year**
- **Sales & Profit by Month**
- **Sales & Profit by Market**
- **Sales by Quarter**
- **Profit Gauge**
- **Monthly Sales Target**
- **Category slicer**
- **Segment slicer**
- **Clear All Slicers button**

The dashboard is designed to allow users to filter the analysis and observe how KPIs and visualizations change dynamically.

---

# 📈 Key Findings from the Dataset

Based on the supplied transactional data:

| Metric | Value |
|---|---:|
| Total Sales | ~$12.64M |
| Total Profit | ~$1.47M |
| Profit Margin | ~11.6% |
| Unique Orders | ~25,035 |
| Customers | ~1,590 |
| Countries | 147 |
| Data Period | 2016–2019 |

### Sales trend

Annual sales increased across the four-year period:

| Year | Sales |
|---|---:|
| 2016 | ~$2.26M |
| 2017 | ~$2.68M |
| 2018 | ~$3.41M |
| 2019 | ~$4.30M |

### Segment contribution

The Consumer segment has the largest sales contribution, followed by Corporate and Home Office.

### Market contribution

APAC and EU are among the largest markets by sales in the supplied data, while the dashboard allows users to compare all markets interactively.

---

# 🧮 Example DAX Measures

Examples of the type of measures used/appropriate for this dashboard include:

```DAX
Total Sales =
SUM(Orders[Sales])
```

```DAX
Total Profit =
SUM(Orders[Profit])
```

```DAX
Profit Margin =
DIVIDE([Total Profit], [Total Sales], 0)
```

```DAX
Total Orders =
DISTINCTCOUNT(Orders[Order ID])
```

```DAX
Total Customers =
DISTINCTCOUNT(Orders[Customer ID])
```

Additional time-intelligence measures can be used for:

- Year-over-Year Sales Growth
- Previous Year Sales
- Monthly Sales
- Quarterly Sales
- Target Variance
- Target Achievement %

---

# 🔄 Data Analysis Workflow

The overall workflow for this project was:

**Excel Dataset → Power Query → Data Cleaning & Transformation → Data Model → DAX Measures → Visualizations → Interactive Dashboard → Business Insights**

### Data preparation

The dataset was prepared for analysis by:

- Reviewing data types
- Working with date fields
- Organizing categorical fields
- Preparing sales/profit measures
- Creating dimensions/groupings required for analysis
- Connecting related tables
- Building calculated measures for KPIs

---

# 🎨 Dashboard Design

The dashboard uses a consistent visual theme across the pages, with:

- KPI cards for important metrics
- Charts for trend and comparison analysis
- Maps for geographic analysis
- Matrix/table visuals for detailed breakdowns
- Slicers for interactive filtering
- Gauge visualization for profit/target tracking
- Clear All Slicers functionality for user navigation

---

# 💡 Business Use Cases

This dashboard can be used by business teams to:

- Monitor sales performance
- Track profitability
- Identify high-performing markets and regions
- Compare customer segments
- Analyze product/category performance
- Monitor order delays
- Evaluate sales against targets
- Identify geographic opportunities
- Support data-driven business decisions

---

# 📁 Recommended GitHub Repository Structure

```text
Global-Superstore-PowerBI/
│
├── README.md
├── GlobalSuperstore.pbix
├── GlobalSuperstore.xlsx
│
├── screenshots/
│   ├── executive-dashboard.png
│   ├── geographic-analysis.png
│   ├── customer-analysis.png
│   └── detailed-analysis.png
│
└── documentation/
    └── project-notes.md
```

> If the Excel dataset is large or you are concerned about repository size, you can keep the source dataset out of the repository and document where the data came from instead.

---

# 🚀 How to Use

1. Download/clone the repository.
2. Open `GlobalSuperstore.pbix` using Power BI Desktop.
3. If required, update the source-data path in Power Query.
4. Refresh the dataset.
5. Use the slicers to filter by category and segment.
6. Navigate between dashboard pages to explore sales, profit, geography, customers, and targets.

---

# 📌 Suggested Improvements

The dashboard already contains a broad range of analysis. For a stronger **portfolio/GitHub project**, I would recommend the following improvements:

### 1. Add a dedicated Executive Summary page
Keep the first page focused on:

- Total Sales
- Total Profit
- Profit Margin %
- Total Orders
- Sales Growth %
- Target Achievement %
- Top 5 Markets/Regions
- Monthly Sales Trend

This makes the dashboard easier for a recruiter or hiring manager to understand quickly.

### 2. Add Profit Margin %
You currently show Sales and Profit. Adding **Profit Margin %** would make profitability easier to compare across markets, regions, and categories of different sizes.

### 3. Add YoY Growth %
A measure such as:

**YoY Growth % = (Current Year Sales − Previous Year Sales) / Previous Year Sales**

would make the year-over-year analysis more business-oriented.

### 4. Add Top 10 / Bottom 10 Products
A recruiter will often expect product-level analysis in a sales dashboard.

Consider adding:

- Top 10 Products by Sales
- Top 10 Products by Profit
- Bottom 10 Products by Profit
- Loss-making Products

### 5. Add a proper Date Slicer
Add a date/year/month slicer so users can easily select a reporting period.

### 6. Improve visual consistency
The current dashboard has a strong custom theme, but the combination of bright pink, peach, dark backgrounds, and map imagery can compete for attention.

For a professional portfolio version, consider using:

- 1 primary background color
- 1 accent color
- 1 secondary accent color
- Neutral KPI cards
- Consistent chart titles
- Less decorative background texture

The goal is to make the **data stand out more than the dashboard styling**.

### 7. Rename visual titles to business questions
Instead of:

`Sum of Sales and Sum of Profit by Region`

use:

`Sales & Profit by Region`

Instead of:

`Count of Order ID by statuses of delay/ontime`

use:

`Order Delivery Status`

This makes the dashboard look more polished.

### 8. Add dynamic titles
For example:

`Sales & Profit by Market — 2016–2019`

or dynamically display the selected Category/Segment.

### 9. Add tooltips
Create a dedicated tooltip page containing:

- Sales
- Profit
- Profit Margin
- Orders
- YoY Growth %

This can provide more information without overcrowding the dashboard.

### 10. Add a dedicated Returns analysis
Because the workbook contains a Returns table, a separate returns section could analyze:

- Return Rate
- Returned Orders
- Returns by Category
- Returns by Market
- Returns by Product
- Return trend over time

This would make better use of the available data.

---

# 🧠 Skills Demonstrated

This project demonstrates practical experience with:

**Power BI**
- Dashboard development
- Interactive reporting
- Data visualization
- Slicers and filtering
- KPI design
- Maps
- Matrix reporting
- Drill-down analysis

**Power Query**
- Data preparation
- Data transformation
- Data type handling
- ETL workflow

**DAX**
- Aggregation measures
- KPI calculations
- Profitability metrics
- Time-based calculations
- Target calculations

**Business Analysis**
- Sales performance analysis
- Profitability analysis
- Customer segmentation
- Geographic analysis
- Market comparison
- Target tracking
- Trend analysis

---

# 👨‍💻 Project Type

**Business Intelligence / Data Analytics Project**

**Primary Tool:** Power BI  
**Data Source:** Excel  
**Domain:** Sales & Retail Analytics

---

## ⭐ Portfolio Summary

> An interactive Power BI business intelligence dashboard built using the Global Superstore dataset to analyze sales, profitability, customers, products, markets, regions, order status, and sales targets. The project combines Power Query, DAX, interactive visualizations, geographic analysis, KPI reporting, and customer segmentation to transform transactional data into an actionable business reporting solution.
