# Assignment 2 – Dataset Quality KPI Analysis

## Overview

This project analyzes the **Online Retail dataset** to evaluate the **quality of the data using Key Performance Indicators (KPIs)**.

The objective is to explore **how noisy the dataset is** and how this noise may affect data analysis and KPI calculations.


---

## Dataset Description

The dataset contains **541,909 transactions** from an online retail store between **December 2010 and December 2011**.

Main columns:

* InvoiceNo
* StockCode
* Description
* Quantity
* InvoiceDate
* UnitPrice
* CustomerID
* Country

---

## Data Quality KPIs

### 1. Data Completeness

Missing values were measured for each column.

* Description: **0.27% missing**
* CustomerID: **24.93% missing**

The **CustomerID** column contains the most missing data, which limits customer-level analysis.

### 2. Duplicate Records

Duplicate rate: **0.97%**

Duplicate rows may distort KPI calculations such as total sales and number of transactions.

### 3. Outliers

Outliers were identified in **UnitPrice** using the **IQR method**.

Outlier rate: **7.31%**

These values may correspond to unusual transactions or possible data errors.

### 4. Data Accuracy

The following checks were used:

* Quantity > 0
* UnitPrice > 0
* CustomerID not null

**Data Accuracy Rate: 73.42%**

### 5. Reference Data Validation

Country values were compared with a reference list.

**Country match rate: 97.18%**

---

## Results Summary

* Missing CustomerID: **24.93%**
* Duplicate Rate: **0.97%**
* Outlier Rate (UnitPrice): **7.31%**
* Data Accuracy Rate: **73.42%**
* Country Match Rate: **97.18%**

---

## Conclusion

The dataset contains several sources of noise.

The most important issue is the **high percentage of missing CustomerID values**, which limits customer behavior analysis.

Other smaller issues include **duplicate records** and **price outliers**, which may affect KPI calculations.

Overall, the dataset is usable, but data cleaning is recommended before deeper analysis.
