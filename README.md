# Retail Sales Performance Analysis (Python + Power BI)

---

## Project Overview

This project presents a complete end-to-end data analytics workflow applied to a retail sales dataset.

It covers data cleaning and exploratory data analysis using Python, followed by the development of an interactive, KPI-driven dashboard in Power BI. The goal is to analyze sales performance, profitability, payment behavior, and seasonality trends to derive actionable business insights.

---

## Tools & Technologies

- Python (pandas, matplotlib, seaborn)
- Jupyter Notebook (via VS Code)
- Power BI Desktop (Interactive Dashboard, DAX Measures)
- CSV — data storage & exchange format

---

## Project Structure

```text
├── sales_dashboard.csv          # Original retail sales dataset
├── sales_eda.ipynb              # Python exploratory data analysis notebook
├── sales_cleaned.csv            # Cleaned dataset exported for Power BI
├── sales_dashboard.pbix         # Power BI dashboard
├── images/                      # Dashboard screenshots & demos
└── README.md                    # Project documentation
```

---

## Data Source

The dataset is a retail sales transactional dataset containing order-level records, including:

- Order dates
- Product categories
- Payment modes
- Customer names
- States
- Revenue
- Profit

---

## Dataset Highlights

- **Total Transactions:** 1,994
- **Categories:** 3 (Furniture, Electronics, Office Supplies)
- **Time Span:** 5 Years
- **Total Revenue:** $6,182,639
- **Total Profit:** $1,610,697
- **Overall Profit Margin:** 26%

---

## Data Cleaning Steps

- Checked and handled null values
- Removed duplicate records
- Renamed the **Amount** column to **Revenue**
- Verified data types across numeric, categorical, and date columns
- Extracted **Year** and **Month** from **Order Date**
- Treated each row as an independent transaction (Order ID not used for aggregation)
- Detected and reviewed negative profit entries
- Identified and treated outliers using boxplots
- Exported the cleaned dataset using `to_csv()` for Power BI

---

## Exploratory Data Analysis (EDA)

- Analyzed categorical distributions across Category, Sub-Category, and Payment Mode
- Investigated negative profit transactions
- Built boxplots for revenue and profit outlier detection
- Calculated transaction-level profit margin
- Generated a correlation heatmap for numeric variables
- Conducted state-level revenue and profit analysis
- Built a Category × Payment Mode crosstab
- Aggregated data before visualization to avoid noisy row-level charts

---

## Dashboard

### Power BI Dashboard

An interactive dashboard featuring dynamic filtering and custom DAX measures.

---

## Features

- KPI Cards:
  - Total Orders
  - Top Sub-Category
  - Profit Margin %
  - Top Payment Mode
- Total Sales & Total Profit cards with YoY growth indicators
- Monthly Revenue Trend (Line Chart)
- Revenue by Category (Bar Chart)
- Payment Mode Distribution (Donut Chart)
- Top State by Revenue (Map)
- Top Sub-Category by Profit (Table)
- Year Slicer for dynamic filtering
- Overview and Insights/Recommendations pages

---

## Dashboard Preview

### Overview

![Overview](images/sales_overview.png)

### Insights & Recommendations

![Insights](images/insights&recommendations.png)

### Dashboard Demo

![Dashboard Demo](images/sales_dashboard_gif.gif)

---

## Key Insights

- Revenue distribution across categories is fairly balanced.
- Order volume remains relatively low across the five-year period, indicating room to increase purchase frequency.
- Overall profit margin is a healthy **26%**.
- Illinois generates the highest revenue.
- Debit Card is the most frequently used payment method.
- Sales consistently peak during early summer and December, reflecting seasonal shopping behavior.
- Electronics sub-categories (Laptops, Phones, Electronic Games, and Printers) contribute relatively less profit compared to their sales volume, suggesting margin compression.

---

## Recommendations

- Reprice Electronics sub-categories (Laptops, Phones, Electronic Games, and Printers) to improve profitability.
- Launch seasonal campaigns during **Q4 (September–December)**, including Halloween, Black Friday, Cyber Monday, and Christmas promotions.
- Increase year-round order volume through loyalty programs, bundles, and customer retention strategies.

---

## Notes

The dataset does not include a continuous date table by default. Year-over-Year (YoY) measures were created using manual DAX calculations alongside a dedicated Date dimension table with `SAMEPERIODLASTYEAR()`.

---

## Data Pipeline

```text
Raw Sales CSV
      │
      ▼
Data Cleaning & EDA (Python)
      │
      ▼
Cleaned CSV Export
      │
      ▼
Power BI Dashboard
```

---

## Author

**Hajar**

**Python | Power BI | Data Analytics**
