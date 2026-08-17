# Banking Financial Analytics using Microsoft Fabric

An end-to-end banking data analytics project built using Microsoft Fabric, PySpark, Delta Lake, Direct Lake, and Power BI.

## 📊 Project Overview

This project demonstrates how raw banking transaction data can be transformed into clean, structured, and business-ready data using a modern data engineering architecture.

The project follows a **Bronze → Silver → Gold** approach and uses Microsoft Fabric for data processing, modeling, and visualization.

## 🎯 Project Objectives

- Ingest raw banking transaction data
- Store raw data in the Bronze layer
- Perform data cleaning and transformation
- Create structured Silver-layer data
- Generate analytical summary data
- Build a semantic model
- Create an interactive Power BI dashboard
- Analyze transactions, customers, payment methods, locations, and transaction status

## 🛠️ Technologies Used

- Microsoft Fabric
- OneLake
- Lakehouse
- Dataflow Gen2
- PySpark
- Delta Lake
- Direct Lake
- Semantic Model
- Power BI

## 🏗️ Project Architecture

```text
Raw Banking Data
       ↓
Bronze Layer
       ↓
Dataflow Gen2
       ↓
PySpark Data Cleaning & Transformation
       ↓
Silver Layer
       ↓
PySpark Aggregation
       ↓
Gold Summary Data
       ↓
Direct Lake Semantic Model
       ↓
Power BI Dashboard
