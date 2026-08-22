# azure-databricks-streaming-project
# 🚀 Uber Real-Time Data Engineering Pipeline on Azure

![Azure](https://img.shields.io/badge/Azure-Cloud-blue?logo=microsoftazure)
![Databricks](https://img.shields.io/badge/Databricks-Spark-red?logo=databricks)
![Apache Spark](https://img.shields.io/badge/Apache-Spark-E25A1C?logo=apachespark)
![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![GitHub](https://img.shields.io/badge/GitHub-Version_Control-black?logo=github)

---

# 📌 Project Overview

This project demonstrates the implementation of an enterprise-scale real-time data engineering pipeline for Uber ride events using Microsoft Azure.

Ride booking events are generated using Python, streamed through Azure Event Hub, processed using Azure Databricks (Apache Spark Structured Streaming), transformed using the Medallion Architecture (Bronze → Silver → Gold), modeled into analytical datasets

The project follows modern Data Engineering best practices including streaming ingestion, distributed data processing, dimensional modeling, and cloud-native architecture.

---

# 🎯 Business Problem

Ride-hailing companies generate millions of ride events every day.

The challenge is to:

- Process streaming events in real time
- Handle high-volume event ingestion
- Clean and validate incoming records
- Build analytics-ready datasets
- Serve curated data for reporting and APIs

This project addresses these challenges using Azure cloud services and Apache Spark.

---

# 🏗 Solution Architecture

<img width="1536" height="1024" alt="architecture" src="https://github.com/user-attachments/assets/ccd1ea4b-cae3-430e-9d4a-bc7f7c60e64a" />


```
Uber Ride Request
        │
        ▼
Python Data Generator
        │
        ▼
Azure Event Hub
        │
        ▼
Azure Databricks
(Spark Structured Streaming)
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

```

---

# ⚙ Technology Stack

| Category | Technology |
|-----------|------------|
| Cloud | Microsoft Azure |
| Streaming | Azure Event Hub |
| Processing | Azure Databricks |
| Framework | Apache Spark |
| Language | Python |
| Storage | Delta Lake |
| Version Control | Git & GitHub |

---

# 📂 Project Structure

```
Uber_Data_Engineer_Project/

│── ADF/
│── Data/
│── architecture/
│── screenshots/
│── Databricks/
│
├── api.py
├── connection.py
├── data.py
├── files_array.json
├── README.md
```

---

# 🔄 End-to-End Workflow

### Step 1

Generate Uber ride events using Python.

↓

### Step 2

Publish events to Azure Event Hub.

↓

### Step 3

Consume streaming events using Spark Structured Streaming.

↓

### Step 4

Store raw records in the Bronze Layer.

↓

### Step 5

Clean, validate and enrich data in the Silver Layer.

↓

### Step 6

Build analytics-ready datasets in the Gold Layer.


# 🥉 Bronze Layer

Stores raw streaming data exactly as received from Event Hub.

Features

- Immutable data
- Historical storage
- No transformations
- Source of truth

---

# 🥈 Silver Layer

Performs data transformation.

Includes

- Null handling
- Duplicate removal
- Schema validation
- Data standardization
- Data enrichment
- OBT

---

# 🥇 Gold Layer

Business-ready datasets.

Includes

- Fact tables
- Dimension tables
- Aggregations
- STAR Schema
- Analytics-ready models


---

# 🚀 Features

✔ Real-Time Event Streaming

✔ Azure Event Hub Integration

✔ Apache Spark Structured Streaming

✔ Azure Databricks

✔ Medallion Architecture

✔ Star Schema Modeling

✔ REST API

✔ Analytics Ready Data

✔ Distributed Processing

---

# 📊 Screenshots

Include the following screenshots.

- Solution Architecture
- Azure Resource Group
- Azure Event Hub
- Databricks Workspace
- Containers
- ADF pipeline
- Linked Services

---

---


# 🎯 Skills Demonstrated

- Azure Event Hub
- Azure Databricks
- Apache Spark
- Spark Structured Streaming
- Python
- Data Modeling
- Delta Lake
- ETL Pipelines
- Cloud Data Engineering
- Git
- SQL

---

---

# 📚 Key Learnings

Through this project, I gained hands-on experience with:

- Azure Event Hub
- Azure Databricks
- Spark Structured Streaming
- Medallion Architecture
- Star Schema Design
- Distributed Data Processing
- Cloud-native ETL Pipelines
- REST API Development

---

# 👨‍💻 Author

**Akshaya Redij**

LinkedIn: https://linkedin.com/in/your-profile

GitHub: https://github.com/yourusername

Email: your@email.com

---
