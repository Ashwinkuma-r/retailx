# RetailX

## Objective
Design and implement an end-to-end data pipeline on Databricks as part of an Oracle to Databricks migration using best practices.

## Architecture
Oracle (simulated via CSV)
* Bronze (Raw Delta Tables)
* Silver (Cleaned & Validated Data)
* Gold (Business Aggregations)

## Technologies Used
* Databricks Community Edition
* Delta Lake
* Unity Catalog
* Auto Loader (conceptual)
* Delta Live Tables (conceptual)
* Lakebridge (Analyzer & Transpiler – conceptual)

## Assignment Mapping

### A1. Unity Catalog Setup
Created catalog and schemas: bronze, silver, gold

### B1. Lakeflow Connect (Simulated)
Orders data ingested as raw CSV simulating Oracle extracts

### B2. Auto Loader (Simulated)
Customers data ingested using file-based ingestion

### C1. Silver Transformations
* Null checks
* Datatype corrections
* Email validation
* Outlier filtering

### C2. Gold Aggregations
Daily sales summary from Silver orders

### D1. Delta Live Tables
Declarative DLT pipeline with expectations

### E1. Data Quality Checks
Null, datatype mismatch, pattern, outlier checks

### F1 & F2. Lakebridge Migration
Logic transpiled into Spark SQL

### Job Pipeline
A Databricks Job pipeline was created to orchestrate the execution of Bronze, Silver, and Gold notebooks, representing production-style scheduling and dependency management.

## Notes
Due to environment limitations, Oracle connectivity, Lakeflow UI, and DLT pipelines were simulated. The solution reflects real-world Databricks migration design.
