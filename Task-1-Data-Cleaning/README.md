# Task 1 — Data Cleaning & Preparation

## Objective
Inspect and prepare the Online Retail dataset while preserving legitimate sales, returns, and cancellation records.

## Tools
Python, Pandas, NumPy, Jupyter Notebook.

## Dataset
The notebook expects the unchanged raw CSV at `data/raw/online_retail.csv` relative to the repository root. The raw file is intentionally not copied into this starter package. Add it locally before running the notebook, and follow the dataset's license/redistribution terms before publishing it.

## Notebook
Run `online_retail_data_cleaning.ipynb` from this task folder. The current notebook performs the initial audit only; it does not yet create the cleaned output.

## Initial audit
The uploaded source file was inspected before changes:
- Shape: 541,909 rows × 8 columns
- Missing `Description`: 1,454
- Missing `CustomerID`: 135,080
- Exact duplicate rows: 5,268
- Cancellation-like invoice numbers beginning with `C`: 9,288
- Negative quantities: 10,624
- Zero unit prices: 2,515
- Negative unit prices: 2
- Unparseable `InvoiceDate` values: 0

These are audit findings, not cleaning outcomes. Values will be rechecked by the notebook and decisions documented before removal or modification.

## Planned cleaning principles
- Keep the raw dataset unchanged.
- Do not automatically delete rows with missing customer IDs.
- Preserve legitimate returns and cancellation records in the master dataset.
- Do not invent product descriptions.
- Investigate duplicates, zero/negative prices, and outliers before deciding how to handle them.
- Validate the cleaned dataset and compare before/after row counts before marking this task complete.

## Status
**In progress — initial audit notebook created.** The cleaned CSV and final results are not yet available.
