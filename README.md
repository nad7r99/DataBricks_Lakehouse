# DataBricks_Lakehouse

Databricks Lakehouse Project repository
The project demonstrates an End-To-End Modern Data Engineering workflow using Databricks, PySpark, Delta Lake, SQL,and the Medallion Architecture (Bronze, Silver, and Gold layers).

The goal of this project is to ingest raw data from CRM and ERP CSV source files, transform it into clean analytical datasets, and model it into a Orders using a Star Schema for reporting and analytics.


# Data Architecture

The data architecture for this project follows the Medallion Architecture using Bronze, Silver, and Gold layers:



1.Bronze Layer
  Stores raw data as-is from the source systems with minimal transformation.
  CSV files from CRM and ERP are ingested into Bronze Delta tables.

2.Silver Layer
  Applies data cleansing, standardization, null handling, date formatting, column renaming, and duplicate checks.
  This layer prepares clean and trusted data for downstream modeling.

3.Gold Layer
  Builds business-ready analytical tables in the form of:

    gold_fact_orders
    gold_dim_customers
    gold_dim_products
    gold_dim_stream
    gold_dim_tickets

These tables are optimized for reporting, analytics, and dashboarding.



# Project Overview :

 This project includes:

  1.Lakehouse Design
    Building a modern Lakehouse solution in Databricks using Bronze, Silver, and Gold layers.

  2.Batch Ingestion
    Loading CRM and ERP CSV source files into the Bronze layer using Databricks notebooks and PySpark.

  3.Data Cleaning & Transformation
       Cleaning and standardizing source data in the Silver layer through dedicated transformation notebooks.

  4.Data Modeling
     Creating a Sales Data Mart in the Gold layer using a Star Schema with fact and dimension tables.

  5.Orchestration
        Running Bronze, Silver, and Gold workflows through orchestration notebooks using:
        dbutils.notebook.run(...)

  6.Analytics & Reporting
    Preparing the final Gold tables for analytics and visualization tools such as Power BI.

This repository is a strong portfolio project for showcasing skills in:

  Databricks
  PySpark
  SQL
  Delta Lake
  Data Engineering
  ETL / ELT Pipelines
  Data Modeling
  Lakehouse Architecture
  Orchestration
  Business Analytics


# Tools :
    Databricks
    PySpark
    Delta Lake
    Unity Catalog
    SQL



# Project Requirements :



Objective

Develop a modern Lakehouse pipeline that consolidates data from multiple source systems and transforms it into analytics-ready business tables.
Specifications

   Data Sources: Import data from two source systems:
      CRM
      ERP
  File Format: CSV files
  Ingestion Method: Batch ingestion using Databricks notebooks and PySpark
  Data Quality: Clean and resolve issues such as:
        null values
        invalid dates
        inconsistent keys
        duplicate records
  Integration: Combine CRM and ERP data into a unified analytical model
  Modeling: Build a Star Schema for sales analytics
  Documentation: Provide architecture, orchestration, and schema documentation



# Source Datasets :

   CRM Source Files

    crm_50000_customers_dirty_v3.csv.csv
    clickstream_500k_events.csv

    
  ERP Source Files

    orders_300k_dirty.csv
    product_catalog_dirty_30pct.csv
    support_tickets_30000_dirty.csv


# Bronze Layer

  The Bronze layer stores the raw ingested data from the source files without applying major transformations.
  Bronze Tables

     lakehouse.bronze.customers
     lakehouse.bronze.stream
     lakehouse.bronze.orders
     lakehouse.bronze.products
     lakehouse.bronze.tickets


     
# Silver Layer

   The Silver layer applies cleaning and transformation logic to each dataset.
   Silver Transformations Include

    Trimming string columns
    Cleaning and converting date columns
    Standardizing IDs and join keys
    Handling null values
    Replacing invalid values
    Fixing inconsistent business values
    Deduplication checks
    Renaming columns to business-friendly names
    Saving cleaned data as Delta tables

# Silver Tables

     lakehouse.silver.customers
     lakehouse.silver.stream
     lakehouse.silver.orders
     lakehouse.silver.products
     lakehouse.silver.tickets




# Gold Layer

   The Gold layer contains business-ready analytical tables.
   Gold Tables

     lakehouse.gold.dim_customers
     lakehouse.gold.dim_stream
     lakehouse.gold.gold_orders
     lakehouse.gold.dim_products
     lakehouse.gold.dim_tickets



# Orchestration Flow
  

<img width="1180" height="686" alt="image" src="https://github.com/user-attachments/assets/1a1f56e1-c7c6-407f-8897-b34553a490dd" />








About Me :

i'm Nader Mohamed ,A Math & CS student at Helwan University
I’m passionate about Data Engineering, ETL pipelines, and modern data solutions.
I enjoy designing data architectures, building scalable pipelines, and transforming raw data into actionable insights.



