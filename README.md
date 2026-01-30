# NYC BoroTaxi End-To-End Analytics & AI Insights Platform
**Role:** Data Engineer  
**Duration:** Dec 2025 – Jan 2026

---

## 🎯 Project Summary
An enterprise-grade **Databricks Lakehouse** solution designed to process 12 years of NYC Green Taxi data (2014–2025). This platform transforms raw, inconsistent historical data into governed, analytics-ready datasets, powering BI dashboards and **Claude 3.7 AI** strategic insights.

---

## 🏗 Architecture & Medallion Flow
The platform follows a standard Medallion Architecture governed by **Unity Catalog**:

* **Bronze Layer:** Raw landing with **Photon-accelerated** ingestion (84M records in 53s).
* **Silver Layer:** Quality enforcement with **DLT Expectations** (2.2M invalid rows filtered).
* **Gold Layer:** Aggregated business logic and 9 analytical views for sub-6s reporting.
* **AI Layer:** Automated strategic intelligence via **Claude 3.7 Sonnet**.

---

## 🛠 Technical Stack
| Category | Tools & Technologies |
| :--- | :--- |
| **Cloud Infrastructure** | Azure Data Lake Storage (ADLS Gen2), Azure Data Factory (ADF) |
| **Data Platform** | Databricks, Delta Live Tables (DLT), Unity Catalog (UC) |
| **Engine & Compute** | Photon Acceleration, PySpark, Spark SQL |
| **AI & Intelligence** | Claude 3.7 Sonnet API, ML-Ready Feature Engineering |

---

<details>
<summary><b>📂 Data Engineering & Technical Challenges (Click to Expand)</b></summary>

### 1. Historical Data Inconsistency
* **Problem:** Schema drift and INT/DOUBLE conflicts across a 12-year window.
* **Solution:** Implemented standardized schemas in Bronze and enforced DLT quality gates in Silver to remove 2.2M invalid rows.
* **Result:** Achieved a **99.5% clean record yield**.

### 2. High-Volume Cloud Ingestion
* **Problem:** Orchestrating decade-long Parquet files without timeouts or failures.
* **Solution:** Built **Azure Data Factory** pipelines with dynamic `ForEach` loops and **Storage Event Triggers** for incremental loading.
* **Result:** Fully automated, event-driven ingestion with zero manual intervention.

### 3. Maintaining Governance & Lineage
* **Problem:** Tracking 16+ tables/views and access control across multiple layers.
* **Solution:** Implemented **Unity Catalog** for a unified namespace (`nyctaxi_catalog`) and fine-grained access control.
* **Result:** 100% data traceability and secure, audited access.

### 4. High-Performance Aggregations
* **Problem:** Querying 80M+ rows for real-time executive dashboards.
* **Solution:** Designed Gold-layer materialized views and applied **Z-Order clustering** on pickup locations.
* **Result:** Reporting query latency reduced to **under 6 seconds**.

</details>

---

## 📈 Key Metrics & Business Impact
| Metric | Value |
| :--- | :--- |
| **Total Records Processed** | 84,027,827 |
| **Clean Record Yield** | 99.5% |
| **Total Revenue Reconciled** | $1.32B+ |
| **AI Strategy Impact** | Identified 101.2% growth in Bronx |

---

## 🤖 AI-Driven Strategic Insights
Integrated **Claude 3.7 Sonnet** to analyze monthly revenue pivots and generate executive-level intelligence:

* **Revenue Leakage:** -26.2% summer decline in Manhattan identified as seasonal rather than structural.
* **ROI Recommendation:** Suggested 15-20% fleet redeployment from Manhattan to Queens, estimated at **+$40-60K monthly revenue** potential.
* **Growth Catalyst:** Pinpointed the Bronx as an underserved market with **+101.2% Q1-Q2 growth**.

---

## 🛠 Skills & Tools
* **Infrastructure:** Azure Databricks, ADLS Gen2, Unity Catalog.
* **ETL:** Delta Live Tables (DLT), Azure Data Factory, PySpark, SQL.
* **AI/ML:** Claude 3.7 Sonnet, ML-Ready Feature Generation.
