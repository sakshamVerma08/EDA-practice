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

- [ ] Standardize column names (lowercase, underscores instead of spaces)
- [ ] Replace placeholder error strings (`ERROR`, `UNKNOWN`) with proper `NaN` values
- [ ] Convert numeric columns from string/object dtype to appropriate numeric dtypes
- [ ] Handle missing values appropriately (drop, fill, or flag depending on context)
- [ ] Parse and standardize date columns
- [ ] Perform basic EDA — distributions, value counts, and summary statistics
- [ ] Document findings and cleaning decisions clearly

## 📝 Notes

This project is a work in progress and will be updated as I learn more about data cleaning, pandas, and EDA best practices. Feedback and suggestions are welcome!

---

*This dataset is used strictly for educational/practice purposes under its CC BY-SA 4.0 license.*