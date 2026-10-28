# Task 4: Final Data Analytics Case Study

## Project Overview

This final case study brings together the data cleaning, exploratory data analysis (EDA), and interactive dashboard development completed as part of the SWYNEX Technologies Data Analyst Internship.

The project analyzes the Online Retail dataset to understand sales performance, customer purchasing behavior, product performance, and business trends.

## Problem Statement

Retail businesses generate large volumes of transaction data. Analyzing this data helps identify revenue trends, high-performing products, valuable customers, and opportunities to improve business decisions.

The objective of this project is to transform raw retail transaction data into meaningful insights using Python and Microsoft Power BI.

## Dataset Information

- **Dataset:** Online Retail
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail)
- **Period:** December 2010 – December 2011
- **Original records:** 541,909
- **Records after cleaning:** 536,641

The dataset includes invoice numbers, product descriptions, quantities, transaction dates, unit prices, customer identifiers, and countries.

**Important:** December 2011 contains data only through December 9, so it represents a partial month.

## Task 1: Data Cleaning and Preparation

The raw dataset was cleaned using Python, Pandas, and NumPy.

Key activities:

- Inspected data types, missing values, and duplicate records.
- Removed duplicate rows.
- Converted transaction dates to datetime format.
- Reviewed missing customer identifiers and product descriptions.
- Created flags for zero-price, negative-price, negative-quantity, and unusually high-quantity records.
- Calculated revenue as quantity multiplied by unit price.

**Result:** The cleaned dataset contains 536,641 rows and 13 columns. Returns, cancellations, and unusual transactions were retained for appropriate analysis.

## Task 2: Exploratory Data Analysis

Exploratory analysis was performed using Pandas, Matplotlib, and Seaborn.

Key analyses included:

- Monthly net revenue trends
- Revenue by country
- Top products and customers by net revenue
- Revenue by weekday
- Monthly invoice volume
- Revenue per invoice
- Customer purchasing frequency
- Correlation analysis and unusual transaction values

### Key Findings

- Total net revenue was approximately 9.73 million in the dataset's currency.
- The United Kingdom contributed approximately 84% of net revenue.
- November 2011 recorded the highest monthly net revenue and invoice volume in the analyzed period.
- Thursday recorded the highest net revenue among the observed weekdays.
- The Regency Cake Stand 3 Tier was the highest-revenue merchandise product after excluding postage-related codes.

## Task 3: Interactive Power BI Dashboard

An interactive dashboard was developed using Microsoft Power BI Desktop.

### Dashboard Components

- KPI cards for Net Revenue, Total Invoices, Identified Customers, Countries, and Total Quantity Sold
- Monthly net revenue trend
- Revenue by country — Top 10
- Net revenue by weekday
- Top 10 products by net revenue
- Top 10 customers by net revenue
- Monthly invoice volume
- Country and YearMonth slicers

The dashboard allows users to explore performance across countries and months.

### Dashboard Preview

See the screenshot and Power BI file in the [Task 3 dashboard folder](../Task-3-Interactive-Dashboard/).

## Business Insights and Recommendations

1. **Monitor country-level performance:** The United Kingdom contributes the majority of net revenue, so tracking its sales trends is important while exploring opportunities in other markets.
2. **Review seasonal demand:** November showed the highest monthly net revenue in the analyzed period. Compare future periods to determine whether this pattern repeats.
3. **Understand product performance:** Use product-level revenue and quantity analysis to support inventory planning and product decisions.
4. **Study customer contribution:** Analyze high-value customers and repeat purchasing behavior to help inform customer retention strategies.
5. **Track returns and cancellations:** Review negative quantities and invoice activity to better understand their effect on net revenue.
6. **Compare complete periods:** Avoid comparing December 2011 directly with full months because the dataset ends on December 9.

These recommendations are based on historical transaction data and should be validated against more recent business data before making operational decisions.

## Tools and Technologies

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Jupyter Notebook
- Microsoft Power BI Desktop
- Git and GitHub

## Project Files

- [Task 1: Data Cleaning](../Task-1-Data-Cleaning/)
- [Task 2: Exploratory Data Analysis](../Task-2-Exploratory-Data-Analysis/)
- [Task 3: Interactive Dashboard](../Task-3-Interactive-Dashboard/)

## Conclusion

This project demonstrates an end-to-end data analytics workflow, from data preparation and exploratory analysis to interactive business reporting.

It provided practical experience in data cleaning, data visualization, KPI development, dashboard design, and communicating business insights.

**Project:** Online Retail Data Analysis  
**Internship:** Data Analyst Internship — SWYNEX Technologies
