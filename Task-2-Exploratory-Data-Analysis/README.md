# Task 2: Exploratory Data Analysis (EDA)

## Project Overview

This project was completed as part of my Data Analyst Internship at SWYNEX Technologies. The objective was to explore the Online Retail dataset, identify trends and patterns, and extract meaningful business insights using Python.

## Dataset Information

- **Dataset:** Online Retail
- **Original records:** 541,909
- **Records after cleaning:** 536,641
- **Original columns:** 8
- **Source:** Cleaned dataset prepared in Task 1

The dataset contains invoice numbers, product codes, product descriptions, quantities, invoice dates, unit prices, customer IDs, and countries.

The cleaned dataset is available in the Task 1 folder of this repository.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Analysis Performed

1. Inspected dataset structure and descriptive statistics.
2. Analyzed the distribution of transaction sales.
3. Compared net recorded sales across countries.
4. Examined monthly sales trends.
5. Identified the top 10 products by net quantity.
6. Investigated negative quantities and invoice numbers beginning with `C`.
7. Calculated the United Kingdom's contribution to total net recorded sales.
8. Identified the top 10 products by net recorded sales value.
9. Compared product quantities with sales values.
10. Analyzed monthly transaction-record counts.

## Key Findings

### 1. Transaction Sales Distribution

Transaction sales were right-skewed. Most records had relatively low sales values, while a smaller number had much higher values.

### 2. Sales by Country

The United Kingdom recorded approximately **8.17 million** in net transaction sales, making it the leading country in the dataset.

### 3. Monthly Sales Trends

November 2011 recorded the highest monthly net sales, at approximately **1.46 million**. December is incomplete because the dataset ends on 9 December 2011.

### 4. Top Products by Quantity

WORLD WAR 2 GLIDERS ASSTD DESIGNS had the highest net recorded quantity, at **53,751 units**.

### 5. Negative Quantities

The dataset contained **10,587 records with negative quantities**. Of these, 9,251 had invoice numbers beginning with `C`. These records require careful investigation rather than automatic removal.

### 6. United Kingdom Sales Contribution

The United Kingdom contributed approximately **83.97%** of total net recorded transaction sales.

### 7. Top Products by Sales Value

DOTCOM POSTAGE had the highest net recorded sales value, at approximately **206,245**, followed by REGENCY CAKESTAND 3 TIER at approximately **164,459**.

### 8. Quantity Versus Sales Value

Products with the highest net quantities did not necessarily have the highest net recorded sales values. Postage-related entries should be distinguished from merchandise when evaluating product performance.

### 9. Monthly Transaction Activity

November 2011 had the highest monthly transaction-record count, at approximately **83,000 records**.

## Important Considerations

- Sales were calculated as `Quantity × UnitPrice`.
- Negative quantities and transaction values were retained for analysis.
- The sales figures represent net recorded transaction values, not profit.
- The sales distribution chart displays the middle 98% of values for visualization only; the underlying dataset was not filtered or modified for this chart.
- December 2011 is an incomplete month.
- Transaction-record counts are not the same as unique invoice counts.
- Missing customer IDs and product descriptions were retained where present.

## Conclusion

This project strengthened my understanding of exploratory data analysis, descriptive statistics, data aggregation, time-series analysis, and data visualization using Python.

The analysis revealed sales concentration by country, monthly sales patterns, differences in product performance, and unusual transaction records. These findings demonstrate how EDA can help identify business patterns and areas for further investigation.

## Project Files

- **`exploratory_data_analysis.ipynb`** — Notebook containing the Python code, charts, analysis, and findings.
- **`README.md`** — Project overview, key findings, and methodology.

## Skills Practiced

Python | Pandas | NumPy | Exploratory Data Analysis | Data Visualization | Data Aggregation | Business Insights
