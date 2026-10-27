# Task 2: Exploratory Data Analysis (EDA) — Online Retail Dataset

## 1. Project Overview

This task focuses on performing Exploratory Data Analysis (EDA) on the cleaned Online Retail dataset. The objective is to identify patterns in revenue, product performance, customer activity, invoice trends, and transaction behavior.

The analysis uses Python to summarize the data, investigate unusual transactions, and create visualizations that support business insights.

## 2. Dataset Information

- **Dataset:** Online Retail
- **Input file:** `../Task-1-Data-Cleaning/cleaned_online_retail.csv`
- **Rows analyzed:** 536,641
- **Original columns:** 13
- **Additional EDA columns:** 2
- **Total columns in the working DataFrame:** 15
- **Date range:** December 1, 2010 – December 9, 2011
- **Unique invoice numbers:** 25,900
- **Identifiable customers:** 4,372
- **Unique stock codes:** 4,070
- **Countries represented:** 38

The cleaned dataset from Task 1 is used as input. The original raw dataset and Task 1 output are not modified by this analysis.

## 3. Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## 4. EDA Process

### Step 1: Load and Inspect the Dataset

Loaded the cleaned CSV and examined the first rows, dataset dimensions, column names, data types, and summary statistics.

### Step 2: Prepare Data Types

- Converted `InvoiceDate` to datetime format.
- Converted `CustomerID` to Pandas nullable integer format.
- Added `YearMonth` for monthly analysis.
- Added `DayOfWeek` for weekday analysis.

These additional columns exist only in the EDA working DataFrame.

### Step 3: Examine Data Quality

Reviewed missing values and unusual transactions.

- Missing descriptions: 1,509
- Missing customer IDs: 135,037
- Zero-price rows: 2,510
- Negative-price rows: 2
- Negative-quantity rows: 10,587
- High-quantity rows: 172
- Cancellation invoice rows: 9,251

Potentially meaningful returns, cancellations, and accounting adjustments were retained rather than automatically deleted.

### Step 4: Monthly Revenue Analysis

Grouped transactions by month and calculated total net revenue.

**Finding:** November 2011 had the highest monthly net revenue, at approximately 1,456,145.80.

December 2011 is a partial month because the dataset ends on December 9, 2011.

### Step 5: Country Revenue Analysis

Calculated net revenue by country and identified the top 10 countries.

**Finding:** The United Kingdom had net revenue of approximately 8,167,128.18, representing about 83.97% of total net revenue.

### Step 6: Product Performance Analysis

Analyzed products by net revenue and net quantity.

**Findings:**
- Regency Cakestand 3 Tier was the highest-ranked merchandise item by net revenue after excluding the postage-related stock codes `DOT` and `POST`.
- Small Popcorn Holder had the highest net quantity among the merchandise items in the quantity analysis.
- The highest-ranked product by revenue was different from the highest-ranked product by quantity.

### Step 7: Weekday Revenue Analysis

Calculated net revenue by day of the week.

**Finding:** Thursday had the highest net revenue, at approximately 2,108,701.53.

No Saturday transaction rows were present in this dataset. This finding applies to the available data and does not establish that the business never operated on Saturdays.

### Step 8: Customer Revenue Analysis

Calculated net revenue and distinct invoice counts for identifiable customers.

**Findings:**
- Customer ID 14646 had the highest net revenue, at approximately 279,489.02.
- Customer ID 18102 ranked second, at approximately 256,438.49.

Customer IDs are used instead of customer names because names are not included in the dataset.

### Step 9: Invoice Revenue Analysis

Grouped transaction rows by invoice number and examined the distribution of net revenue per invoice.

**Findings:**
- Average net revenue per invoice: approximately 375.52
- Median net revenue per invoice: approximately 206.31

The distribution was right-skewed, with some unusually high positive and negative invoice values.

### Step 10: Monthly Invoice and Customer Trends

Compared monthly invoice counts, identifiable customer counts, and net revenue per invoice.

