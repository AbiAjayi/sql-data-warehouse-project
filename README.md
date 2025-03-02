# SQL-Data-Warehouse-Project
Developing a data warehouse using SQL Server, covering ETL processes, data modeling, and analytics. This project demonstrates a comprehensive approach to data warehousing and analytics, from building the data warehouse to generating actionable insights. It showcases best practices in data engineering, including efficient data integration, schema design, and performance optimization. Additionally, it emphasizes using advanced analytics to turn raw data into meaningful business intelligence, ensuring data integrity, scalability, and effective reporting.

### Objective
Create a modern data warehouse using SQL Server to centralize sales data, enable analytical reporting, and support data-driven decision-making.

### Project Overview
This project involves: 
- Data Architecture: Designed a structured data pipeline with Bronze, Silver, and Gold layers.
- ETL Pipelines: Developed ETL processes to efficiently extract, transform, and load (ETL) data from source systems into the data warehouse.
- Data Modeling: Designed fact and dimension tables using industry best practices to support analytical queries and reporting.

### Data Architecture
The data architecture of this project follows the medallion architecture Bronze, Silver, and Gold layers:

![image](https://github.com/user-attachments/assets/cadbcc75-6d44-4d7d-b7ed-9e215ea86e3e)

1. Bronze Layer: This layer holds raw data sourced from CSV files, which were ingested into the SQL Server. No transformations or modeling were applied at this stage.

2. Silver Layer: In this phase, extensive data cleaning, transformation, and normalization were performed. New columns were derived, and data quality checks were conducted. Additionally, stored procedures were created for all table files to streamline processing.

3. Gold Layer: This layer contains integrated, cleaned, and business-ready data for reporting and analytics. A data model was developed using the star schema methodology, defining dimension and fact tables and their relationships. Views were created to simplify reporting and enhance user accessibility.

