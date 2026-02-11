# 🔐 Security, Identity & Compliance – Deep Dive

A detailed and exam-focused breakdown of AWS Security services.

---

## 🔹 AWS IAM (Identity and Access Management)

IAM controls access to AWS resources.

It defines **who can access what**.

---

### 🏗 Core Components

- **Users** → Individual identities
- **Groups** → Collection of users 
- **Roles** → Temporary credentials for services/users
- **Policies** → JSON documents defining permissions

---

### 📜 Policy Types

- Identity-based policies
- Resource-based policies
- Inline policies
- Managed policies

---

### 🔐 Security Features

- MFA (Multi-Factor Authentication)
- Password policies
- IAM Access Analyzer
- IAM Policy Simulator

---

### 📌 Exam Focus

- IAM is global service
- Root user should not be used
- Roles are preferred over access keys
- Least privilege principle
- STS provides temporary credentials

---

### 🌍 Real-World Example

EC2 instance assumes IAM role to access S3 securely without storing access keys.

---

---

## 🔹 Amazon Cognito

Cognito provides authentication and authorization for applications.

---

### 🏗 Components

- **User Pools** → Authentication (sign-in/sign-up)
- **Identity Pools** → Temporary AWS credentials

---

### ⚙️ Features

- Social login (Google, Facebook)
- MFA support
- JWT tokens
- Integration with API Gateway

---

### 📌 Exam Focus

- Used for mobile/web app authentication
- Works with IAM roles
- Often used with API Gateway

---

### 🌍 Real-World Example

Mobile app allowing users to sign in with Google and access backend APIs.

---

---

## 🔹 AWS Secrets Manager

Stores and rotates secrets securely.

---

### 🔐 Features

- Automatic secret rotation
- Integration with RDS
- Encryption via KMS
- Fine-grained IAM access control

---

### 📌 Exam Focus

- Used for DB credentials
- Rotates secrets automatically
- Better than storing credentials in code

---

### 🌍 Real-World Example

Application retrieving database password securely from Secrets Manager.

---

---

## 🔹 AWS KMS (Key Management Service)

Managed encryption key service.

---

### 🔑 Key Types

- AWS-managed keys
- Customer-managed keys (CMK)
- Customer-provided keys

---

### ⚙️ Features

- Integrated with most AWS services
- Automatic key rotation
- Envelope encryption
- CloudTrail logging

---

### 📌 Exam Focus

- KMS is regional
- Used with S3, EBS, RDS, etc.
- Customer-managed keys give more control

---

### 🌍 Real-World Example

Encrypting S3 bucket with customer-managed KMS key.

---

---

## 🔹 AWS CloudHSM

Dedicated hardware security module.

Provides hardware-based encryption.

---

### ⚙️ Key Characteristics

- Single-tenant HSM
- FIPS 140-2 Level 3 compliance
- Full control of keys
- More expensive than KMS

---

### 📌 Exam Focus

- Choose CloudHSM when regulatory compliance requires dedicated hardware
- More control than KMS

---

### 🌍 Real-World Example

Financial institution requiring hardware-based key storage.

---

---

## 🔹 Amazon GuardDuty

Threat detection service.

Analyzes logs to detect malicious activity.

---

### 🔎 Monitors

- VPC Flow Logs
- DNS Logs
- CloudTrail events

---

### 📌 Exam Focus

- No agent required
- Continuous threat monitoring
- Detects compromised EC2 instances

---

### 🌍 Real-World Example

Detecting unusual API calls from compromised IAM credentials.

---

---

## 🔹 Amazon Inspector

Automated security assessment service.

---

### 🔎 Scans

- EC2 instances
- Container images (ECR)
- Lambda functions

---

### 📌 Exam Focus

- Vulnerability scanning
- CVE detection
- Continuous monitoring

---

### 🌍 Real-World Example

Scanning EC2 instances for outdated packages.

---

---

## 🔹 Amazon Macie

Data security and classification service.

Uses machine learning to discover sensitive data.

---

### 🔍 Detects

- Personally Identifiable Information (PII)
- Financial data
- Sensitive documents in S3

---

### 📌 Exam Focus

- Focuses on S3
- Data classification
- Helps with compliance

---

### 🌍 Real-World Example

Detecting unencrypted PII stored in S3 bucket.

---

---

## 🔹 AWS WAF (Web Application Firewall)

Protects applications from common web exploits.

---

### ⚙️ Features

- IP filtering
- SQL injection protection
- XSS protection
- Rate-based rules
- Works with ALB & CloudFront

---

### 📌 Exam Focus

- Protects against Layer 7 attacks
- Often paired with CloudFront
- Integrated with Shield

---

### 🌍 Real-World Example

Blocking malicious IP addresses attacking login endpoint.

---

---

## 🔹 AWS Shield

DDoS protection service.

---

### 🛡 Shield Types

- Shield Standard (automatic, free)
- Shield Advanced (paid, enhanced protection)

---

### 📌 Exam Focus

- Protects against DDoS
- Works with CloudFront, ALB, Route 53
- Advanced provides cost protection

---

### 🌍 Real-World Example

Protecting high-traffic website from DDoS attack.

---

---

## 🔹 AWS Artifact

Provides compliance reports and agreements.

---

### 📄 Includes

- SOC reports
- ISO certifications
- PCI compliance documents

---

### 📌 Exam Focus

- Used for compliance documentation
- Not a monitoring tool
- Access to audit reports

---

### 🌍 Real-World Example

Company downloading SOC report for compliance audit.

---

# ✅ Security Section Complete
