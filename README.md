# SQL-Data-Warehouse-Project
## 1. Introduction
### 1.1 Project Overview
This project focuses on developing a data warehouse using SQL Server to centralize sales data, enable analytical reporting, and support data-driven decision-making. The project follows best practices in data engineering, including efficient data integration, schema design, and performance optimization. It transforms raw data into actionable insights through advanced analytics while ensuring data integrity and scalability.

### 1.2 Business Problem
Organizations face challenges in managing large-scale data efficiently. These include:
-	Disparate data sources leading to inefficiencies in analysis.
-	Poor data quality affecting business decision-making.
-	Performance issues in querying large datasets.
A structured data warehouse addresses these challenges by providing a centralized repository with clean, business-ready data.

## 2. Data Architecture
### 2.1 Medallion Architecture (Bronze, Silver, Gold Layers)
The project adopts a multi-layered approach:
-	Bronze Layer: Raw data ingestion from CSV files into SQL Server without transformations.
-	Silver Layer: Data cleaning, transformation, normalization, and quality checks.
-	Gold Layer: Business-ready, structured data optimized for reporting using the Star Schema.
### 2.2 Schema Design
The data warehouse schema follows the Star Schema approach with:
-	Fact Table: Sales Transactions (OrderID, CustomerID, ProductID, Amount, Date)
-	Dimension Tables: Customers, Products, Time, Locations
### 2.3 Data Sources
Data is ingested from:
-	CSV Files containing transactional sales data.
-	ERP Files

## 3. ETL Process
### 3.1 Data Extraction
-	CSV files are loaded into staging tables using SQL Server’s BULK INSERT.
-	Data is extracted from transactional databases.
### 3.2 Data Transformation
-	Standardization of column formats.
-	Handling missing values and duplicate records.
-	Derived column creation and normalization.
### 3.3 Data Loading
-	Stored Procedures used to transform and load data into the Gold Layer.
-	Indexing and partitioning techniques applied for performance optimization.




![image](https://github.com/user-attachments/assets/cadbcc75-6d44-4d7d-b7ed-9e215ea86e3e)

1. Bronze Layer: This layer holds raw data sourced from CSV files, which were ingested into the SQL Server. No transformations or modeling were applied at this stage.

2. Silver Layer: In this phase, extensive data cleaning, transformation, and normalization were performed. New columns were derived, and data quality checks were conducted. Additionally, stored procedures were created for all table files to streamline processing.

3. Gold Layer: This layer contains integrated, cleaned, and business-ready data for reporting and analytics. A data model was developed using the star schema methodology, defining dimension and fact tables and their relationships. Views were created to simplify reporting and enhance user accessibility.

