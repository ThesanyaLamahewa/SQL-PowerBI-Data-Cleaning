# 🗄️ SQL Data Cleaning & Power BI Visualization — ADSC41 Assignment 3

> **Course:** ADSC41 — Data Science (1st Year, 2nd Semester)  
> **Team:** CodeCrushers  
> **Tools:** Microsoft SQL Server (T-SQL) · Power BI · CSV Datasets

---

## 📌 Project Overview

This project demonstrates end-to-end **data wrangling and business intelligence** using two real-world datasets. We applied T-SQL for data cleaning and transformation, then built interactive Power BI dashboards to uncover meaningful insights.

---

## 📁 Repository Structure

```
📦 SQL-PowerBI-Assignment3
 ┣ 📂 T-SQL_Queries
 ┃ ┣ 📄 Task 01.sql          # Data cleaning — National Passenger Travel dataset
 ┃ ┗ 📄 Task 02.sql          # Data cleaning — Jobs/Employment dataset
 ┣ 📂 SQL_Assignment3_Datasets
 ┃ ┣ 📄 National Passenger Travel.csv
 ┃ ┗ 📄 Jobs.csv
 ┣ 📂 Power_BI_Dashboards
 ┃ ┣ 📄 Task 01.pbix          # Travel trends dashboard
 ┃ ┗ 📄 Task 02.pbix          # Employment statistics dashboard
 ┣ 📂 Power_BI_Reports
 ┃ ┣ 📄 Task 01.pbix
 ┃ ┗ 📄 Task 02.pbix
 ┣ 📂 SQL_Assignment3_Report.pdf
 ┃ ┣ 📄 Task 1.pdf            # Full written report — Task 1
 ┃ ┗ 📄 Task 2.pdf            # Full written report — Task 2
 ┗ 📄 README.md
```

---

## 🧹 Task 1 — National Passenger Travel Data Cleaning

**Dataset:** `National Passenger Travel.csv`  
**Database:** `Travel` (restored from `.bak`)

### What we did:
- ✅ Identified and handled **NULL values** across all transport mode columns (Passenger Cars, Buses, Rail, Air, Other, Total)
- ✅ Validated **data ranges** — flagged and handled negative values
- ✅ Replaced missing numerical values with `0` using `UPDATE` statements
- ✅ Removed irrelevant records where `Total = 0`
- ✅ Final verification query to confirm clean dataset

### Key T-SQL Techniques Used:
```sql
-- Detect missing values
SELECT * FROM dbo.[Travel]
WHERE [Passenger_cars] IS NULL OR [Rail] IS NULL ...;

-- Fill NULLs with 0
UPDATE dbo.[Travel]
SET [Passenger_cars] = 0
WHERE [Passenger_cars] IS NULL;

-- Remove zero-total rows
DELETE FROM dbo.[Travel] WHERE [Total] = 0;
```

---

## 💼 Task 2 — Jobs & Employment Data Cleaning

**Dataset:** `Jobs.csv`  
**Database:** `Task 02`

### What we did:
- ✅ Replaced placeholder `'--'` strings with proper `NULL` using `NULLIF()`
- ✅ Standardised text fields with `TRIM()` and `LOWER()`
- ✅ Cleaned numeric columns by removing commas and casting to `INT` using `TRY_CAST()` and `COALESCE()`
- ✅ Removed redundant/duplicate columns with `ALTER TABLE DROP COLUMN`
- ✅ Renamed columns for consistency using `sp_rename`
- ✅ Changed column data types to `INT` using `ALTER COLUMN`

### Key T-SQL Techniques Used:
```sql
-- Replace placeholder with NULL
UPDATE Jobs SET "Jan" = NULLIF("Jan", '--');

-- Clean and cast to integer
UPDATE Jobs
SET "Jan" = COALESCE(TRY_CAST(REPLACE("Jan", ',', '') AS INT), 0);

-- Rename column
EXEC sp_rename 'dbo.Jobs.[_2024_Total]', 'Total_2024', 'COLUMN';
```

---

## 📊 Power BI Dashboards

Interactive dashboards were built for both tasks to visualise the cleaned data:

| Dashboard | Dataset | Focus |
|-----------|---------|-------|
| Task 01 | National Passenger Travel | Transport mode trends over time |
| Task 02 | Jobs / Employment | Provincial employment statistics — 2024 |

> 📌 Open `.pbix` files using **Microsoft Power BI Desktop** (free download at [powerbi.microsoft.com](https://powerbi.microsoft.com))

---

## 🛠️ Technologies & Skills Demonstrated

| Skill | Details |
|-------|---------|
| **T-SQL / SQL Server** | Data cleaning, NULL handling, type casting, schema modification |
| **Power BI** | Dashboard design, data modelling, interactive reports |
| **Data Wrangling** | Handling real-world messy data (missing values, wrong types, placeholders) |
| **Teamwork** | Group assignment with peer evaluation |

---

## 👥 Team — CodeCrushers

> ADSC41 · 1st Year, 2nd Semester

---

## 📄 License

This project was created for academic purposes as part of the ADSC41 coursework.
