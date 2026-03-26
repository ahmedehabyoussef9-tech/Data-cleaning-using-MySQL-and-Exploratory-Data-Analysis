# MySQL Data Cleaning Project

## Overview

This project focuses on cleaning a real-world dataset using SQL. The goal was to transform raw, inconsistent data into a structured and analysis-ready format.

The dataset contains company layoff data, which required multiple cleaning steps before it could be used for analysis.

---

## Dataset

* Source: Layoffs dataset (Excel file included in repository)
* Tool used: MySQL

---

## Data Cleaning Steps

### 1. Remove Duplicates

* Identified duplicate rows using `ROW_NUMBER()` with `PARTITION BY`
* Created a staging table to safely manipulate data
* Removed duplicate records by keeping only the first occurrence

---

### 2. Standardize the Data

* Removed leading/trailing spaces using `TRIM()`
* Standardized inconsistent values (e.g., "Crypto%" → "Crypto")
* Cleaned country names (removed extra characters like periods)
* Converted date column from text to proper `DATE` format using `STR_TO_DATE()`

---

### 3. Handle Null and Blank Values

* Identified missing or blank values
* Cleaned or updated values where necessary
* Ensured consistency across columns

---

## Key Skills Demonstrated

* Data cleaning using SQL
* Window functions (`ROW_NUMBER()`)
* String functions (`TRIM`, `LIKE`)
* Data standardization techniques
* Data type conversion
* Working with staging tables

---

## Project Structure

* SQL scripts for each step of cleaning
* Original dataset (Excel)
* Cleaned dataset (after processing)

---

## Next Step

The cleaned dataset will be used for **Exploratory Data Analysis (EDA)** to extract insights and trends.
