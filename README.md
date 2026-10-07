# UPI-Fraud-Analysis
# UPI Fraud Risk Analytics & Anomaly Detection

## 📌 Project Overview

This project is an end-to-end **UPI transaction risk analytics solution** built using Microsoft Azure, Azure Data Factory, Azure Data Lake Storage Gen2, Azure SQL Database, SQL, and Power BI.

The objective is to analyze UPI transaction data, identify potentially unusual transaction patterns, and provide an interactive dashboard for monitoring transaction activity and risk indicators.

> ⚠️ This project focuses on **data analytics and rule-based risk indicators**, not machine learning.  
> A risk indicator does not confirm that a transaction is fraudulent. Transactions identified by the dashboard should be treated as candidates for further investigation.

---

## 🎯 Project Objectives

- Build an end-to-end cloud-based analytics pipeline.
- Store raw and processed UPI transaction data in Azure.
- Use Azure Data Factory for data ingestion and transformation.
- Store structured analytical data in Azure SQL Database.
- Perform SQL-based transaction analysis.
- Build an interactive Power BI dashboard.
- Identify potentially unusual transaction patterns.
- Analyze customers, merchants, devices, locations, and transactions.
- Provide business-oriented insights for fraud/risk investigation teams.

---


# 🏗️ Solution Architecture

The project follows a multi-stage data analytics pipeline. The dataset is first cleaned using **IntelliClean**, then moved into the Azure cloud environment for ingestion, storage, processing, SQL analytics, and visualization.

```text
                 Raw / Synthetic UPI Dataset
                            │
                            ▼
                  ┌──────────────────┐
                  │   IntelliClean   │
                  │                  │
                  │ Data Cleaning    │
                  │ Data Validation  │
                  │ Data Preparation │
                  └────────┬─────────┘
                           │
                           ▼
                Cleaned UPI Dataset
                           │
                           ▼
                ┌─────────────────────┐
                │ Azure Data Factory  │
                │       (ADF)        │
                └──────────┬──────────┘
                           │
                           ▼
              ┌─────────────────────────┐
              │ Azure Data Lake Storage │
              │        Gen2             │
              │                         │
              │  ┌───────┐              │
              │  │  Raw  │              │
              │  └───────┘              │
              │  ┌───────────┐          │
              │  │ Processed │          │
              │  └───────────┘          │
              │  ┌─────────┐            │
              │  │ Curated │            │
              │  └─────────┘            │
              └─────────────┬───────────┘
                            │
                            ▼
                 ┌────────────────────┐
                 │   Azure SQL DB     │
                 │                    │
                 │ Customers          │
                 │ Merchants          │
                 │ Devices            │
                 │ Locations          │
                 │ Transactions       │
                 └─────────┬──────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │    Power BI     │
                  │                 │
                  │ Data Model      │
                  │ DAX Measures    │
                  │ Risk Analytics  │
                  │ Dashboards      │
                  └─────────────────┘

```text
                    
