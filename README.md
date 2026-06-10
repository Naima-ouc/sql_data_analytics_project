# SQL Data Analytics Project

## Project Overview

This project focuses on SQL-based data analysis using sales data from CRM and ERP source systems. The goal is to explore the data, calculate business metrics, identify trends, and generate insights around customers, products, and sales performance.

The analysis is based on prepared datasets from a related SQL Data Warehouse project. While the data warehouse project focuses on data ingestion, cleaning, transformation, and modeling, this repository focuses on using the prepared data for business analysis and reporting.

I rebuilt this project as part of my data analytics learning journey to practice translating business questions into SQL queries and analytical reports.

Related project:

[`sql-data-warehouse-project`] (https://github.com/Naima-ouc/sql_data_warehouse_project)

---

## Business Questions

This project answers analytical questions such as:

* How many customers, products, and orders are available in the dataset?
* What is the overall sales performance?
* Which products generate the highest revenue?
* Which customers contribute the most to sales?
* How do sales change over time?
* What are the monthly and yearly sales trends?
* Which product categories contribute most to total revenue?
* How can customers and products be segmented based on performance?
* Which customers and products should be prioritized for reporting?

---

## Analysis Areas

The SQL scripts are organized from basic exploration to more advanced analytical techniques.

### 1. Database Exploration

The first scripts explore the structure of the database, available tables, columns, and metadata.

### 2. Dimensions Exploration

These queries analyze categorical fields such as countries, categories, subcategories, products, and customer attributes.

### 3. Date Range Exploration

This section identifies the available time period in the dataset and checks the range of order dates, birth dates, and other date-related fields.

### 4. Measures Exploration

These queries calculate key metrics such as total sales, total quantity, average price, number of orders, number of customers, and number of products.

### 5. Magnitude Analysis

Magnitude analysis compares values across categories, such as sales by country, category, product, or customer group.

### 6. Ranking Analysis

Ranking queries identify top and bottom performers, such as best-selling products, highest-revenue customers, and underperforming categories.

### 7. Change Over Time Analysis

These queries analyze trends across time periods and help identify how business performance develops over months and years.

### 8. Cumulative Analysis

Cumulative analysis calculates running totals and moving averages to understand long-term growth and performance patterns.

### 9. Performance Analysis

Performance analysis compares products, customers, or time periods against averages or previous results to identify overperformance and underperformance.

### 10. Data Segmentation

Segmentation groups customers and products into meaningful categories based on business logic, such as spending behavior or product performance.

### 11. Part-to-Whole Analysis

Part-to-whole analysis calculates how much each category, product, or segment contributes to the overall total.

### 12. Customer Report

The customer report combines multiple metrics into a customer-level analytical view, including customer value, order behavior, and segmentation.

### 13. Product Report

The product report creates a product-level analytical view to evaluate sales performance, product contribution, and business relevance.

---

## SQL Techniques Used

This project demonstrates the use of:

* SELECT statements
* Filtering with WHERE
* Aggregations with SUM, COUNT, AVG, MIN, and MAX
* GROUP BY and ORDER BY
* Joins
* CASE statements
* Common Table Expressions
* Window functions
* Ranking functions
* Date functions
* Running totals
* Moving averages
* Part-to-whole calculations
* Customer and product segmentation

---

## Dataset

The repository contains CSV exports from different stages of the data pipeline:

* *Bronze datasets:* Raw source data from CRM and ERP systems.
* *Silver datasets:* Cleaned and standardized data.
* *Gold datasets:* Business-ready analytical tables.
* *Report datasets:* Final customer and product report outputs.

These datasets are stored in:

text
datasets/csv-files/


The Gold Layer datasets are the main basis for the analytical SQL scripts.

---

## Repository Structure

```text
sql-data-analytics-project/
│
├── datasets/                              # CSV datasets used for the analysis
│   ├── placeholder                        # Keeps the datasets folder visible in GitHub
│   └── csv-files/                         # Bronze, Silver, Gold, and report CSV files
│       ├── bronze.crm_cust_info.csv
│       ├── bronze.crm_prd_info.csv
│       ├── bronze.crm_sales_details.csv
│       ├── bronze.erp_cust_az12.csv
│       ├── bronze.erp_loc_a101.csv
│       ├── bronze.erp_px_cat_g1v2.csv
│       ├── silver.crm_cust_info.csv
│       ├── silver.crm_prd_info.csv
│       ├── silver.crm_sales_details.csv
│       ├── silver.erp_cust_az12.csv
│       ├── silver.erp_loc_a101.csv
│       ├── silver.erp_px_cat_g1v2.csv
│       ├── gold.dim_customers.csv
│       ├── gold.dim_products.csv
│       ├── gold.fact_sales.csv
│       ├── gold.report_customers.csv
│       └── gold.report_products.csv
│
├── scripts/                               # SQL scripts for exploration and analysis
│   ├── 00_init_database.sql               # Initializes the analytics database
│   ├── 01_database_exploration.sql        # Explores database objects and metadata
│   ├── 02_dimensions_exploration.sql      # Explores categorical dimensions
│   ├── 03_date_range_exploration.sql      # Analyzes available date ranges
│   ├── 04_measures_exploration.sql        # Calculates basic business measures
│   ├── 05_magnitude_analysis.sql          # Compares values across categories
│   ├── 06_ranking_analysis.sql            # Identifies top and bottom performers
│   ├── 07_change_over_time_analysis.sql   # Analyzes trends over time
│   ├── 08_cumulative_analysis.sql         # Calculates running totals and moving averages
│   ├── 09_performance_analysis.sql        # Compares performance across entities and periods
│   ├── 10_data_segmentation.sql           # Segments customers and products
│   ├── 11_part_to_whole_analysis.sql      # Calculates contribution to total values
│   ├── 12_report_customers.sql            # Creates a customer-level report
│   └── 13_report_products.sql             # Creates a product-level report
│
├── README.md                              # Project overview and documentation
└── LICENSE                                # MIT License from the original project
```

---

## How to Use This Repository

1. Clone or download this repository.
2. Open the SQL scripts in SQL Server Management Studio.
3. Run scripts/00_init_database.sql to initialize the analytics database.
4. Load or connect the CSV datasets from datasets/csv-files/.
5. Run the SQL scripts in numerical order.
6. Review the query results to understand sales, customer, and product performance.

---

## Skills Demonstrated

* Exploring relational datasets with SQL
* Translating business questions into SQL queries
* Calculating business KPIs
* Analyzing sales trends over time
* Ranking customers and products by performance
* Segmenting customers and products
* Creating reusable customer and product reports
* Using SQL for business-oriented data analysis
* Documenting an analytics project for portfolio use

---

## Project Status

This project is part of my personal data analytics portfolio. It demonstrates how SQL can be used to explore prepared business data, calculate KPIs, identify trends, and create analytical reports.

The project is connected to my SQL Data Warehouse project, where the source data was prepared using a Bronze, Silver, and Gold Layer approach.

---

## Credits and License

This project was inspired by the SQL Data Analytics project by DataWithBaraa.

I rebuilt and adapted the project for learning and portfolio purposes, using it to practice SQL-based exploration, business analysis, reporting logic, and portfolio documentation.

Original project: DataWithBaraa/sql-data-analytics-project

This repository includes code and project structure based on the original MIT-licensed project. The original license notice is included in the LICENSE file.
