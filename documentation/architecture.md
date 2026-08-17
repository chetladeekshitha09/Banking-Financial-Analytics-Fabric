# Project Architecture

## Banking Financial Analytics using Microsoft Fabric

This project implements an end-to-end banking data analytics solution using Microsoft Fabric.

## Architecture Flow

Raw Banking Data
        ↓
Bronze Layer
        ↓
Dataflow Gen2
        ↓
PySpark Transformation
        ↓
Silver Layer
        ↓
Analytical Data
        ↓
Direct Lake Semantic Model
        ↓
Power BI Dashboard

---

## 1. Raw Data

The project starts with raw banking transaction data stored as CSV files.

The main dataset contains banking transaction information such as:

- Transaction ID
- Account ID
- Customer ID
- Transaction Date
- Transaction Type
- Amount
- Payment Method
- Transaction Status
- Location

---

## 2. Bronze Layer

The raw banking data is stored in the Bronze layer of the Fabric Lakehouse.

Purpose:

- Store raw/source data
- Preserve the original data
- Provide a starting point for data processing

---

## 3. Dataflow Gen2

Dataflow Gen2 is used for initial data preparation.

Dataflow name:

`DF_Banking_Bronze_to_Silver`

Main activities include:

- Importing CSV data
- Filtering rows
- Promoting headers
- Applying appropriate data types
- Loading the prepared data into the Banking Lakehouse

---

## 4. Bronze to Silver Transformation

PySpark is used for further data processing.

Notebook:

`01_Bronze_to_Silver_Transformation`

Main activities include:

- Reading the banking transaction data
- Inspecting the dataset
- Checking the schema
- Cleaning and transforming data
- Preparing structured Silver-layer data

---

## 5. Silver Layer

The Silver layer contains cleaned and structured banking data.

The cleaned transaction data is prepared for downstream analytics and reporting.

---

## 6. Analytical Layer

The processed data is used to support banking analytics and reporting.

The analytical data is used by the semantic model to provide business-friendly information for Power BI.

---

## 7. Semantic Model

A semantic model is created in Microsoft Fabric for reporting and analysis.

Model name:

`Banking_Analytics_Model`

The semantic model provides the data model used by the Power BI report.

---

## 8. Power BI Dashboard

The semantic model is connected to a Power BI report.

Dashboard title:

**Banking Financial Analytics Dashboard**

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

## 9. Technologies Used

- Microsoft Fabric
- OneLake
- Lakehouse
- Dataflow Gen2
- PySpark
- Delta Lake
- Direct Lake
- Semantic Model
- Power BI

---

## 10. End-to-End Data Flow

The complete processing flow is:

Raw CSV Data
↓
Bronze Layer
↓
Dataflow Gen2
↓
PySpark Data Cleaning & Transformation
↓
Silver Layer
↓
Analytical Data
↓
Direct Lake Semantic Model
↓
Power BI Dashboard

---

## 11. Project Objective

The main objective of this project is to build an end-to-end banking analytics solution that transforms raw banking transaction data into clean and structured data and presents meaningful business insights through a Power BI dashboard using Microsoft Fabric.
