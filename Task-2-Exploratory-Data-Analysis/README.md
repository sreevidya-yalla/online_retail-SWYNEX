# Task 2: Exploratory Data Analysis (EDA)

## Project Overview

This project focuses on Exploratory Data Analysis (EDA) of the Online Retail dataset as part of my Data Analyst Internship at SWYNEX Technologies.

The objective is to analyze retail transaction data, identify patterns and trends, compare product performance, and extract meaningful business insights using Python.

## Dataset Information

- **Dataset:** Online Retail
- **Original records:** 541,909
- **Records after cleaning:** 536,641
- **Columns:** 8 original columns, plus additional analysis columns
- **Data source:** Online Retail dataset used in Task 1

The dataset contains invoice numbers, product codes, descriptions, quantities, invoice dates, unit prices, customer IDs, and countries.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Analysis Performed

1. Inspected the dataset structure and descriptive statistics.
2. Analyzed the distribution of transaction sales using a histogram.
3. Compared recorded sales across countries.
4. Examined monthly sales trends.
5. Identified the top 10 products by net recorded quantity.
6. Investigated negative quantities and invoice numbers beginning with C.
7. Calculated the United Kingdom's percentage contribution to total net recorded sales.
8. Identified the top 10 products by net recorded sales value.
9. Compared product quantities with recorded sales values.
10. Analyzed monthly transaction-record counts.

## Key Findings

### 1. Transaction Sales Distribution

The distribution is right-skewed. Most transactions have relatively low recorded sales values, while a smaller number have much higher values.

### 2. Sales by Country

The United Kingdom recorded approximately 8.17 million in net transaction sales, making it the leading market in the dataset.

### 3. Monthly Sales Trends

November 2011 recorded the highest monthly net sales, at approximately 1.46 million. December is incomplete because the dataset ends on 9 December 2011.

### 4. Top Products by Quantity

WORLD WAR 2 GLIDERS ASSTD DESIGNS had the highest net recorded quantity, at 53,751 units.

### 5. Negative Quantities

The dataset contains 10,587 records with negative quantities. Of these, 9,251 have invoice numbers beginning with C. These records require careful interpretation rather than automatic removal.

### 6. United Kingdom Sales Contribution

The United Kingdom contributed approximately 83.97% of total net recorded transaction sales.

### 7. Top Products by Recorded Sales Value

DOTCOM POSTAGE had the highest net recorded sales value, at approximately 206,245, followed by REGENCY CAKESTAND 3 TIER at approximately 164,459.

### 8. Quantity Versus Sales Value

Products with the highest net quantities did not necessarily have the highest net recorded sales values. Postage-related entries should be distinguished from merchandise when interpreting product performance.

### 9. Monthly Transaction Activity

November 2011 had the highest monthly transaction-record count, at approximately 83,000 records.

## Important Considerations

- Net recorded sales were calculated by multiplying Quantity by UnitPrice.
- Negative quantities and negative transaction values were retained for analysis.
- The sales figures represent net recorded transaction values, not profit.
- The sales distribution chart displays the middle 98% of sales values for visualization purposes only.
- December 2011 represents an incomplete month in this dataset.
- Transaction-record counts are not the same as unique invoice counts.

## Conclusion

This project helped me practice data exploration, descriptive statistics, grouping and aggregation, time-series analysis, and data visualization using Python.

The analysis identified sales concentration by country, monthly patterns, differences in product performance, and unusual transaction records. These findings demonstrate how EDA can help prepare data for further business analysis.

## Project Files

- `exploratory_data_analysis.ipynb` — Notebook containing the analysis, visualizations, and findings.

## Skills Practiced

Python | Pandas | NumPy | Data Cleaning | Exploratory Data Analysis | Data Visualization | Business Insights
