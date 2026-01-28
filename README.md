# zepto_sql
Zepto customer shopping dataset imported directly into PostgreSQL using pgAdmin for SQL practice and analysis.
# Zepto Customer Shopping Dataset – PostgreSQL Project

This repository contains a Zepto customer shopping dataset that was imported
directly into PostgreSQL using pgAdmin.  
No Python or ETL tools were used for data loading.

## Repository Contents

- `ZEPTO.csv`  
  Original customer shopping dataset.

- `zepto_dataset.sql`  
  SQL schema / dump file of the Zepto table created in PostgreSQL.

- `README.md`  
  Project documentation.

## Dataset Description

The dataset represents customer shopping behavior data from Zepto.
It includes transaction-level and customer-related information that can be
used for analysis and SQL practice.

## Data Loading Method

The dataset was imported **directly into PostgreSQL** using **pgAdmin**.

### Steps Followed

1. Created a database in PostgreSQL.
2. Created a schema and a table named `zepto`.
3. Imported the CSV file using:
   - pgAdmin → Schemas → Tables → Import/Export Data
4. Verified the data using SQL queries.

⚠️ Python was **not used** at any stage.

## Database Details

- Database Type: PostgreSQL
- Tool Used: pgAdmin
- Table Name: `zepto`
- Import Method: Direct CSV import

## Sample SQL Queries

```sql
-- View first 10 records
SELECT * FROM zepto
LIMIT 10;

-- Count total records
SELECT COUNT(*) FROM zepto;

-- Example analysis
SELECT category, COUNT(*) AS total_orders
FROM zepto
GROUP BY category;
