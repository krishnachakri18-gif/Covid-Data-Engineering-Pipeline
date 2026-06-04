# Clinical Analytics Lakehouse Pipeline: End-to-End Medallion Tier Data Engineering Project

## Project Overview
This repository contains an enterprise-grade medical analytics pipeline executing a **Lakehouse Medallion Architecture** over cloud storage arrays. The pipeline automates the ingestion of high-volume clinical transaction logs across two specialized **Databricks Notebooks**, enforces strict schema optimization patterns using **Apache Spark (PySpark)**, models enriched entities into a denormalized **Gold Star Schema**, and productionalizes business logic into **Azure Synapse Serverless SQL Pool Views**.

The analytics framework is purpose-built to solve advanced data constraints—including regional single-state data profiling barriers, granular record array-flattening, and cross-domain relational multiplication anomalies—delivering pre-aggregated, low-latency, chart-ready database perspectives optimized for sub-second dashboard rendering engines.

---

##  Cloud Data Lake Architecture & Technology Stack
* **Storage Environment:** Azure Data Lake Storage Gen2 (ADLS Gen2) structured into distinct Bronze, Silver, and Gold Parquet/Delta Lake directories.
* **Compute & Processing Engine:** Azure Databricks / Apache Spark (PySpark) executing configuration-driven data schema enforcement and narrow filtering.
* **Data Warehouse Analytics Layer:** Azure Synapse Analytics (Serverless SQL Pool) managing structural view abstractions over external tables.
* **Downstream Consumption:** Power BI / Tableau semantic layers connected via dedicated cloud gateway serverless connection strings (`ondemand.sql.azuresynapse.net`).

---

## 📁 Repository Directory Layout
```text
├── databricks_notebooks/
│   ├── 1_bronze_to_silver_ingestion.ipynb    # Metadata Bulk Casting, Cleaning, & Validation
│   └── 2_silver_to_gold_modeling.ipynb      # Star Schema Modeling & Fact Table Denormalization
├── reporting_layer/
│   ├── 01_age_metrics_demographics.sql      # Risk Bracket Analysis (CASE WHEN + DATEDIFF)
│   ├── 02_elderly_allergy_aggregation.sql   # Complex Array List Compression (STRING_AGG)
│   ├── 03_monthly_case_trends.sql           # Time-Series Month-over-Month Velocity (LAG)
│   ├── 04_cumulative_total_tracker.sql      # Rolling Pandemic Progressions (SUM OVER)
│   ├── 05_hospital_leaderboard_per_city.sql # Municipal Load Constraints (DENSE_RANK)
│   └── 06_seasonal_surge_peaks.sql          # Peak Operational Wave Pressures (YEAR/MONTH Windows)
└── README.md                                # Architecture Documentation Matrix
