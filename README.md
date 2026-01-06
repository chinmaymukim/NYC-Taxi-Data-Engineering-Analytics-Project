# NYC-Taxi-Data-Engineering-Analytics-Project

📌 Project Overview

This project implements an end-to-end, production-style data engineering and analytics platform using Microsoft Fabric on NYC Taxi trip data (2025).

The system ingests monthly-updating raw data, performs automated cleaning and transformation, stores curated data in a Fabric Warehouse, and delivers self-refreshing Power BI reports for analytics and insights — with zero manual intervention after setup.

🎯 Business Problem

NYC Taxi data is:

High volume

Frequently updated (monthly)

Schema-sensitive (dates, numeric fields, nulls)

Challenge:
Build a scalable, automated, and reliable pipeline that:

Handles recurring data updates

Cleans and standardizes raw data

Supports analytics without manual refresh

Follows modern lakehouse / warehouse best practices

✅ Solution Architecture

End-to-end flow:

NYC Taxi Source Data (Monthly)
        ↓
Azure Blob Storage (Raw Zone)
        ↓
Microsoft Fabric Pipelines (Orchestration)
        ↓
Dataflow Gen2 (Cleaning & Transformation)
        ↓
Fabric Warehouse (Staging → Curated Tables)
        ↓
Power BI Semantic Model & Reports

🧰 Tech Stack

Microsoft Fabric

Dataflow Gen2

Fabric Pipelines

Fabric Warehouse

Azure Blob Storage

SQL (DDL, MERGE, Transformations)

Power Query (M)

Power BI

Semantic Modeling

DAX

Interactive Dashboards

⚙️ Key Engineering Features
🔹 Automated Ingestion

Monthly NYC Taxi data lands in Azure Blob Storage

Fabric pipeline orchestrates ingestion and transformation

🔹 Robust Data Cleaning

Date normalization

Data type enforcement

Null and error handling

Schema consistency across loads

🔹 Warehouse Design

Staging and curated tables

Explicit schema control

SQL-based transformations and MERGE logic

🔹 Orchestration & Reliability

Pipelines manage execution order

Idempotent loads

No manual reruns required

🔹 Analytics-Ready Output

Optimized warehouse tables

Power BI semantic model

Reports auto-refresh as new data arrives

📊 Power BI Reporting

The report updates automatically every month when new data is ingested.

Insights include:

📈 Monthly trip volume trends

🚕 Vendor performance analysis

👥 Passenger count distribution

💰 Fare amount & trip distance analysis

🕒 Time-based travel patterns

📂 Repository Structure
nyc-taxi-microsoft-fabric/
│
├── 1-architecture/
│   └── fabric-architecture.png
│
├── 2-ingestion/
│   └── blob_container_structure.png
│
├── 3-dataflow-gen2/
│   ├── power_query_m_code.txt
│
├── 4-warehouse/
│   ├── create_tables.sql
│   ├── merge_procedures.sql
│   └── schema_design.md
│
├── 5-orchestration-pipelines/
│   └── pipeline_flow.png
│
├── 6-powerbi/
│   └── report_screenshots/
│
└── README.md

🧠 What This Project Demonstrates

Real-world data engineering lifecycle

Hands-on Microsoft Fabric expertise

Understanding of orchestration, schema control, and automation

Strong analytics and business insight delivery

Production mindset (not just experimentation)

🚀 Impact

Eliminated manual data refresh effort

Enabled scalable monthly ingestion

Delivered analytics-ready data to Power BI

Created a reusable Fabric architecture pattern

🔮 Future Enhancements

Incremental data loading optimization

Data quality monitoring & alerts

CI/CD using Fabric deployment pipelines

Parameterized pipelines for multi-year data
