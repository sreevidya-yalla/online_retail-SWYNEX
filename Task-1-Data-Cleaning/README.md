# Task 1: Data Cleaning and Preparation

## Project Overview
This project focuses on cleaning and preparing the Online Retail dataset as part of the SWYNEX Technologies Data Analyst Internship.

## Tools Used
- Python
- Pandas
- NumPy
- Jupyter Notebook
- GitHub

## Dataset Description
The dataset contains online retail transactions with the following columns:
- InvoiceNo
- StockCode
- Description
- Quantity
- InvoiceDate
- UnitPrice
- CustomerID
- Country

## Data Cleaning Steps
1. Inspected the dataset structure, data types, and summary statistics.
2. Identified missing values in Description and CustomerID.
3. Removed exact duplicate rows.
4. Removed leading and trailing whitespace from text columns.
5. Converted InvoiceDate to datetime format.
6. Converted CustomerID to a nullable integer type.
7. Validated the cleaned dataset.

## Results
- Original rows: 541,909
- Duplicate rows removed: 5,268
- Cleaned rows: 536,641
- Columns retained: 8
- Remaining missing descriptions: 1,454
- Remaining missing CustomerIDs: 135,037
- Remaining exact duplicate rows: 0

## Data Quality Decisions
Missing descriptions and CustomerIDs were retained to avoid unnecessarily losing potentially useful transactions. Negative quantities, zero unit prices, and negative unit prices were preserved for further investigation rather than automatically deleting them.

## Output Files
- `cleaned_online_retail.zip` — compressed cleaned dataset.

## Status
Data cleaning and initial validation completed.
