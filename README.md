# Banking Financial Analytics using Microsoft Fabric

An end-to-end banking data analytics project built using **Microsoft Fabric, PySpark, Delta Lake, Direct Lake, and Power BI**.

## 📊 Project Overview

This project demonstrates how raw banking data can be transformed into clean, business-ready datasets and analytical summaries using a modern data engineering architecture.

The project follows a **Bronze → Silver → Gold** architecture and uses Power BI for interactive reporting.

## 🏗️ Project Architecture

```text
Raw Banking Data
       ↓
Bronze Layer
       ↓
PySpark Data Cleaning & Transformation
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
