# 🗄 Database Services – Deep Dive

A detailed and exam-focused breakdown of AWS Database services.

---

## 🔹 Amazon RDS (Relational Database Service) 

Amazon RDS is a managed relational database service.

Supports:

- MySQL
- PostgreSQL
- MariaDB
- Oracle
- SQL Server
- Amazon Aurora

---

### 🏗 Core Features

- Automated provisioning
- Automated backups
- Patching & maintenance
- Monitoring via CloudWatch
- Multi-AZ deployment
- Read Replicas

---

### 🔁 High Availability vs Scaling

- **Multi-AZ**
  - Synchronous replication
  - Automatic failover
  - Used for HA (not scaling)

- **Read Replicas**
  - Asynchronous replication
  - Used for read scaling
  - Can be cross-region

---

### 💾 Storage

- gp3 (General SSD)
- io2 (Provisioned IOPS)
- Magnetic (legacy)

Snapshots stored in S3.

---

### 📌 Exam Focus

- Multi-AZ = HA
- Read Replica = Scaling
- RDS Proxy improves connection handling
- Backups stored automatically in S3
- Vertical scaling = change instance size

---

### 🌍 Real-World Example

Food delivery app storing orders and payments with Multi-AZ enabled and read replicas for reporting.

---

---

## 🔹 Amazon Aurora

Aurora is AWS-optimized relational database.

Compatible with MySQL & PostgreSQL.

---

### 🚀 Key Advantages

- 5x performance over MySQL
- 3x performance over PostgreSQL
- 6 copies across 3 AZs
- Automatic failover (<30 seconds)
- Up to 15 read replicas

---

### 🔄 Aurora Variants

- Provisioned
- Aurora Serverless
- Aurora Global Database

---

### 📌 Exam Focus

- 15 read replicas → Aurora
- Multi-region read → Aurora Global
- Unpredictable workload → Serverless
- Storage auto-scales up to 128 TB

---

### 🌍 Real-World Example

Ride-sharing app using Aurora with 10 read replicas during peak hours.

---

---

## 🔹 Amazon DynamoDB

Fully managed NoSQL key-value & document database.

Serverless and highly scalable.

---

### 🏗 Core Concepts

- Partition Key
- Sort Key (optional)
- Tables
- Items
- Attributes

---

### ⚙️ Capacity Modes

- On-Demand
- Provisioned (with auto-scaling)

---

### 🚀 Advanced Features

- Global Tables (multi-region)
- DynamoDB Streams
- TTL (Time to Live)
- Transactions (ACID)
- DAX (in-memory caching)

---

### 📌 Exam Focus

- Single-digit millisecond latency
- Unlimited horizontal scaling
- Streams used with Lambda
- Good for unpredictable workloads

---

### 🌍 Real-World Example

Gaming leaderboard storing millions of real-time score updates.

---

---

## 🔹 Amazon ElastiCache

Managed in-memory caching service.

Supports:

- Redis
- Memcached

---

### 🔥 Redis vs Memcached

| Feature | Redis | Memcached |
|----------|--------|------------|
| Persistence | Yes | No |
| Replication | Yes | No |
| Clustering | Yes | Yes |
| Pub/Sub | Yes | No |

---

### 📌 Exam Focus

- Reduces database load
- Microsecond latency
- Redis supports Multi-AZ failover
- Used for session caching

---

### 🌍 Real-World Example

E-commerce app caching product catalog during high traffic.

---

---

## 🔹 Amazon Neptune

Managed graph database.

Optimized for highly connected datasets.

---

### 🔎 Query Languages

- Gremlin (Property Graph)
- SPARQL (RDF)

---

### 📌 Exam Focus

- Social networks
- Fraud detection
- Recommendation engines
- Up to 15 read replicas

---

### 🌍 Real-World Example

Bank detecting fraud patterns through relationship mapping.

---

---

## 🔹 Amazon Redshift

Managed data warehouse for analytics (OLAP).

---

### ⚙️ Core Features

- Columnar storage
- Massively Parallel Processing (MPP)
- Redshift Spectrum (query S3)
- Concurrency Scaling
- RA3 nodes (separate compute & storage)

---

### 📌 Exam Focus

- OLAP workloads
- Petabyte-scale analytics
- Works with S3 data lakes
- Snapshots stored in S3

---

### 🌍 Real-World Example

Retail company analyzing billions of transactions for reporting.

---

---

## 🔹 Amazon QLDB

Managed ledger database.

Provides immutable and cryptographically verifiable transaction log.

---

### 📌 Exam Focus

- Centralized ledger
- Not decentralized like blockchain
- Uses PartiQL
- Immutable audit trail

---

### 🌍 Real-World Example

Supply chain system tracking product ownership history.

---

---

## 🔹 Amazon DocumentDB

MongoDB-compatible document database.

Stores JSON-like documents.

---

### 🔄 Key Features

- Auto-scaling storage (up to 64 TB)
- Multi-AZ replication
- 15 read replicas
- Continuous backup

---

### 📌 Exam Focus

- MongoDB compatibility
- Document-oriented
- Managed alternative to self-hosted MongoDB

---

### 🌍 Real-World Example

Content management system storing blog posts and comments.

---

---

## 🔹 Amazon Keyspaces (for Apache Cassandra)

Managed Cassandra-compatible database.

Wide-column NoSQL database.

---

### ⚙️ Features

- Serverless scaling
- Multi-AZ replication
- CQL support
- On-demand or provisioned capacity

---

### 📌 Exam Focus

- Cassandra workloads
- High write throughput
- Time-series-like workloads

---

### 🌍 Real-World Example

Telecom storing call detail records.

---

---

## 🔹 Amazon Timestream

Managed time-series database.

Optimized for timestamp-based data.

---

### ⚙️ Key Features

- Serverless
- Automatic lifecycle tiering
- Fast time-based queries
- SQL-like querying

---

### 📌 Exam Focus

- IoT sensor data
- DevOps metrics
- Financial tick data
- Much faster than relational DB for time-series

---

### 🌍 Real-World Example

Smart city collecting traffic sensor metrics.

---

# ✅ Database Section Complete
