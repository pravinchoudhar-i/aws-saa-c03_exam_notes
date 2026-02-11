# 🌐 Networking & Content Delivery – Deep Dive

A detailed and exam-focused breakdown of AWS Networking services.

---

## 🔹 Amazon VPC (Virtual Private Cloud)

Amazon VPC is a logically isolated virtual network in AWS. 

It allows you to control:

- IP address ranges
- Subnets
- Route tables
- Gateways
- Firewalls

---

### 🏗 Core Components

- **CIDR Block** → IP range (e.g., /16 to /28)
- **Subnets**
  - Public Subnet
  - Private Subnet
- **Route Tables**
- **Internet Gateway (IGW)**
- **NAT Gateway**
- **Security Groups**
- **Network ACLs**

---

### 🔐 Security Groups vs NACL

| Feature | Security Group | NACL |
|----------|----------------|------|
| Level | Instance | Subnet |
| Stateful | Yes | No |
| Allow/Deny | Allow only | Allow & Deny |

---

### 🔄 Connectivity Options

- VPC Peering (no transitive routing)
- Transit Gateway (hub model)
- VPN
- Direct Connect
- VPC Endpoints
  - Gateway Endpoint (S3, DynamoDB)
  - Interface Endpoint (PrivateLink)

---

### 📌 Exam Focus

- NAT Gateway → Private subnet outbound internet
- IGW → Public subnet internet access
- Gateway Endpoint supports only S3 & DynamoDB
- Security Groups are stateful
- VPC Peering is not transitive
- Transit Gateway supports multiple VPCs

---

### 🌍 Real-World Example

Three-tier architecture:

- Public subnet → ALB
- Private subnet → EC2 app servers
- Private subnet → RDS
- NAT Gateway for outbound access

---

---

## 🔹 Amazon Route 53

Route 53 is AWS’s DNS and domain management service.

---

### 🌍 Routing Policies

| Policy | Use Case |
|--------|----------|
| Simple | Single resource |
| Weighted | A/B testing |
| Latency-Based | Lowest latency routing |
| Geolocation | Based on user location |
| Failover | Active-passive DR |
| Multi-Value | Return multiple healthy IPs |

---

### 🩺 Health Checks

- Monitor endpoints
- Automatic failover
- Integrated with CloudWatch

---

### 📌 Exam Focus

- Weighted → Gradual migration
- Failover → Disaster recovery
- Latency-based → Global apps
- Route 53 integrates with CloudFront & ALB

---

### 🌍 Real-World Example

Global SaaS platform routing users to nearest region using latency-based routing.

---

---

## 🔹 Amazon CloudFront

CloudFront is a global Content Delivery Network (CDN).

Delivers content via Edge Locations.

---

### ⚙️ Key Features

- Edge caching
- Dynamic & static content support
- HTTPS via ACM
- Lambda@Edge
- Signed URLs & cookies
- Integrated with WAF & Shield

---

### 📌 Exam Focus

- Reduces latency globally
- Protects against DDoS
- Works with S3, ALB, API Gateway
- Lambda@Edge customizes requests

---

### 🌍 Real-World Example

Video streaming platform delivering content globally with low latency.

---

---

## 🔹 Elastic Load Balancing (ELB)

Distributes incoming traffic across multiple targets.

---

### ⚙️ Types of Load Balancers

| Type | Layer | Use Case |
|------|-------|----------|
| ALB | Layer 7 | HTTP/HTTPS apps |
| NLB | Layer 4 | TCP/UDP high performance |
| CLB | Legacy | Older apps |

---

### 🔄 Features

- Health Checks
- Cross-zone load balancing
- SSL termination
- Sticky sessions
- Auto Scaling integration

---

### 📌 Exam Focus

- ALB → Path-based routing
- NLB → Static IP
- Multi-AZ required
- Works with ECS & Auto Scaling

---

### 🌍 Real-World Example

E-commerce app distributing traffic across multiple EC2 instances in 3 AZs.

---

---

## 🔹 AWS Direct Connect

Dedicated private connection from on-prem to AWS.

---

### ⚙️ Key Features

- Private connectivity
- Lower latency
- Consistent bandwidth
- Bypasses public internet

---

### 📌 Exam Focus

- Used for hybrid architecture
- More reliable than VPN
- Often paired with VPN as backup

---

### 🌍 Real-World Example

Enterprise connecting corporate data center to AWS securely.

---

---

## 🔹 AWS Global Accelerator

Improves global application availability and performance.

Uses AWS global network instead of internet routing.

---

### ⚙️ Key Features

- Static IP addresses
- Health checks
- Automatic failover
- Uses AWS backbone network

---

### 📌 Exam Focus

- Improves global performance
- Not a CDN (CloudFront is CDN)
- Works for TCP/UDP apps

---

### 🌍 Real-World Example

Gaming platform reducing latency for players worldwide.

---

---

## 🔹 Amazon API Gateway

Managed service for creating and managing APIs.

---

### ⚙️ API Types

- REST API
- HTTP API
- WebSocket API

---

### 🔄 Integrations

- Lambda
- EC2
- ALB
- DynamoDB
- SQS

---

### 🔐 Features

- Throttling
- Authorization (IAM, Cognito)
- API Keys
- Usage plans
- Caching

---

### 📌 Exam Focus

- Often paired with Lambda
- Supports serverless architecture
- Built-in throttling & rate limiting
- Works with WAF

---

### 🌍 Real-World Example

Mobile app backend using API Gateway + Lambda to handle requests.

---

# ✅ Networking Section Complete
