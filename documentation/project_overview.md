**Banking Financial Analytics using Microsoft Fabric**

## Project Overview

This is an end-to-end banking data analytics project developed using Microsoft Fabric.

The project follows a Medallion Architecture:

Source Data → Bronze → Silver → Gold → Semantic Model → Power BI Dashboard

## Objective

The objective of this project is to process banking transaction data, transform raw data into clean and business-ready datasets, generate analytical summaries, and visualize important banking KPIs through a Power BI dashboard.

## Technologies Used

- Microsoft Fabric
- OneLake
- Lakehouse
- Dataflow Gen2
- PySpark
- Delta Lake
- Semantic Model
- Power BI

## Project Architecture

### 1. Bronze Layer

The Bronze layer contains the raw banking data.

Raw data is stored in the Microsoft Fabric Lakehouse before transformation.

### 2. Silver Layer

The Bronze data is cleaned and transformed using PySpark.

The Silver layer contains cleaned and structured transaction data that is ready for analytical processing.

### 3. Gold Layer

The Silver data is aggregated using PySpark.

The following business summary tables were created:

- account_summary
- branch_summary
- customer_summary
- date_summary
- location_summary
- payment_summary
- status_summary
- transaction_summary

### 4. Semantic Model

A Power BI semantic model named `Banking_Analytics_Model` was created using the Gold tables.

This model provides business-ready data for reporting and visualization.

### 5. Power BI Dashboard

A dashboard named `Banking Financial Analytics Dashboard` was created.

The dashboard contains:

- Total Transactions
- Total Transaction Amount
- Completed Transactions
- Failed Transactions
- Pending Transactions
- Total Customers
- Transactions by Type
- Transactions by Status
- Transactions by Location
- Transaction Share by Payment Method
- Total Amount by Location
- Transactions by Payment Method

## Data Processing Flow

```text
Raw Banking Data
       ↓
Bronze Layer
       ↓
PySpark Transformation
       ↓
Silver Layer
       ↓
PySpark Aggregation
       ↓
Gold Summary Tables
       ↓
Semantic Model
       ↓
Power BI Dashboard
