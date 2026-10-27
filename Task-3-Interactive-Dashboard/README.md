# Task 3: Power BI Sales Dashboard

## Project Overview
This task focuses on developing an interactive sales dashboard using Microsoft Power BI to analyze the Online Retail dataset. The dashboard presents key business metrics and visual insights into revenue, invoices, customers, products, countries, and sales trends.

## Tools Used
- Microsoft Power BI Desktop
- Power Query / Data Model
- DAX (Data Analysis Expressions), where applicable
- Cleaned Online Retail dataset from Task 1

## Dataset
The dashboard uses the cleaned Online Retail dataset prepared during Task 1.

- **Source:** Online Retail dataset
- **Period:** December 2010 – December 2011
- **Last transaction date:** December 9, 2011
- **Note:** December 2011 is a partial month.

## Dashboard Preview

![Online Retail Sales Dashboard](./dashboard_screenshot.png)

The interactive Power BI dashboard summarizes online retail performance through key metrics, sales trends, country-wise revenue, and top-performing products and customers.

## Dashboard KPIs
The dashboard includes five key performance indicators:

1. **Net Revenue** — Total revenue calculated from quantity multiplied by unit price, including negative values from returns and cancellations.
2. **Total Invoices** — Count of invoice numbers.
3. **Identified Customers** — Count of distinct customer IDs represented by the current card aggregation.
4. **Countries** — Number of countries represented in the data.
5. **Total Quantity Sold** — Net quantity across transactions, including returns and cancellations.

## Visualizations
The dashboard contains six visualizations:

- **Monthly Net Revenue Trend:** Tracks changes in net revenue over time.
- **Revenue by Country — Top 10:** Compares net revenue across countries.
- **Net Revenue by Weekday:** Shows revenue distribution by weekday.
- **Top 10 Products by Net Revenue:** Identifies products with the highest net revenue.
- **Top 10 Customers by Net Revenue:** Highlights customers with the highest net revenue.
- **Monthly Invoice Volume:** Compares invoice activity across months.

## Interactive Slicers
The dashboard includes two dropdown slicers:

- **Country:** Filters dashboard results by country.
- **YearMonth:** Filters results by month.

These slicers allow users to explore the dashboard for different countries and time periods.

## Key Insights
- The United Kingdom contributes the largest share of net revenue.
- November 2011 records the highest monthly net revenue and invoice volume in the analyzed period.
- Thursday has the highest net revenue among the observed weekdays.
- Regency Cakestand 3 Tier is the leading merchandise product by net revenue in the analysis.
- Customer revenue varies considerably, with a small group of customers contributing substantial revenue.
- December 2011 results cover only the first nine days of the month and should not be compared directly with complete months.

## Important Data Considerations
- The dataset includes returns and cancellation transactions, so net revenue and net quantity can be negative.
- Customer IDs are missing for some transactions.
- Unusual values were retained and flagged during Task 1 rather than automatically deleted.
- Dashboard results depend on the selected slicer filters and the aggregation used by each visual.

## Project Files
- `Online_Retail_Dashboard.pbix` — Power BI dashboard file. The filename may differ depending on the saved file name.
- `README.md` — Documentation for this task.

## Conclusion
The Power BI dashboard converts the cleaned retail transaction data into an interactive report. It supports exploration of sales performance, customer activity, product revenue, country-level performance, and monthly trends.

This task completes the dashboard development stage of the Online Retail Data Analysis project.
