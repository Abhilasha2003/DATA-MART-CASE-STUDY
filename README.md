#  SQL Case Study: Data Mart Analysis

##  Introduction
This case study focuses on analyzing the sales performance of **Data Mart**, a venture that adopted sustainable packaging in June 2020. The goal was to evaluate sales trends and performance across regions, platforms, and demographics before and after this major change.

Using SQL (MySQL Workbench), I performed **data cleansing** and answered **7 business questions** through structured queries on the `weekly_sales` dataset.

---

##  Schema Used: `weekly_sales`

| Column Name      | Data Type  |
|------------------|------------|
| week_date        | DATE       |
| region           | VARCHAR(20)|
| platform         | VARCHAR(20)|
| segment          | VARCHAR(10)|
| customer         | VARCHAR(20)|
| transactions     | INT        |
| sales            | INT        |

---

##  Part A: Data Cleaning Steps

Performed all transformations in a single SQL query and created a new table `clean_weekly_sales`. Key operations included:

- Extracted `week_number`, `month_number`, and `calendar_year` from `week_date`
- Mapped segment codes to `age_band` (e.g., '1' = Young Adults)
- Derived `demographic` based on segment prefix ('C' = Couples, 'F' = Families)
- Replaced all `NULL` and empty values with `'unknown'`
- Created a new column `avg_transaction` as `sales ÷ transactions` (rounded to 2 decimal places)

---

##  Part B: Data Exploration

Answered the following questions using advanced SQL queries:

1.  **Missing Week Numbers**  
   → Identified missing week numbers to find gaps in data collection

2.  **Total Transactions by Year**  
   → Summed transactions grouped by calendar year

3.  **Monthly Sales by Region**  
   → Analyzed regional performance by month

4.  **Total Transactions by Platform**  
   → Compared Retail vs Shopify

5.  **Monthly Sales Percentage – Retail vs Shopify**  
   → Calculated platform-wise sales share for each month using `CASE` and `CTE`

6.  **Sales Percentage by Demographic (Yearly)**  
   → Used `PARTITION BY` to find each demographic’s sales distribution across years

7.  **Top-Contributing Age Bands & Demographics**  
   → Identified the highest-performing customer segments

---

## 🛠 Tools Used
- **MySQL Workbench**
- SQL (Joins, CTEs, CASE, Aggregates, Window Functions)

---

##  Key Learnings
- Performed real-world data transformation and reporting entirely in SQL
- Gained hands-on experience with `CTEs`, `CASE`, `GROUP BY`, and `PARTITION BY`
- Understood how to draw insights from sales data using pure SQL

---

## 📎 File Included
- `data_mart_case_study.sql`: All SQL queries including data cleaning and exploration




