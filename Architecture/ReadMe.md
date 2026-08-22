# 🏗️ Architecture Documentation

This folder contains the architecture diagrams used in the **Real-Time Data Engineering Pipeline** project. The solution follows modern Data Engineering principles using Microsoft Azure, Apache Spark and the Medallion Architecture to process streaming ride-booking events.

---


# 📌 Solution Architecture

The project implements a real-time streaming pipeline for processing Uber ride events.

```
                   Uber Ride Booking Application
                                │
                                ▼
                    Python Event Generator
                                │
                                ▼
                     Azure Event Hub (Kafka)
                                │
                                ▼
                    Azure Data Factory (ADF)
                                │
                                ▼
                 Azure Databricks (Spark Streaming)
                                │
               ┌────────────────┼────────────────┐
               ▼                ▼                ▼
          Bronze Layer     Silver Layer     Gold Layer
               │                │                │
               └────────────────┼────────────────┘
                                ▼
                          Star Schema
                                │
                                ▼
                    Analytics & Business Reports
```

---

# 📖 Architecture Components

## 1. Python Data Generator

The project begins by generating synthetic Uber ride booking events.

The generated events simulate real-world streaming ride requests.

---

## 2. Azure Event Hub

Azure Event Hub acts as the streaming ingestion layer.

Responsibilities:

- Receive ride booking events
- Buffer streaming data
- Enable scalable event ingestion
- Provide reliable event streaming

---

## 3. Azure Data Factory

Azure Data Factory orchestrates the end-to-end pipeline.

Responsibilities

- Trigger streaming jobs
- Manage workflows
- Schedule data movement
- Connect Azure services

---

## 4. Azure Databricks

Azure Databricks is responsible for distributed processing using Apache Spark.

Responsibilities

- Read streaming events
- Apply business transformations
- Validate records
- Clean data
- Create Delta Tables
- Load Medallion layers

---

# 🥉 Bronze Layer

Purpose

Store raw streaming data exactly as received from Azure Event Hub.

Characteristics

- Raw events
- Append-only storage
- Immutable data
- Historical source of truth

---

# 🥈 Silver Layer

Purpose

Improve data quality.

Operations

- Data cleansing
- Duplicate removal
- Null handling
- Data validation
- Standardization
- Business rule enforcement
- OBT 

---

# 🥇 Gold Layer

Purpose

Create analytics-ready datasets.

Operations

- Fact table creation
- Dimension table creation
- Aggregations
- Reporting models

---

# 🔄 Data Flow

```
Ride Booking Event

        │

        ▼

Python Event Generator

        │

        ▼

Azure Event Hub

        │

        ▼

Azure Data Factory

        │

        ▼

Azure Databricks

        │

        ▼

Bronze Layer

        │

        ▼

Silver Layer

        │

        ▼

Gold Layer

        │

        ▼

Star Schema

        │

        ▼

Analytics Dashboard
```

---

# 🎯 Design Principles

This architecture is designed with the following goals:

- Scalability
- Fault Tolerance
- Low Latency
- Modular Design
- Distributed Processing
- Cloud-Native Architecture
- Analytics-Ready Data
- Separation of Storage and Compute

---

# 🚀 Technologies Used

| Layer | Technology |
|---------|------------|
| Programming | Python |
| Streaming | Azure Event Hub |
| Orchestration | Azure Data Factory |
| Processing | Azure Databricks |
| Engine | Apache Spark Structured Streaming |
| Storage | Delta Lake |
| Data Modeling | Star Schema |
| API | FastAPI |
| Version Control | GitHub |


