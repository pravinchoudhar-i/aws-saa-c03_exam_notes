# 💾 Storage Services – Deep Dive

A detailed and exam-focused breakdown of AWS Storage services.

---

## 🔹 Amazon S3 (Simple Storage Service)

Amazon S3 is a scalable object storage service.

It is designed for durability, availability, and virtually unlimited storage.

---

### 🏗 Core Concepts

- **Bucket** – Container for storing objects
- **Object** – File stored in S3 (max size 5 TB)
- **Key** – Unique identifier of object inside bucket
- **Versioning** – Keeps multiple versions of objects
- **Metadata** – Additional information about object

---

### 📦 Storage Classes

| Storage Class | Use Case |
|---------------|----------|
| Standard | Frequently accessed data |
| Standard-IA | Infrequent access |
| One Zone-IA | Infrequent access (single AZ) |
| Glacier Instant Retrieval | Archive with ms retrieval |
| Glacier Flexible Retrieval | Minutes to hours retrieval |
| Glacier Deep Archive | Lowest cost, 12+ hour retrieval |

---

### 🔐 Security

- IAM Policies
- Bucket Policies
- ACLs
- SSE-S3 (AWS-managed keys)
- SSE-KMS (Customer-managed keys)
- SSE-C (Customer-provided keys)
- MFA Delete

---

### 🔄 Data Management

- Lifecycle Policies
- Cross-Region Replication (CRR)
- Same-Region Replication (SRR)
- Object Lock (WORM compliance)
- Pre-signed URLs

---

### 📌 Exam Focus

- S3 is **object storage**, not block
- Max object size = 5 TB
- Strong read-after-write consistency
- Glacier is integrated via lifecycle rules
- Gateway Endpoint supports S3
- Use versioning to protect against accidental deletes

---

### 🌍 Real-World Example

Social media platform storing user photos:

- S3 Standard for active photos
- Lifecycle policy moves older photos to Glacier
- CloudFront used for global delivery

---

---

## 🔹 Amazon S3 Glacier & Glacier Deep Archive

Low-cost archival storage for long-term retention.

Designed for data that is rarely accessed.

---

### 📦 Retrieval Options

- Expedited (minutes)
- Standard (hours)
- Bulk (lowest cost, longest time)

---

### 📌 Exam Focus

- Cheapest storage = Glacier Deep Archive
- Retrieval time is key decision factor
- Used for compliance, backups, archival

---

### 🌍 Real-World Example

Healthcare provider storing patient X-rays for 10+ years for compliance.

---

---

## 🔹 Amazon EBS (Elastic Block Store)

EBS provides persistent block storage for EC2.

It is AZ-specific.

---

### 💾 Volume Types

| Type | Use Case |
|------|----------|
| gp3 | General-purpose SSD |
| io2 | Provisioned IOPS |
| st1 | Throughput optimized HDD |
| sc1 | Cold HDD |

---

### 🔄 Features

- Snapshots (stored in S3)
- Encryption via KMS
- Attach/detach volumes
- Resize volumes
- RAID configurations supported

---

### 📌 Exam Focus

- EBS is block storage
- EBS is AZ-specific
- Snapshots are stored in S3
- Root volume delete-on-termination matters
- Only EC2 can attach EBS

---

### 🌍 Real-World Example

Database running on EC2 uses io2 EBS for high IOPS workload.

---

---

## 🔹 Amazon EFS (Elastic File System)

EFS provides scalable file storage using NFS protocol.

Designed for shared access across multiple EC2 instances.

---

### ⚙️ Features

- Automatically scales storage
- Multi-AZ availability
- POSIX compliant
- Supports thousands of concurrent connections
- Standard and One Zone storage classes

---

### 📌 Exam Focus

- EFS is file storage
- Multi-AZ
- Good for shared workloads
- Pay only for storage used

---

### 🌍 Real-World Example

Web servers sharing uploaded files across multiple EC2 instances.

---

---

## 🔹 Amazon FSx

Fully managed file systems for specialized workloads.

---

### 📂 FSx Variants

- **FSx for Windows File Server**
  - SMB protocol
  - Active Directory integration

- **FSx for Lustre**
  - High-performance workloads
  - Integrates with S3
  - Used for ML, HPC

- **FSx for NetApp ONTAP**
  - Enterprise workloads
  - Hybrid deployments

- **FSx for OpenZFS**
  - Linux workloads
  - Low latency

---

### 📌 Exam Focus

- Choose FSx when you need specific file system features
- Lustre for HPC & ML
- Windows FS for Microsoft workloads
- Integrates with S3 for data processing

---

### 🌍 Real-World Example

ML training workload using FSx for Lustre to process data stored in S3.

---

---

## 🔹 AWS Storage Gateway

Hybrid storage service connecting on-premises to AWS.

---

### 🏗 Gateway Types

- **File Gateway**
  - Store files in S3
  - Local cache for fast access

- **Volume Gateway**
  - Block storage backed by S3
  - iSCSI interface

- **Tape Gateway**
  - Replaces physical tape backups
  - Stores virtual tapes in Glacier

---

### 📌 Exam Focus

- Used in hybrid architectures
- Tape Gateway replaces traditional tape backup
- Helps migrate data to AWS gradually

---

### 🌍 Real-World Example

Bank replacing physical tape backups with virtual tapes stored in Glacier.

---

# ✅ Storage Section Complete
