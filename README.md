# Data Science Task 1: Data Cleaning & Preprocessing

## Project Overview
This project involves transforming raw, unstructured datasets into analysis-ready formats. Real-world data often contains inconsistencies, gaps, and errors that can distort insights. This task demonstrates a systematic approach to diagnosing data health and applying cleaning techniques to ensure reliability.

## Cleaning Workflow & Methodology
Following the systematic 6-step process:

1. **Data Ingestion**: Loaded datasets using `pd.read_csv()` and performed initial sanity checks with `df.head()` and `df.info()`.
2. **Deduplication**: Identified and removed exact/partial duplicate rows using `df.drop_duplicates()`.
3. **Column Management**: Dropped irrelevant columns (IDs, free-text notes) and renamed columns for clarity.
4. **Missing Value Handling**: 
    * Diagnosed missingness patterns.
    * Applied imputation: Filled numerical gaps with the mean/median and categorical gaps with the mode.
5. **Data Type Correction**: Converted strings to datetime objects and fixed numerical columns trapped as strings.
6. **Format Standardization**: Normalized text (lowercase/strip) and mapped categorical variants for consistency.

## Skills Gained
* **Advanced pandas Operations**: Mastery of data manipulation using DataFrames/Series.
* **Data Quality Assessment**: Ability to quantify and visualize data issues.
* **Strategic Decision-Making**: Judgement in choosing between imputation or deletion based on context.
* **Efficiency Optimization**: Using vectorized operations for large datasets.

## Validation
To prevent silent failures, all changes were validated using assertions:
```python
assert df[col].isna().sum() == 0
assert df.duplicated().sum() == 0
