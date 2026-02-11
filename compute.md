# 🖥 Compute Services – Deep Dive

---

# 1️⃣ Amazon EC2

---

## 📖 What It Is

Amazon EC2 provides resizable virtual servers in the cloud.

It gives full control over:
- Operating System
- Networking
- Storage
- Security

EC2 is **Infrastructure as a Service (IaaS)**.

---

## 🏗 Core Components

### 🧱 AMI (Amazon Machine Image)

- Preconfigured OS template
- Includes OS + software + configurations
- Can create custom AMIs
- Region-specific

---

### 🖥 Instance Types

Grouped by workload category:

- **General Purpose (t, m)** → Balanced workloads
- **Compute Optimized (c)** → CPU-intensive apps
- **Memory Optimized (r, x)** → Databases & caching
- **Storage Optimized (i, d)** → High IOPS workloads
- **Accelerated (p, g)** → ML & GPU workloads

---

## 💾 Storage Options

- **EBS** – Persistent block storage
- **Instance Store** – Temporary storage
- **EFS** – Shared file storage
- **FSx** – Specialized file systems

---

## 💰 Pricing Models

- On-Demand
- Reserved Instances
- Savings Plans
- Spot Instances
- Dedicated Hosts
- Capacity Reservations

---

## 📌 Exam Focus

- Security Groups are **stateful**
- Public IP changes after stop/start
- Spot instances can terminate anytime
- Placement Groups:
  - Cluster → Low latency
  - Spread → High availability
  - Partition → Big data workloads
- EBS is AZ-specific

---

## 🌍 Real-World Example

E-commerce platform:
- EC2 web servers across 3 AZs
- ALB distributes traffic
- Auto Scaling handles traffic spikes
- RDS in private subnet

---

---

# 2️⃣ Amazon ECS

---

## 📖 What It Is

AWS-native container orchestration service.

Runs Docker containers without managing Kubernetes.

---

## 🚀 Launch Types

### EC2 Launch Type
You manage EC2 infrastructure.

### Fargate Launch Type
Serverless containers. No server management.

---

## 🏗 Core Concepts

- **Cluster**
- **Task Definition**
- **Task**
- **Service**

---

## 📌 Exam Focus

- ECS is simpler than EKS
- Fargate = serverless containers
- Works tightly with ECR
- ALB used for routing

---

## 🌍 Real-World Example

Microservices app:
- User Service
- Payment Service
- Notification Service

Each runs as container in ECS Fargate.
ALB routes traffic by path.

---

---

# 3️⃣ Amazon EKS

---

## 📖 What It Is

Managed Kubernetes service.

AWS manages control plane.

---

## 🏗 Architecture

- Managed Control Plane
- Worker Nodes (EC2 or Fargate)
- Pods
- Services
- Ingress

---

## 📌 Exam Focus

- EKS = portability
- Kubernetes standard
- Supports hybrid
- Uses VPC CNI for networking

---

## 🌍 Example

Company migrates on-prem Kubernetes to EKS.
Keeps same kubectl workflows.

---

