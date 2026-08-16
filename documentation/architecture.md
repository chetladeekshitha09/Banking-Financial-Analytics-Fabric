# Project Architecture

## Banking Financial Analytics using Microsoft Fabric

This project implements an end-to-end banking data analytics solution using Microsoft Fabric.

## Architecture Flow

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
Direct Lake Semantic Model
        ↓
Power BI Dashboard

---

## 1. Raw Data

The project starts with raw banking data stored as CSV files.

Examples:

- Accounts
- Customers
- Transactions
- Payments
- Branches
- Loans
- Fraud Transactions
- Date data

---

## 2. Bronze Layer

The raw data is stored in the Bronze layer.

Purpose:

- Store the original/raw data
- Maintain the source data
- Provide a starting point for transformation

---

## 3. Bronze to Silver Transformation

PySpark is used to transform the Bronze data.

Main activities:

- Read raw data
- Clean the data
- Handle data types
- Remove unwanted records
- Standardize columns
- Create clean transaction data

The cleaned data is stored in the Silver layer.

---

## 4. Silver Layer

The Silver layer contains cleaned and structured data.

Example:

- `silver.transactions`

This layer is used as the reliable data source for further analytics.

---

## 5. Silver to Gold Transformation

PySpark is used to aggregate the Silver data into analytical summary tables.

Gold tables include:

- `transaction_summary`
- `payment_summary`
- `location_summary`
- `status_summary`
- `account_summary`
- `customer_summary`
- `branch_summary`
- `date_summary`

These tables are designed for faster and easier reporting.

---

## 6. Semantic Model

A Direct Lake semantic model is created using the Gold tables.

The semantic model acts as a bridge between the prepared data and Power BI reporting.

Model name:

`Banking_Analytics_Model`

---

## 7. Power BI Dashboard

The semantic model is connected to a Power BI report.

Dashboard title:

**Banking Financial Analytics Dashboard**

The dashboard contains:

### KPI Cards

- Total Transactions
- Total Transaction Amount
- Completed Transactions
- Failed Transactions
- Pending Transactions
- Total Customers

### Visualizations

- Transactions by Type
- Transactions by Transaction Status
- Transactions by Location
- Transaction Share by Payment Method
- Total Amount by Location
- Transactions by Payment Method

---

## 8. Technologies Used

- Microsoft Fabric
- OneLake
- Lakehouse
- PySpark
- Delta Lake
- Dataflow Gen2
- Direct Lake
- Semantic Model
- Power BI

---

## 9. End-to-End Data Flow

The complete data processing flow is:

Raw CSV Data  
↓  
Bronze Layer  
↓  
Data Cleaning using PySpark  
↓  
Silver Layer  
↓  
Data Aggregation using PySpark  
↓  
Gold Summary Tables  
↓  
Direct Lake Semantic Model  
↓  
Power BI Dashboard

---

## 10. Project Objective

The main objective of this project is to build an end-to-end banking analytics platform that transforms raw banking data into clean, analytical datasets and interactive business dashboards using Microsoft Fabric.
