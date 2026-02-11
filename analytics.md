# 📊 Analytics & Big Data – Deep Dive

A detailed and exam-focused breakdown of AWS Analytics services.

---

## 🔹 Amazon Athena

Amazon Athena is a serverless interactive query service.

It allows you to run SQL queries directly on data stored in S3. 

---

### ⚙️ Key Characteristics

- Serverless (no infrastructure management)
- Pay per TB scanned
- Uses Presto/Trino engine
- Supports CSV, JSON, Parquet, ORC, Avro
- Query results stored in S3

---

### 🏗 Schema on Read

- No need to load data into a database
- Define schema at query time
- Uses Glue Data Catalog for metadata

---

### 📌 Exam Focus

- Query S3 directly using SQL
- Optimize cost using compressed & columnar formats
- Often paired with Glue
- Good for ad-hoc analysis

---

### 🌍 Real-World Example

Security team analyzing CloudTrail logs stored in S3 without moving data to a database.

---

---

## 🔹 AWS Glue

AWS Glue is a fully managed ETL (Extract, Transform, Load) service.

It prepares and transforms data for analytics.

---

### 🏗 Core Components

- Glue Data Catalog
- Crawlers (automatic schema discovery)
- ETL Jobs (Apache Spark-based)
- Glue Studio (visual interface)
- Glue Workflows

---

### 🔄 Integrations

- S3
- Redshift
- Athena
- RDS
- DynamoDB
- Lake Formation

---

### 📌 Exam Focus

- Glue = ETL
- Crawlers automatically detect schema
- Data Catalog shared with Athena
- Serverless Spark jobs

---

### 🌍 Real-World Example

Cleaning raw clickstream logs in S3 before loading into Redshift.

---

---

## 🔹 Amazon EMR (Elastic MapReduce)

Amazon EMR is a managed big data platform.

Runs open-source frameworks like:

- Apache Spark
- Hadoop
- Hive
- Presto
- HBase
- Flink

---

### 🏗 Architecture

- Master Node
- Core Nodes
- Task Nodes

---

### ⚙️ Key Features

- Can use Spot instances
- Integrates with S3 (data lake)
- Auto scaling
- EMR Studio

---

### 📌 Exam Focus

- EMR for large-scale distributed processing
- Typically uses S3 instead of HDFS
- More control than Glue
- Cost-effective with Spot instances

---

### 🌍 Real-World Example

Processing petabytes of genomic research data using Spark.

---

---

## 🔹 Amazon Kinesis

Amazon Kinesis is a real-time data streaming service.

---

### 📦 Components

- Kinesis Data Streams
- Kinesis Data Firehose
- Kinesis Data Analytics
- Kinesis Video Streams

---

### 🔄 Differences

- **Data Streams** → Custom processing applications
- **Firehose** → Automatically loads data to S3, Redshift, OpenSearch
- **Data Analytics** → SQL on streaming data

---

### 📌 Exam Focus

- Real-time data ingestion
- Scales via shards
- Retention up to 7 days
- Used for IoT & clickstream data

---

### 🌍 Real-World Example

Ride-hailing app analyzing driver GPS data in real-time.

---

---

## 🔹 Amazon QuickSight

QuickSight is AWS’s Business Intelligence (BI) service.

Creates dashboards and visualizations.

---

### ⚙️ Key Features

- Connects to S3, Redshift, Athena, RDS
- SPICE in-memory engine
- ML-powered insights
- Row-level security

---

### 📌 Exam Focus

- Visualization layer
- Works with Redshift & Athena
- Pay-per-session pricing
- SPICE improves performance

---

### 🌍 Real-World Example

Retail company dashboard tracking sales performance across regions.

---

---

## 🔹 AWS Data Pipeline

Data Pipeline is a workflow orchestration service.

Moves and transforms data between AWS services and on-prem systems.

---

### ⚙️ Features

- Scheduled data movement
- Dependency management
- Fault tolerance
- Can run on EC2 or EMR

---

### 📌 Exam Focus

- Used for scheduled data workflows
- Older service compared to Glue
- Good for orchestrating recurring tasks

---

### 🌍 Real-World Example

Nightly job moving transaction data from RDS to S3.

---

---

## 🔹 Amazon MSK (Managed Streaming for Apache Kafka)

Amazon MSK is a managed Apache Kafka service.

---

### ⚙️ Key Features

- Fully managed Kafka clusters
- Multi-AZ deployment
- Automatic patching
- Integration with IAM

---

### 📌 Exam Focus

- Kafka-based streaming
- Alternative to Kinesis
- Good for existing Kafka workloads
- Used in event-driven architectures

---

### 🌍 Real-World Example

E-commerce platform using Kafka for order event streaming.

---

# ✅ Analytics & Big Data Section Complete
