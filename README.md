## World Layoffs Data Analysis (MySQL)

# Project Overview

This project focuses on **data cleaning and exploratory data analysis (EDA)** using a real-world layoffs dataset.
The goal was to transform raw, inconsistent data into a clean and reliable dataset, then extract meaningful insights about global layoffs trends across companies, industries, and time.

---

# Objectives

* Clean and standardize raw data using SQL
* Handle missing and inconsistent values
* Remove duplicates to ensure data accuracy
* Perform exploratory data analysis to uncover trends and patterns
* Identify key factors influencing layoffs (company, industry, location, time)

---

# Tools & Technologies

* **MySQL** – Data cleaning & analysis
* **SQL (Window Functions, CTEs, Aggregations)**
* **Excel** – Source dataset (uploaded in repository)

---

# Data Cleaning Process

The dataset required several preprocessing steps before analysis:

### 1. Removing Duplicates

* Used `ROW_NUMBER()` with `PARTITION BY` to identify duplicate rows
* Stored cleaned data in a staging table
* Deleted duplicate records safely

### 2. Standardizing Data

* Trimmed extra spaces in text fields (`company`, `country`)
* Unified inconsistent values (e.g., *Crypto-related labels*)
* Converted `date` column from text to proper `DATE` format

### 3. Handling Missing Values

* Replaced blank values with `NULL`
* Filled missing `industry` values using self-joins
* Removed rows with insufficient data (both layoffs and percentage missing)

### 4. Removing Unnecessary Columns

* Dropped helper columns (e.g., `row_num`) after processing

---

##  Exploratory Data Analysis (EDA)

After cleaning, several analyses were performed to uncover insights:

###  General Insights

* Identified **maximum layoffs** in a single event
* Analyzed **percentage layoffs**, including companies with **100% workforce reduction**
* Observed that many fully laid-off companies were **startups**

---

### Company-Level Analysis

* Top companies with the **highest total layoffs**
* Companies with the **largest single-day layoffs**

---

###  Geographic Analysis

* Layoffs aggregated by:

  * Location
  * Country

---

###  Industry & Stage Analysis

* Industries most affected by layoffs
* Company stages (e.g., startup vs late-stage) and their layoff trends

---

###  Time-Based Analysis

* Yearly layoffs trend
* Monthly layoffs with **rolling total calculation**
* Top 3 companies with the highest layoffs **per year** using `DENSE_RANK()`

---

##  Key Insights

* Certain industries (e.g., tech & crypto) experienced significant layoffs
* Layoffs peaked during specific years, indicating economic or market shifts
* Startups showed higher chances of **complete shutdown (100% layoffs)**
* A small number of companies contributed disproportionately to total layoffs

---

##  Dataset

* Source dataset is included in this repository as an **Excel file**
* Contains company, industry, layoffs, funding, and date information

---

##  How to Use

1. Import the dataset into MySQL
2. Run the data cleaning queries
3. Execute EDA queries to reproduce insights
4. Modify queries to explore additional patterns

---

##  Future Improvements

* Add data visualization (Power BI / Tableau / Python)
* Build an interactive dashboard
* Perform predictive analysis on layoffs trends

---

##  Author

**Ahmed Ehab Youssef**
Aspiring Data Analyst | SQL | Data Cleaning | EDA

---

##  Project Value

This project demonstrates:

* Strong SQL skills
* Real-world data cleaning techniques
* Analytical thinking using EDA
* Ability to extract actionable insights from raw data

---

