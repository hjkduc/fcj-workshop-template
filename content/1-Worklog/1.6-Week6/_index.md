---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:
* Build foundational knowledge of Data Lakes, Data Governance, and Data Analytics pipelines on AWS.
* Learn serverless query engines (Amazon Athena) and Business Intelligence (BI) visualization using Amazon QuickSight.
* Deepen relational database expertise with Amazon Aurora PostgreSQL and dive into Machine Learning workflows using Amazon SageMaker.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: AWS Data Lake Fundamentals & Architecting Data Lakes**<br>- **Knowledge:**<br>  + Data Lake vs Data Warehouse: Differences, storage decoupling, structured vs unstructured data.<br>  + AWS Lake Formation: Centralized data governance, fine-grained access control (column/row-level permissions), and Data Cataloging.<br>- **Practice:**<br>  + Ingest raw datasets into Amazon S3 storage tiers.<br>  + Configure AWS Lake Formation permissions and register S3 paths into the AWS Glue Data Catalog. | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: Data Analytics Service Overview & Business Intelligence with Amazon QuickSight**<br>- **Knowledge:**<br>  + AWS Analytics Ecosystem: Amazon Kinesis (streaming data), EMR (Big Data), Redshift (Data Warehouse).<br>  + Amazon QuickSight: Cloud-native BI, SPICE in-memory engine, interactive dashboards, and ML-powered insights.<br>- **Practice:**<br>  + Connect Amazon QuickSight to an Athena/S3 data source using SPICE caching.<br>  + Build and publish an interactive business analytics dashboard with customized visuals. | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: Data Engineering Immersion Day & Serverless Analytics with Amazon Athena**<br>- **Knowledge:**<br>  + Serverless Querying: Amazon Athena, Presto SQL engine, pay-per-query cost model.<br>  + Performance & Cost Optimization: Columnar storage formats (Apache Parquet / ORC), compression (Snappy), and data partitioning strategies.<br>- **Practice:**<br>  + Convert raw JSON/CSV log datasets into Apache Parquet format using AWS Glue ETL jobs.<br>  + Execute SQL analytics queries in Amazon Athena and measure query cost savings via partitioning. | 27/05/2026 | 27/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: Advanced PostgreSQL on AWS - Part 1 & 2 (Amazon Aurora PostgreSQL)**<br>- **Knowledge:**<br>  + Amazon Aurora Architecture: Cloud-native relational database, distributed 6-way storage replication, Serverless v2, and Read Replicas.<br>  + Database Performance Tuning: Amazon RDS Performance Insights, Query Execution Plans, and pgvector extension for AI workloads.<br>- **Practice:**<br>  + Provision an Amazon Aurora PostgreSQL Serverless v2 cluster with auto-scaling capacity.<br>  + Analyze database workload bottlenecks and slow queries using RDS Performance Insights. | 28/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: Machine Learning Concepts & Model Training with Amazon SageMaker**<br>- **Knowledge:**<br>  + End-to-End ML Lifecycle: Data preparation, model building, training, tuning, deployment, and monitoring.<br>  + Amazon SageMaker Suite: SageMaker Studio, built-in algorithms (XGBoost, Linear Learner), Managed Spot Training, and Inference Endpoints.<br>- **Practice:**<br>  + Prepare and clean a sample dataset inside Amazon SageMaker Studio Jupyter Notebooks.<br>  + Train an XGBoost classification model and deploy it to a real-time SageMaker Inference Endpoint. | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 6 Achievements:

#### Monday (25/05/2026):
* Mastered architectural differences between traditional Data Warehouses and modern Data Lakes on Amazon S3.
* Configured fine-grained access control policies (row and column-level security) using AWS Lake Formation.
* Registered raw S3 datasets into the AWS Glue Data Catalog to build a centralized metadata repository.

#### Tuesday (26/05/2026):
* Explored the full spectrum of AWS Big Data and Analytics services (Kinesis, EMR, Redshift, QuickSight).
* Connected Amazon QuickSight to cloud data sources and leveraged the SPICE in-memory engine for rapid data processing.
* Built interactive Business Intelligence (BI) dashboards featuring automated ML insights and visual KPIs.

#### Wednesday (27/05/2026):
* Learned serverless data engineering techniques using Amazon Athena to query S3 data directly with SQL.
* Optimized analytics performance and reduced query costs by converting raw files into Apache Parquet columnar format via AWS Glue.
* Implemented data partitioning strategies to minimize data scanned during analytical queries.

#### Thursday (28/05/2026):
* Deepened database management skills with Amazon Aurora PostgreSQL Serverless v2 enterprise architecture.
* Evaluated Aurora's distributed multi-AZ storage replication and instant read-scaling capabilities.
* Utilized RDS Performance Insights to diagnose database execution bottlenecks and tune SQL queries.

#### Friday (29/05/2026):
* Acquired a comprehensive understanding of the complete Machine Learning lifecycle on AWS.
* Utilized Amazon SageMaker Studio to prepare datasets, build feature pipelines, and train models using built-in algorithms.
* Deployed a trained Machine Learning model to a scalable, real-time SageMaker Inference Endpoint for API predictions.