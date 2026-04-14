
# SQL Data Cleaning & Power BI Visualization

### Data Wrangling and Business Intelligence Project

---

## 1. Project Overview

This project presents a complete workflow for transforming raw datasets into meaningful business insights using **SQL Server and Power BI**.

Two real-world datasets were used to demonstrate practical data handling challenges, including missing values, inconsistent formats, and invalid entries. The cleaned datasets were then visualized through interactive dashboards to highlight trends and patterns relevant to decision-making.

The work reflects a strong focus on **data preparation, accuracy, and insight generation**, which are critical stages in any data-driven project.

---

## 2. System Purpose

Raw data is rarely ready for analysis. In most real-world scenarios, datasets contain inconsistencies that can lead to misleading insights if not handled properly.

This project was carried out to demonstrate how structured data cleaning using SQL can:

* Improve data reliability and consistency
* Handle missing and invalid values effectively
* Standardize formats for analysis
* Prepare datasets for visualization tools

The final outcome shows how clean data can be used to produce **clear, meaningful, and actionable visual insights** in Power BI.

---

## 3. Core Workflow Design

The overall workflow follows a structured pipeline:

Raw Dataset (CSV)


SQL Server (Data Cleaning & Transformation using T-SQL)


Validated & Structured Tables


Power BI (Data Modelling & Visualization)


Interactive Dashboards & Reports

Each step was carefully executed to ensure that the transition from raw data to final insights remained consistent and accurate.

---

## 4. Dataset Handling Approach

### Task 1 - National Passenger Travel

This dataset focuses on transport trends across different modes such as passenger cars, buses, rail, and air.

Key cleaning steps included:

* Handling missing values across multiple columns
* Identifying and correcting invalid (negative) values
* Replacing NULL values with appropriate defaults
* Removing records that did not contribute meaningful information
* Verifying the dataset after cleaning

The final dataset was structured to support time-based trend analysis in Power BI.

---

### Task 2 - Jobs & Employment Data

This dataset contained employment statistics with formatting inconsistencies and placeholder values.

Key cleaning steps included:

* Converting placeholder values (e.g., `"--"`) into NULL
* Standardizing text fields for consistency
* Cleaning numeric columns by removing formatting issues (commas, strings)
* Converting data types into usable numeric formats
* Renaming and restructuring columns for clarity

This resulted in a dataset suitable for comparative and regional analysis.

---

## 5. Technical Implementation

The project primarily relied on **T-SQL** for data preparation.

Key techniques applied:

* NULL handling using `IS NULL`, `NULLIF()`, and `COALESCE()`
* Data validation and filtering
* String cleaning and transformation
* Type conversion using `TRY_CAST()`
* Schema modification using `ALTER TABLE`
* Column renaming and restructuring

These operations ensured that both datasets were clean, consistent, and analysis-ready.

---

## 6. Technology Stack

**Data Processing**

* Microsoft SQL Server
* T-SQL

**Data Visualization**

* Microsoft Power BI

**Data Source Format**

* CSV files

---

## 7. Key Features

* Structured data cleaning using SQL queries
* Handling of real-world messy datasets
* Transformation of raw data into analysis-ready format
* Interactive Power BI dashboards
* Clear visualization of trends and comparisons
* End-to-end data workflow from ingestion to insight

---

## 8. Project Structure

```
SQL-PowerBI-Assignment3/
│
├── T-SQL_Queries/
│   ├── Task 01.sql
│   └── Task 02.sql
│
├── SQL_Assignment3_Datasets/
│   ├── National Passenger Travel.csv
│   └── Jobs.csv
│
├── Power_BI_Dashboards/
│   ├── Task 01.pbix
│   └── Task 02.pbix
│
├── Power_BI_Reports/
│   ├── Task 01.pbix
│   └── Task 02.pbix
│
├── SQL_Assignment3_Report/
│   ├── Task 1.pdf
│   └── Task 2.pdf
│
└── README.md
```

---

## 9. Usage Guide

1. Open SQL Server Management Studio
2. Import the provided CSV datasets into the database
3. Execute the T-SQL scripts in the `T-SQL_Queries` folder
4. Verify the cleaned data tables
5. Open the `.pbix` files using Power BI Desktop
6. Explore the dashboards and interact with filters and visuals

---

## 10. Dashboard Insights

The Power BI dashboards were designed to highlight key findings from both datasets:

* Transport usage patterns across different modes
* Variations and trends over time
* Employment distribution across regions
* Comparative analysis of workforce data

These dashboards demonstrate how proper data preparation directly improves the quality of insights.

---

## 11. Academic & Practical Contribution

This project demonstrates:

* Practical application of SQL in data cleaning
* Understanding of real-world data issues
* Ability to transform raw data into structured formats
* Data visualization and storytelling using Power BI
* End-to-end data analysis workflow

It serves as a strong foundation for roles in:

* Data Analysis
* Business Intelligence
* Data Engineering (entry-level)

---

## 12. Limitations

* Data cleaning rules were applied based on assumptions due to lack of metadata
* No automation pipeline (manual execution required)
* Limited dataset size for deeper predictive analysis
* No integration with live or streaming data sources

---

## 13. Future Improvements

* Automating the ETL process
* Integrating real-time or larger datasets
* Adding advanced analytics or forecasting models
* Enhancing dashboard interactivity
* Connecting to cloud-based data platforms

---

## 14. Team

**CodeCrushers**
ADSC41 - 1st Year, 2nd Semester

