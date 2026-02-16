# 📉 Company Layoffs Data Cleaning (SQL)

## Project Overview
In this project, I performed comprehensive data cleaning on a raw dataset containing global company layoffs. The goal was to transform messy, unformatted data into a clean, structured format ready for exploratory data analysis (EDA).

**Dataset Source:** [Kaggle Company Layoffs 2022](https://www.kaggle.com/datasets/swaptr/layoffs-2022)

## Key SQL Skills Applied
- **Data Staging:** Created staging tables to preserve raw data integrity.
- **Deduplication:** Utilized `ROW_NUMBER()` and `PARTITION BY` to identify and remove duplicate records.
- **Data Standardization:** 
  - Standardized inconsistent industry naming (e.g., merging 'Crypto Currency' into 'Crypto').
  - Fixed trailing punctuation in country fields using `TRIM(TRAILING '.' FROM ...)`.
- **Handling Nulls:** Used **Self-Joins** to populate missing industry data based on existing records for the same company.
- **Type Conversion:** Converted `text` date strings into proper `DATE` formats using `STR_TO_DATE`.
- **Schema Optimization:** Dropped unnecessary helper columns and removed rows with insufficient data for analysis.

## The Workflow
1. **Remove Duplicates:** Used a temporary `row_num` column to filter out redundant data.
2. **Standardize Data:** Fixed spelling issues and whitespace.
3. **Null Values:** Populated nulls where possible and removed data that wasn't useful for modeling.
4. **Final Clean:** Dropped the `row_num` column and verified the final schema.

## How to use
The full script can be found in the [Portfolio Project - Data Cleaning.sql](./Portfolio%20Project%20-%20Data%20Cleaning.sql) file.
