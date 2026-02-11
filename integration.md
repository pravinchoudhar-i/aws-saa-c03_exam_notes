# 🔄 Application Integration – Deep Dive

A detailed and exam-focused breakdown of AWS Application Integration services.

---

## 🔹 Amazon SQS (Simple Queue Service)

Amazon SQS is a fully managed message queuing service.
 
It decouples and scales microservices, distributed systems, and serverless applications.

---

### 📦 Queue Types

#### 1️⃣ Standard Queue
- Unlimited throughput
- At-least-once delivery
- Best-effort ordering

#### 2️⃣ FIFO Queue
- Exactly-once processing
- Strict message ordering
- Lower throughput than Standard

---

### ⚙️ Key Features

- Message retention (1 minute to 14 days)
- Visibility timeout
- Dead Letter Queue (DLQ)
- Long polling
- Encryption via KMS

---

### 📌 Exam Focus

- SQS decouples applications
- FIFO for strict ordering
- DLQ for failed messages
- Visibility timeout prevents duplicate processing

---

### 🌍 Real-World Example

E-commerce app placing orders:

- Web server sends order to SQS
- Worker service processes order asynchronously
- Prevents system overload during traffic spikes

---

---

## 🔹 Amazon SNS (Simple Notification Service)

SNS is a fully managed pub/sub messaging service.

Used for pushing messages to multiple subscribers.

---

### 📡 Message Delivery Targets

- SQS
- Lambda
- HTTP/S endpoints
- Email
- SMS
- Mobile push notifications

---

### ⚙️ Features

- Fan-out architecture
- Message filtering
- Dead Letter Queue support
- Encryption via KMS

---

### 📌 Exam Focus

- SNS pushes messages (pub/sub)
- Often paired with SQS (fan-out pattern)
- Used for alerts & notifications

---

### 🌍 Real-World Example

Order placed → SNS notifies:
- Billing service
- Inventory service
- Shipping service

---

---

## 🔹 AWS Step Functions

Step Functions is a serverless workflow orchestration service.

It coordinates multiple AWS services into workflows.

---

### 🏗 Core Concepts

- State machine
- Tasks
- Choice states
- Parallel execution
- Error handling & retries

---

### ⚙️ Features

- Visual workflow builder
- Automatic retries
- Error handling
- Supports Lambda, ECS, SNS, SQS, etc.

---

### 📌 Exam Focus

- Used for orchestrating microservices
- Good for long-running workflows
- Better than custom code for coordination
- Integrates heavily with Lambda

---

### 🌍 Real-World Example

Loan processing workflow:

1. Validate application
2. Check credit score
3. Approve or reject
4. Send notification

All coordinated via Step Functions.

---

---

## 🔹 Amazon EventBridge

EventBridge is a serverless event bus service.

Enables event-driven architectures.

---

### ⚙️ Key Features

- Event routing
- SaaS integration
- Custom event buses
- Rule-based filtering
- Scheduled events (cron)

---

### 🔄 Integrations

- Lambda
- ECS
- Step Functions
- SNS
- SQS

---

### 📌 Exam Focus

- Event-driven architecture
- Replaces CloudWatch Events
- Routes events between services
- Works with SaaS applications

---

### 🌍 Real-World Example

When EC2 instance state changes → EventBridge triggers Lambda to notify admin.

---

---

## 🔹 Amazon AppFlow

AppFlow automates data transfer between AWS and SaaS applications.

---

### 🔄 Supported Integrations

- Salesforce
- SAP
- Slack
- Google Analytics
- S3
- Redshift

---

### ⚙️ Features

- No-code integration
- Scheduled or event-based flows
- Data transformation
- Encryption in transit & at rest

---

### 📌 Exam Focus

- SaaS integration service
- Secure data transfer
- No custom integration code required
- Used in data migration scenarios

---

### 🌍 Real-World Example

Syncing Salesforce customer data into Amazon Redshift for analytics.

---

# ✅ Application Integration Section Complete
