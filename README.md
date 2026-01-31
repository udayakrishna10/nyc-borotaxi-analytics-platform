%md
# NYC BoroTaxi End-To-End Analytics & AI Insights Platform
Dec 2025 – Jan 2026

---

## Project Summary
An end-to-end data engineering solution built on the Databricks Lakehouse platform using medallion architecture (Bronze → Silver → Gold). It processes 12 years of NYC Green Taxi data (2014–2025, 84M+ trip records, $1.3B+ revenue) and transforms raw, inconsistent data into governed, analytics-ready datasets. The platform supports BI dashboards, ML features, and AI-powered strategic insights using Claude 3.7 Sonnet.

<p align="center">
  <img src="/Images/BoroTaxi.jpg" width="600" title="NYC Boro Taxi">
  <br>
  <em>The iconic "Apple Green" Boro Taxi - the primary subject of this 84M record analysis.</em>
</p>

---

## Architecture & Medallion Flow
The platform follows a standard Medallion Architecture governed by **Unity Catalog**:

* **Bronze Layer:** Raw landing with Photon-accelerated ingestion (84M records in 53s).
* **Silver Layer:** Quality enforcement with **DLT Expectations** (2.2M invalid rows filtered).
* **Gold Layer:** Aggregated business logic and 9 analytical views for sub-6s reporting.
* **AI Layer:** Automated strategic intelligence via **Claude 3.7 Sonnet**.

---

## Why I chose Databricks Lakehouse?
I intentionally built on the Databricks Lakehouse to unify streaming,
batch analytics, governance, and AI workloads on a single platform.

Key advantages:
- **Delta Lake** for ACID transactions, schema evolution, and time travel
- **Delta Live Tables** for declarative, reliable data pipelines with built-in quality enforcement
- **Photon Engine** for high-performance query execution at scale
- **Unity Catalog** for centralized governance, lineage, and secure data sharing
- **Native AI integration** enabling analytics and GenAI insights on the same data


---

## Technical Stack
| Category | Tools & Technologies |
| :--- | :--- |
| **Cloud Infrastructure** | Azure Data Lake Storage (ADLS Gen2), Azure Data Factory (ADF) |
| **Data Platform** | Databricks, Delta Live Tables (DLT), Unity Catalog (UC) |
| **Engine & Compute** | Photon Acceleration, PySpark, Spark SQL |
| **AI & Intelligence** | Claude 3.7 Sonnet API, ML-Ready Feature Engineering |

---
## Data Engineering & Technical Challenges

### Challenge 1: Schema Evolution Across 12 Years
* **Problem:** INT vs DOUBLE type conflicts across 2014-2025 Parquet files
* **Solution:** File-by-file ingestion with explicit type casting to DOUBLE
* **Impact:** Successfully unified 84M records without data loss

### Challenge 2: Data Quality at Scale
* **Problem:** 2.2M invalid records (negative fares, illogical timestamps)
* **Solution:** DLT Expectations with expect_or_drop enforcement
* **Impact:** 99.5% clean record yield, automated quality monitoring

### Challenge 3: Query Performance
* **Problem:** Slow queries on 84M records
* **Solution:** Year+Month partitioning with Photon acceleration
* **Impact:** 99.3% data skipping, sub-6s dashboard queries

### Challenge 4: High-Volume Cloud Ingestion
* **Problem:** Orchestrating decade-long Parquet files without timeouts or failures
* **Solution:** Built Azure Data Factory pipelines using dynamic `ForEach` loops and parameterized datasets.
* **Impact:**  Automated, fault tolerant ingestion with zero manual intervention.

### Challenge 5: Maintaining Governance & Lineage
* **Problem:** Tracking 16+ tables/views and access control across multiple layers
* **Solution:** Implemented **Unity Catalog** for unified namespace and fine-grained access control
* **Impact:** 100% data traceability and secure, audited access

### Challenge 6: AI Integration
* **Problem:** Manual analysis of revenue trends time-consuming
* **Solution:** Claude 3.7 Sonnet API for automated strategic insights
* **Impact:** Identified $40-60K monthly revenue opportunity

---

## Key Metrics & Business Impact
| Metric | Value |
| :--- | :--- |
| **Total Records Processed** | 84,027,827 |
| **Clean Record Yield** | 99.5% |
| **Total Revenue Reconciled** | $1.32B+ |
| **AI Strategy Impact** | Identified 101.2% growth in Bronx |

---

## Key Achievements

**Performance**: Ingested 84M records in 53 seconds using Photon acceleration  
**Data Quality**: Achieved 99.5% clean record yield with automated DLT expectations  
**AI Innovation**: Generated actionable insights worth $40-60K monthly revenue potential  
**Scalability**: Built streaming pipeline with 99.3% data skipping efficiency

---

## AI-Driven Strategic Insights
Integrated **Claude 3.7 Sonnet** to analyze monthly revenue pivots and generate executive-level intelligence:

* **Revenue Leakage:** -26.2% summer decline in Manhattan identified as seasonal rather than structural.
* **ROI Recommendation:** Suggested 15-20% fleet redeployment from Manhattan to Queens, estimated at **+$40-60K monthly revenue** potential.
* **Growth Catalyst:** Pinpointed the Bronx as an underserved market with **+101.2% Q1-Q2 growth**.

---

## Skills & Tools
* **Infrastructure:** Azure Databricks, ADLS Gen2, Unity Catalog
* **ETL:** Delta Live Tables (DLT), Azure Data Factory, PySpark, SQL
* **AI/ML:** Claude 3.7 Sonnet, ML-Ready Feature Generation

---

## Dashboard

![Dashboard](/Images/Dashboard.jpg)

---

## Report By Claude 3.7 Sonnet

* [NYC's BoroTaxi Strategic Intelligence Report 2025](Docs/NYC’s_BoroTaxi_Strategic_Intelligence_Report_by_Claude_3.7_Sonnet.pdf)

---

## References
* **Data Source:** [TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)
* **Image Credit:** [Wikipedia - Boro Taxi](https://en.wikipedia.org/wiki/Boro_taxi)

---

## **Udaya Krishna Karanam**  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/udayakrishnakaranam10)
[![Email](https://img.shields.io/badge/Email-Contact-red?style=flat&logo=gmail)](mailto:ukrishn10@gmail.com)

---

* **Image Credit:** [Wikipedia - Boro Taxi](https://upload.wikimedia.org/wikipedia/commons/e/e0/%28USA-New_York%29_NYC_Boro_Cab_Toyota_Camry_NY-Taxi-T762166C_2024-06-16.jpg)

