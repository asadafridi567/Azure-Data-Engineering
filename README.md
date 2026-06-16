<div align="center">

# ☁️ Azure Data Engineering Projects

[![Azure](https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com)
[![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)](https://databricks.com)
[![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)](https://spark.apache.org)
[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com)

A collection of **three end-to-end cloud data engineering projects** built on Microsoft Azure, covering real-world datasets with production-grade pipeline architecture — from raw ingestion to business-ready analytics.

</div>

---

## 📁 Repository Structure

```
Azure-Data-Engineering-Projects/
│
├── 📂 NYC Taxi End-to-End Data Engineering Project/
├── 📂 Netflix Azure End-to-End Data Engineering Project/
└── 📂 Spotify Data Engineering Project/
```

---

## 🏗️ Architecture Overview

All three projects follow the **Medallion Architecture** pattern:

```
Data Source
    │
    ▼
┌─────────────┐      ┌──────────────┐      ┌────────────────┐      ┌──────────┐
│   BRONZE    │ ───▶ │    SILVER    │ ───▶ │      GOLD      │ ───▶ │  Power   │
│  Raw Data   │      │  Cleaned &   │      │  Aggregated &  │      │    BI    │
│  (Ingested) │      │  Validated   │      │  Business-Ready│      │Dashboard │
└─────────────┘      └──────────────┘      └────────────────┘      └──────────┘
     ADF / REST              PySpark              DLT / Delta              Viz
```

---

## 🚕 Project 1 — NYC Taxi End-to-End Data Engineering

> Building a scalable cloud pipeline to process NYC taxi trip data using Azure's core data engineering stack.

### 🛠️ Tech Stack
| Service | Purpose |
|---|---|
| Azure Data Factory | Pipeline orchestration & scheduling |
| ADLS Gen2 | Central data lake storage |
| Azure Databricks | Distributed data processing |
| PySpark | Large-scale data transformation |
| Delta Lake | ACID transactions & time travel |
| Azure Service Principal | Secure Databricks ↔ Data Lake access |
| Power BI | Data visualization & dashboards |

### ✅ Key Highlights
- Built a fully orchestrated cloud pipeline using **Azure Data Factory** with **Medallion Architecture** (Bronze → Silver → Gold)
- Processed and transformed large-scale NYC taxi datasets using **PySpark on Azure Databricks**
- Leveraged **Delta Lake** for ACID-compliant transactions and time travel capabilities
- Secured Databricks-to-Data Lake connectivity via **Azure Service Principal**
- Delivered business insights through interactive **Power BI** dashboards on curated Gold-layer data

📂 [View Project Folder](./NYC%20Taxi%20End-to-End%20Data%20Engineering%20Project/)

---

## 🎬 Project 2 — Netflix Azure End-to-End Data Engineering

> An end-to-end pipeline ingesting Netflix data via REST APIs, processing through Databricks, and enforcing enterprise-grade governance with Unity Catalog.

### 🛠️ Tech Stack
| Service | Purpose |
|---|---|
| Azure Data Factory | Parameterized pipeline orchestration |
| ADLS Gen2 | Medallion Architecture data lake |
| Azure Databricks + Autoloader | Incremental data ingestion |
| PySpark | Schema casting & window transformations |
| Delta Live Tables (DLT) | Reliable Gold-layer pipeline management |
| Unity Catalog | Data governance & access control |
| Power BI | Analytics & reporting |

### ✅ Key Highlights
- Designed **parameterized ADF pipelines** to ingest Netflix data via HTTP/REST APIs into a structured data lake
- Used **Databricks Autoloader** for efficient incremental ingestion without manual file tracking
- Applied **PySpark** transformations including schema casting and complex window functions
- Built reliable **Gold-layer pipelines** with Delta Live Tables and data quality Expectations
- Enforced enterprise-level data governance and access control using **Unity Catalog**

📂 [View Project Folder](./Netflix%20Azure%20End-to-End%20Data%20Engineering%20Project/)

---

## 🎵 Project 3 — Spotify Azure End-to-End Data Engineering

> A real-time, metadata-driven data engineering pipeline for Spotify data with SCD Type 2 logic, CI/CD automation, and live failure alerting.

### 🛠️ Tech Stack
| Service | Purpose |
|---|---|
| Azure Data Factory | Dynamic pipelines with backfilling |
| Azure SQL Database | Source system for Spotify data |
| ADLS Gen2 | Bronze / Silver / Gold data lake |
| Databricks + Autoloader | Spark Structured Streaming |
| Delta Live Tables | SCD Type 2 & Gold-layer pipelines |
| Unity Catalog | Data governance |
| Logic Apps | Pipeline failure alerting |
| Jinja Templating | Metadata-driven SQL views |
| Databricks Asset Bundles | CI/CD deployment |

### ✅ Key Highlights
- Built **real-time dynamic ADF pipelines** with backfilling support to move Spotify data from Azure SQL Database to ADLS Gen2
- Implemented **Spark Structured Streaming** with Autoloader for continuous incremental ingestion
- Applied **SCD Type 2** logic via Delta Live Tables to maintain full historical records in the Gold layer
- Used **Jinja templating** for metadata-driven, reusable SQL view generation
- Configured **Logic Apps** to send automated alerts on pipeline failures
- Deployed pipelines using **Databricks Asset Bundles** for proper CI/CD lifecycle management

📂 [View Project Folder](./Spotify%20Data%20Engineering%20Project/)

---

## 🧰 Common Tools & Technologies

<div align="center">

![ADF](https://img.shields.io/badge/Azure%20Data%20Factory-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white)
![ADLS](https://img.shields.io/badge/ADLS%20Gen2-0078D4?style=flat-square&logo=microsoft-azure&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-003366?style=flat-square&logo=apache&logoColor=white)
![DLT](https://img.shields.io/badge/Delta%20Live%20Tables-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Unity Catalog](https://img.shields.io/badge/Unity%20Catalog-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-CC2927?style=flat-square&logo=microsoft-sql-server&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

</div>

---

## 🚀 Getting Started

Each project folder contains its own notebooks, pipelines, and setup instructions. To explore a project:

1. Navigate into the project folder of your choice
2. Follow the setup steps in that folder's README *(if available)*
3. Import Databricks notebooks into your Azure Databricks workspace
4. Configure ADF pipelines with your own Azure credentials and resource names
5. Set up ADLS Gen2 containers following the Bronze/Silver/Gold structure

> **Prerequisites:** An active Microsoft Azure subscription with access to ADF, ADLS Gen2, and Azure Databricks.

---

## 👨‍💻 Author

**Muhammad Asad** — Data Engineer & Python Developer

[![Email](https://img.shields.io/badge/Email-muasad007%40gmail.com-red?style=flat-square&logo=gmail&logoColor=white)](mailto:muasad007@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-asadafridi567-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/asadafridi567)
[![EpubForge](https://img.shields.io/badge/Live%20Project-EpubForge-38BDF8?style=flat-square&logo=vercel&logoColor=white)](https://www.epubforge.com)
