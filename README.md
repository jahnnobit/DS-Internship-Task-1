# DS-Internship-Task-1
# Task 1: Data Cleaning & Preprocessing

## 📌 Project Overview
[cite_start]This project involves transforming a raw dataset of Data Science job postings into an analysis-ready format[cite: 4]. [cite_start]Real-world data often contains inconsistencies, gaps, and errors that can distort insights[cite: 5]. [cite_start]This task demonstrates the ability to diagnose data health issues and apply systematic cleaning techniques[cite: 6].

## 🛠️ Key Responsibilities & Workflow
[cite_start]Following the industry-standard preprocessing pipeline[cite: 8, 9]:

1. [cite_start]**Data Ingestion**: Loaded the dataset using `pd.read_csv()` and performed sanity checks with `df.info()`[cite: 8].
2. [cite_start]**Deduplication**: Identified and removed redundant entries using `df.drop_duplicates()` to ensure data reliability[cite: 8].
3. [cite_start]**Column Management**: Dropped irrelevant features (e.g., job descriptions, IDs) and renamed columns for clarity using `df.drop()` and `df.rename()`[cite: 8].
4. **Missing Value Handling**: 
    * [cite_start]Diagnosed missingness patterns[cite: 9].
    * [cite_start]Applied imputation strategies: filling numerical gaps with the median and categorical gaps with the mode[cite: 9].
5. [cite_start]**Type Correction**: Converted salary data and ratings trapped as strings into proper numerical formats using `pd.to_numeric()`[cite: 9].
6. [cite_start]**Format Standardization**: Normalized text (lowercase/strip) and mapped categorical variants (e.g., standardizing job titles)[cite: 9].

## 🧠 Skills Gained
* [cite_start]**Advanced pandas Operations**: Mastery of data manipulation using DataFrames/Series[cite: 13].
* [cite_start]**Data Quality Assessment**: Ability to quantify and visualize data issues like missingness matrices[cite: 15].
* [cite_start]**Strategic Decision-Making**: Judgement in choosing between imputation and deletion based on context[cite: 17].
* [cite_start]**Efficiency Optimization**: Utilizing vectorized operations for large datasets[cite: 21].

## 🚀 Pro Tip: Validation
[cite_start]To prevent silent failures, I validated all changes using assertions[cite: 38]:
```python
assert df[col].isna().sum() == 0
assert df.duplicated().sum() == 0
