# 🚕 ZoomRide_SQL_Data_Analysis
A MySQL data analysis project focused on understanding ZoomRide trip patterns, revenue performance, customer behavior, and data quality across multiple cities

## 📌 Project Overview

This project is a **SQL data analysis project** based on a fictional ride-hailing company, **ZoomRide**, operating across six African cities.

The project uses **MySQL** to analyze trip activity, revenue, customers, drivers, vehicle types, and data quality issues. The dataset contains deliberately messy real-world-style data, providing an opportunity to demonstrate SQL querying, data cleaning, aggregation, joins, duplicate detection, and business-focused analysis.

The analysis was completed as part of a **Week 2 SQL Data Analysis project**.

---

## 🎯 Business Objective

The main objective was to use SQL to answer important business questions that could help ZoomRide understand its operations and make better investment decisions.

### Key business questions

* Which month has the highest number of trips?
* Which vehicle type generates the most revenue?
* How many trip records are in the dataset?
* What are the five longest completed trips?
* How many trips does each city have?
* Are there duplicate trip records?
* How many completed trips have missing fares?
* What data quality problems exist?
* Which city generates the most revenue?
* Which month generates the most revenue?
* Which vehicle type generates the most revenue?
* Which customers have never booked a trip?
* Who are the top three customers by total spending?

---

## 🗂️ Dataset

The database contains three related tables:

### 1. Customers

Contains information about ZoomRide customers.

| Column           | Description                  |
| ---------------- | ---------------------------- |
| `customer_id`    | Unique customer identifier   |
| `customer_name`  | Customer name                |
| `home_city`      | Customer's home city         |
| `signup_date`    | Date the customer registered |
| `signup_channel` | Customer acquisition channel |

### 2. Drivers

Contains information about ZoomRide drivers.

| Column         | Description                 |
| -------------- | --------------------------- |
| `driver_id`    | Unique driver identifier    |
| `driver_name`  | Driver name                 |
| `city`         | Driver's operating city     |
| `vehicle_type` | Type of vehicle             |
| `rating`       | Driver rating               |
| `joined_date`  | Date driver joined ZoomRide |

### 3. Trips

Contains individual ride transactions linking customers and drivers.

| Column           | Description                  |
| ---------------- | ---------------------------- |
| `trip_id`        | Unique trip identifier       |
| `customer_id`    | Customer who booked the trip |
| `driver_id`      | Driver assigned to the trip  |
| `city`           | Trip city                    |
| `trip_date`      | Date of trip                 |
| `distance_km`    | Trip distance                |
| `fare`           | Trip fare in Naira           |
| `status`         | Completed or Cancelled       |
| `payment_method` | Payment method               |

The original dataset contains **300 trip records** before data cleaning.

---

## 🛠️ Tools Used

* **MySQL**
* SQL
* OneCompiler MySQL environment
* GitHub

### SQL techniques used

* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `HAVING`
* `COUNT()`
* `SUM()`
* `MONTH()`
* `MONTHNAME()`
* `JOIN`
* `LEFT JOIN`
* `IS NULL`
* `TRIM()`
* `UPDATE`
* `DELETE`
* `LIMIT`

---

## 🧹 Data Cleaning

The dataset was intentionally created with several data quality problems.

### 1. Inconsistent city names

The same cities appeared under different names, for example:

* `PH` → `Port Harcourt`
* `Port-Harcourt` → `Port Harcourt`
* `Nairobbi` → `Nairobi`
* `Kampla` → `Kampala`
* Leading spaces such as `' Lagos'` and `' Accra'`

These inconsistencies were cleaned using `TRIM()` and `UPDATE` statements.

### 2. Duplicate trip record

A duplicate trip record was identified and removed.

The duplicate was:

* Trip `72`
* Trip `299`

Trip `299` was the later duplicate record and was removed.

### 3. Missing fare values

Some completed trips contained `NULL` fares.

These values were identified but **not replaced with invented values**, because there was insufficient information to determine the correct fare.

---

## 📊 Key Findings

After cleaning the city names and removing the duplicate trip, the city-level analysis showed:

| City          |   Trips |      Revenue |
| ------------- | ------: | -----------: |
| **Lagos**     | **105** | **₦218,890** |
| Accra         |      44 |      ₦92,640 |
| Port Harcourt |      41 |      ₦73,860 |
| Abuja         |      40 |      ₦88,720 |
| Nairobi       |      38 |      ₦58,960 |
| Kampala       |      31 |      ₦38,020 |

### 🥇 Top-performing city: Lagos

Lagos recorded the highest number of trips with **105 trips** and generated approximately **₦218,890 in revenue**.

This makes Lagos the strongest candidate for additional investment based on the available trip volume and revenue data.

---

## 💡 Business Recommendation

Based on the analysis, **ZoomRide should consider prioritizing Lagos for further investment**.

Lagos has both the highest trip volume and highest revenue among the six cities analyzed. Additional investment could focus on areas such as driver availability, customer acquisition, service reliability, and operational capacity.

However, revenue alone should not determine a major investment decision. Before committing significant resources, ZoomRide should also examine **operating costs, profit margins, customer retention, demand growth, driver availability, and cancellation rates** by city.

---

## 🔍 Data Quality Lessons

This project demonstrated why data cleaning is an important part of data analysis.

If city names such as `PH`, `Port Harcourt`, and `Port-Harcourt` were not standardized, the same city would appear as multiple cities in reports. This could lead to incorrect trip counts, revenue comparisons, and potentially poor business decisions.

Duplicate records could also cause trip volume and revenue to be overstated.

---

## 📁 Project Structure

```text
zoomride-sql-data-analysis/
│
├── zoomride_setup.sql
├── README.md
└── queries/
    └── zoomride_analysis.sql
```

---

## 🚀 SQL Analysis Workflow

The project followed this workflow:

```text
Understand the dataset
        ↓
Explore tables and records
        ↓
Answer business questions
        ↓
Identify data quality issues
        ↓
Clean inconsistent city names
        ↓
Identify and remove duplicate record
        ↓
Check missing values
        ↓
Re-run analysis
        ↓
Generate business insights
        ↓
Make recommendations
```

---

## 📈 Skills Demonstrated

This project demonstrates my ability to:

* Write SQL queries to answer business questions
* Aggregate and summarize large datasets
* Use joins across related tables
* Identify duplicate records
* Detect missing values
* Clean inconsistent categorical data
* Analyze revenue and trip performance
* Translate SQL results into business insights

---

## 👤 Author

**Nkechika Julian Nnodiogu**

Data Analyst | Data Scientist | Medical Laboratory Scientist

### Areas of Interest

* Data Analytics
* Data Science
* SQL
* Python
* Business Intelligence
* Machine Learning
portfolio-project
```
