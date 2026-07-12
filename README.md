# Muzica Data Engineering Pipeline
End-to-End Data Engineering Pipeline using Databricks, PySpark, SQL, and Delta Lake
## Project Overview

Muzica is a simulated music streaming platform inspired by applications like Spotify. This project demonstrates how raw streaming data can be ingested, cleaned, transformed, and analyzed using a modern Data Engineering pipeline built on Databricks.

The project follows the Medallion Architecture (Bronze → Silver → Gold) to organize data through different stages of processing and produce business-ready datasets.

## Business Problem

Music streaming platforms generate thousands of listening events every day. Raw data often contains duplicate records, missing values, and inconsistent formats, making it unsuitable for business reporting.

The objective of this project is to build an end-to-end ETL pipeline that transforms raw streaming data into reliable datasets that business teams can use for analytics and decision-making.

## Solution

The pipeline performs the following tasks:

Generate realistic music streaming data
Ingest raw CSV data into Databricks
Store raw data in the Bronze layer
Clean and standardize data using PySpark
Store cleaned data in the Silver layer using Delta Lake
Create business-ready Gold tables
Analyze data using SQL
## Project Architecture

```text
Generated Streaming Data (CSV)
            │
            ▼
Databricks Workspace
            │
            ▼
Bronze Layer (Raw Data)
            │
            ▼
PySpark Transformations
    ├── Remove duplicates
    ├── Handle missing values
    └── Standardize genres
            │
            ▼
Silver Layer (Clean Data)
            │
            ▼
Business Aggregations
            │
            ▼
Gold Layer
    ├── Top Artists
    ├── Genre Popularity
    └── Country Streams
            │
            ▼
SQL Analysis
```
## Technology Stack
Technology	Purpose
Python	Generate sample streaming data
PySpark	Data cleaning and transformation
SQL	Business analysis
Databricks	Cloud data engineering platform
Delta Lake	Reliable storage for processed data
Git & GitHub	Version control and project portfolio
## Project Structure

```text
muzica-data-engineering-pipeline/
│
├── data/
│   ├── bronze/
│   ├── silver/
│   └── gold/
│
├── notebooks/
│   ├── 01_ingest_bronze.ipynb
│   ├── 02_transform_silver.ipynb
│   ├── 03_create_gold.ipynb
│   └── 04_business_analysis.ipynb
│
├── scripts/
│   └── generate_streaming_data.py
│
├── sql/
│   └── business_queries.sql
│
├── images/
│
├── README.md
└── requirements.txt
```
## ETL Pipeline
Bronze Layer
Loaded raw streaming CSV into Databricks
Preserved original data without modification
Silver Layer
Removed duplicate records
Handled missing values
Standardized genre values
Created clean Delta table
Gold Layer

Created business-ready datasets:

Top Artists
Genre Popularity
Country-wise Streams
## SQL Analysis

Example business questions answered:

Which artists receive the most streams?
Which genre is the most popular?
Which countries generate the highest streaming activity?
Who are the top 3 artists by total streams?
## Key Learnings

Through this project I learned:

Building an end-to-end ETL pipeline
Working with Databricks notebooks
Reading and transforming data using PySpark
Implementing the Medallion Architecture
Creating Delta Lake tables
Writing SQL for business analytics
Organizing a Data Engineering project using GitHub
## Future Improvements
Automate the pipeline using Databricks Workflows
Process incremental data instead of full loads
Connect the Gold layer to a BI dashboard
Add data quality validation tests
Deploy the pipeline on a cloud platform such as Azure or AWS
## Author

Deshni Stanley

This project was created as part of my Data Engineering learning journey to strengthen my understanding of ETL pipelines, Databricks, PySpark, SQL, and Delta Lake while preparing for Data Engineering and Analytics roles.