**Findings:**
- November 2011 had the highest invoice count, at 3,462.
- November 2011 had the highest identifiable customer count, at 1,711.
- September 2011 had the highest net revenue per invoice, at approximately 437.30.

These patterns show that total revenue, invoice activity, and average invoice value provide different perspectives on business performance.

### Step 11: Customer Purchase Frequency

Counted distinct invoice numbers for each identifiable customer.

**Findings:**
- Customers with one invoice: 1,313
- Customers with more than one invoice: 3,059
- Median distinct invoice count per customer: 3

These results describe invoice activity, including cancellation invoice numbers, rather than confirmed successful repeat purchases.

### Step 12: Correlation Analysis

Examined correlations between quantity, unit price, and revenue.

- Quantity and Revenue: approximately 0.887
- UnitPrice and Revenue: approximately -0.162
- Quantity and UnitPrice: approximately -0.001

Revenue is calculated as `Quantity × UnitPrice`. Therefore, these correlations are influenced by the mathematical relationship, negative transactions, and extreme values. Correlation does not establish causation.

### Step 13: Extreme Revenue Investigation

Used the 1st and 99th percentiles to identify unusually low and high transaction revenue values.

- 1st percentile: approximately -6.62
- 99th percentile: approximately 180.37
- Rows outside these percentile limits: 10,734

Large positive and negative transactions were investigated rather than automatically removed. For example, some extreme quantities had corresponding cancellation records.

## 5. Visualizations Created

The notebook includes the following charts:

1. Monthly Net Revenue
2. Top 10 Countries by Net Revenue
3. Top 10 Merchandise Items by Net Revenue
4. Net Revenue by Day of the Week
5. Top 10 Merchandise Items by Net Quantity
6. Top 10 Customers by Net Revenue
7. Distribution of Net Revenue per Invoice
8. Monthly Invoice Count
9. Monthly Net Revenue per Invoice
10. Monthly Unique Customers
11. Customer Purchase Frequency
12. Correlation Heatmap

## 6. Overall Business Insights

- The United Kingdom is the dominant market by net revenue.
- November 2011 had the highest monthly net revenue and invoice count.
- Regency Cakestand 3 Tier ranked highest among merchandise items by net revenue in the analyzed table.
- Small Popcorn Holder ranked highest by net quantity in the merchandise quantity analysis.
- Thursday had the highest weekday net revenue in the available records.
- September 2011 had the highest net revenue per invoice.
- Many identifiable customers had multiple distinct invoice numbers during the dataset period.
- Unusual transaction values can materially affect averages and revenue totals.

## 7. Limitations and Considerations

- Net revenue includes negative quantities, returns, cancellations, and other negative transactions.
- Missing customer IDs limit customer-level analysis.
- Product descriptions may be missing or inconsistent.
- December 2011 is incomplete.
- No Saturday transactions appear in the available dataset.
- Extreme transaction values may represent legitimate business activity and require context before being excluded.
- Revenue is not profit because product costs and operating expenses are not provided.
- Customer invoice counts include cancellation invoice numbers.
- Country and product revenue rankings describe the analyzed dataset and should not automatically be generalized beyond it.

## 8. Validation

The final validation checks confirmed:

- 536,641 transaction rows.
- No duplicate rows across the original 13 dataset columns.
- No missing invoice dates.
- Revenue calculations match `Quantity × UnitPrice`.
- No Saturday transaction rows were present.

## 9. Output Files

- `online_retail_eda.ipynb` — EDA code, tables, visualizations, and findings.
- `README.md` — documentation of the analysis.

The cleaned input file remains in `Task-1-Data-Cleaning/cleaned_online_retail.csv`.

## 10. Conclusion

This EDA explored revenue patterns, product performance, customer activity, invoice trends, and transaction quality in the Online Retail dataset. The results highlight the United Kingdom's dominant revenue contribution, increased activity toward November 2011, and differences between products ranked by revenue and quantity.

The findings provide a foundation for the next project stage: building a dashboard to communicate the key business metrics and trends.
