# Cafe Sales Data Cleaning & EDA Practice

## 📌 About This Project

This repository is a personal practice project where I'm working on improving my **data cleaning** and **exploratory data analysis (EDA)** skills using Python and pandas.

I'm currently a **beginner** in data science / data analysis, and this project is part of my learning-in-public journey. The goal is to take a messy, real-world-style dataset and practice:

- Handling missing values
- Identifying and fixing inconsistent data and error placeholders (e.g. `ERROR`, `UNKNOWN`)
- Standardizing column names and data types
- Converting columns to appropriate dtypes (e.g. strings → `int32`/`int64`/`float64`)
- Performing basic exploratory data analysis to understand patterns in the data

This is a learning exercise, not a production pipeline — so the code here reflects an evolving understanding of pandas and data cleaning techniques rather than a polished, final solution.

## 📊 Dataset Information

**Dataset Name:** Cafe Sales - Dirty Data for Cleaning Training
**Source:** [Kaggle](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training)
**Author:** Ahmed Mohamed
**License:** CC BY-SA 4.0

### Overview

The Dirty Cafe Sales dataset contains 10,000 rows of synthetic data representing sales transactions in a cafe. It's intentionally "dirty" — meaning it includes missing values, inconsistent formatting, and deliberately introduced errors — to simulate a realistic scenario for practicing data cleaning and EDA.

### File Details

| Detail | Value |
|---|---|
| File Name | `dirty_cafe_sales.csv` |
| Number of Rows | 10,000 |
| Number of Columns | 8 |

### Columns (approximate, based on dataset contents)

- Transaction ID
- Item
- Quantity
- Price Per Unit
- Total Spent
- Payment Method
- Location
- Transaction Date

> Note: Several columns contain placeholder error values like `"ERROR"` and `"UNKNOWN"` instead of proper missing-value markers (`NaN`), which is one of the key cleaning challenges this dataset is designed to teach.

## 🔗 How to Find This Dataset on Kaggle

1. Go to [kaggle.com](https://www.kaggle.com)
2. Search for **"Cafe Sales Dirty Data for Cleaning Training"**
3. Or use the direct link: [https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training](https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training)
4. Click **Download** to get the `dirty_cafe_sales.csv` file, or use the Kaggle API/CLI to download it directly into your working environment

## 🛠️ Tools & Libraries Used

- Python
- pandas
- NumPy
- Jupyter Notebook / JupyterLab

## 🎯 Goals of This Practice

- [x] Standardize column names (lowercase, underscores instead of spaces)
- [x] Replace placeholder error strings (`ERROR`, `UNKNOWN`) with proper `NaN` values
- [x] Convert numeric columns from string/object dtype to appropriate numeric dtypes
- [x] Handle missing values appropriately (drop, fill, or flag depending on context)
- [x] Parse and standardize date columns
- [x] Perform basic EDA — distributions, value counts, and summary statistics
- [x] Document findings and cleaning decisions clearly

## 🧹 Cleaning & Analysis Walkthrough

All data cleaning and analysis steps are documented in the Jupyter notebook [eda.ipynb](file:///c:/Users/user/OneDrive/Desktop/EDA-Practice/sales_data_cleaning/notebooks/eda.ipynb).

### 1. Data Exploration & Info
Using the helper function [print_basic_info](file:///c:/Users/user/OneDrive/Desktop/EDA-Practice/sales_data_cleaning/notebooks/eda.ipynb#L303-L314), we investigated the dataset structure:
- **Initial types**: All columns were read as `object` (string) due to dirty formatting/placeholders.
- **Missing values**: Identified significant missing data across columns (e.g. `location` had 3,265 missing values, `payment_method` had 2,579 missing values).

### 2. Data Cleaning & Normalization
Implemented in the function [normalize_data](file:///c:/Users/user/OneDrive/Desktop/EDA-Practice/sales_data_cleaning/notebooks/eda.ipynb#L438-L481):
- **Column Standardization**: Cleaned whitespaces, converted column titles to lowercase, and replaced spaces with underscores (`_`).
- **Text Standardization**: Standardized string fields (`item`, `payment_method`, `location`) to lowercase.
- **Dtype Correction**: Converted `price_per_unit`, `quantity`, and `total_spent` to float64, and `transaction_date` to datetime, turning errors like `ERROR` and `UNKNOWN` into `NaN`.
- **Handling Missing Values**: Imputed missing numeric fields (`price_per_unit`, `quantity`, `total_spent`) with their respective column mean.

### 3. Key Findings & Insights
Implemented in the function [perform_groupby_operations](file:///c:/Users/user/OneDrive/Desktop/EDA-Practice/sales_data_cleaning/notebooks/eda.ipynb#L542-L566):
- **Top Product by Revenue**: **Salad** generated the highest total revenue ($17,069.07 total revenue, mean spend per transaction is ~$14.87).
- **Most Popular Payment Method**: **Digital Wallet** (2,291 transactions).
- **Top Dining Choice**: **Takeaway** (3,022 transactions) compared to In-store.
- **Messy Item Placeholders**: The `item` column itself contained placeholder strings `"error"` (292 times) and `"unknown"` (344 times).

## 📝 Notes

This project is a work in progress and will be updated as I learn more about data cleaning, pandas, and EDA best practices. Feedback and suggestions are welcome!

---

*This dataset is used strictly for educational/practice purposes under its CC BY-SA 4.0 license.*