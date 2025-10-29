Jaffle Retail Store - Data Engineering Capstone Project
Project Overview
This project designs and implements an end-to-end batch data pipeline on the Databricks Lakehouse Platform to transform raw, fragmented retail data into a structured, analytics-ready data warehouse for Jaffle Retail Store.

Problem Statement
Retail businesses generate vast amounts of fragmented data across multiple sources that is often:

Siloed & Disconnected: Residing in separate systems, preventing unified view

Unclean & Unreliable: Containing missing values, duplicates, and inconsistencies

Not Analytics-Ready: Raw and unstructured, making it slow and difficult to query

Objectives & Scope
Vision: Create a centralized, reliable, and optimized single source of truth for retail data analytics.

Core Objective: Design and implement a scalable end-to-end batch data pipeline on Databricks Lakehouse Platform.

In-Scope Deliverables:

Data Ingestion: Consolidate multiple batch datasets (Customers, Transactions, Products)

Data Processing: Cleanse, standardize, and enrich data using PySpark

Data Modeling: Build optimized Star Schema in Databricks Delta Lake

Analytics Enablement: Deliver trusted data foundation for dashboards

🛠 Technology Stack
Databricks | PySpark | Delta Lake | SQL

Architecture & Implementation
Medallion Architecture
Bronze Layer
Objective: Ingest and preserve raw source data in original form

Data Sources: 6 CSV files (customers, orders, order_items, products, supplies, stores)

Storage: S3 bucket → Delta Lake tables in jaffle_shop_retail.bronze schema

Key Principle: Immutable storage with append-only mode for complete auditability

Silver Layer
Objective: Clean and validate raw data from Bronze layer

Processing:

Data cleaning (null handling, whitespace trimming, format standardization)

Deduplication using key identifiers

Data validation for quality assurance

Basic enrichment through table joins

Output: Clean, reliable datasets in Silver Delta tables

Gold Layer
Objective: Transform cleaned data into business-ready analytics models

Core Deliverables:

Star Schema Implementation: Dimension & Fact tables

Dimension Tables: Customers, Products, Stores, Date, Suppliers

Fact Tables: Sales transactions, Inventory metrics

Advanced Metrics: Customer Lifetime Value, Daily Sales

Star Schema Design
Optimized dimensional model for efficient querying and business intelligence.

SQL Warehouse & Querying
Serverless SQL Warehouse: Fully managed, auto-scaling SQL endpoint

Features: Instant setup, high performance, Unity Catalog integration

Usage: Direct querying on Gold layer tables for dashboards and analytics

Visualization & Dashboards
Interactive dashboards powered by the Gold layer data, providing real-time business insights with direct data lake connection.

Challenges & Learnings
Key Challenges
Data Quality: Managing inconsistent formats & missing values across sources

Architecture Scale: Implementing robust Medallion architecture

Performance: Optimizing Delta tables & Spark for efficient processing

Key Learnings
End-to-End Pipeline: Mastered complete data lifecycle on single platform

Production Engineering: Built scalable, monitored data workflows

Business Integration: Connected clean data directly to actionable dashboards

Conclusion & Achievements
Achievement: Delivered production-grade Medallion Architecture pipeline transforming raw CSVs into actionable business intelligence.

Business Impact:

Single Source of Truth: Centralized trusted data for the organization

Accelerated Insights: Reduced time from raw data to dashboard

Scalable Foundation: Architecture built for growing data needs

Future Enhancements
Predictive Analytics: Integrate ML for forecasting & segmentation

Real-time Capabilities: Extend to streaming for live insights

Enhanced Governance: Implement lineage monitoring & access controls
