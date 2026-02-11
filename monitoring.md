# 📊 Monitoring & Management – Deep Dive

A detailed and exam-focused breakdown of AWS Monitoring & Management services.

---

## 🔹 Amazon CloudWatch

CloudWatch is AWS’s monitoring and observability service.

It collects and tracks metrics, logs, and events from AWS resources.

---

### 📈 Core Capabilities

- Metrics collection (CPU, memory, network, etc.)
- Log monitoring (CloudWatch Logs)
- Alarms & notifications
- Dashboards
- Event monitoring (EventBridge integration)

---

### 📊 Metrics

- Default metrics from AWS services
- Custom metrics
- Detailed monitoring (1-minute granularity)

---

### 🚨 Alarms

- Trigger based on thresholds
- Send notifications via SNS
- Can trigger Auto Scaling actions

---

### 📌 Exam Focus

- Used for monitoring infrastructure
- CloudWatch Logs vs CloudTrail difference
- Can trigger scaling actions
- Works with Lambda, EC2, RDS, etc.

---

### 🌍 Real-World Example

Auto Scaling increases EC2 instances when CPU > 70%.

---

---

## 🔹 AWS CloudTrail

CloudTrail tracks API activity in your AWS account.

It records **who did what and when**.

---

### 📝 Logs Include

- IAM actions
- Resource creation/deletion
- Console logins
- API calls

---

### ⚙️ Features

- Stored in S3
- Multi-region support
- Log file integrity validation
- Integrated with CloudWatch

---

### 📌 Exam Focus

- CloudTrail = auditing
- Used for compliance
- Tracks API calls (not performance metrics)
- Can send logs to CloudWatch for alerts

---

### 🌍 Real-World Example

Security team detecting unauthorized IAM policy changes.

---

---

## 🔹 AWS Config

AWS Config monitors resource configuration changes.

Tracks compliance over time.

---

### 🔍 Capabilities

- Configuration history
- Compliance rules
- Resource inventory
- Change tracking

---

### 📜 Config Rules

- AWS-managed rules
- Custom rules (Lambda-based)

---

### 📌 Exam Focus

- Tracks configuration changes
- Not real-time metrics (CloudWatch does that)
- Used for compliance monitoring
- Works with SNS notifications

---

### 🌍 Real-World Example

Detecting if any S3 bucket becomes publicly accessible.

---

---

## 🔹 AWS Systems Manager (SSM)

SSM helps manage infrastructure at scale.

---

### 🛠 Key Features

- Session Manager (secure shell access without SSH)
- Patch Manager
- Parameter Store
- Run Command
- Automation
- Fleet Manager

---

### 🔐 Security Benefits

- No need to open port 22
- IAM-based access control
- Works inside private subnets

---

### 📌 Exam Focus

- Use Session Manager instead of SSH
- Parameter Store for configuration values
- Automation for operational tasks
- Helps manage EC2 at scale

---

### 🌍 Real-World Example

DevOps team patching hundreds of EC2 instances automatically.

---

---

## 🔹 AWS Trusted Advisor

Provides best practice recommendations.

---

### 📋 Categories

- Cost Optimization
- Performance
- Security
- Fault Tolerance
- Service Limits

---

### 📌 Exam Focus

- Identifies unused resources
- Helps reduce cost
- Checks for security risks
- Not real-time monitoring

---

### 🌍 Real-World Example

Identifying underutilized EC2 instances to reduce cost.

---

---

## 🔹 AWS Service Catalog

Helps manage approved AWS services within organizations.

---

### 🏗 Key Features

- Pre-approved service templates
- Portfolio management
- Governance control
- Integration with IAM & Organizations

---

### 📌 Exam Focus

- Used in large enterprises
- Standardizes infrastructure deployment
- Controls what services users can provision

---

### 🌍 Real-World Example

Enterprise allowing developers to deploy only approved EC2 configurations.

---

# ✅ Monitoring & Management Section Complete
