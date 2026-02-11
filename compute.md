# 🖥 Compute Services – Deep Dive

A detailed and exam-focused breakdown of AWS Compute services.

---

## 🔹 Amazon EC2 (Elastic Compute Cloud) 

Amazon EC2 provides resizable virtual servers in the cloud.

It gives full control over:

- Operating System  
- Networking  
- Storage  
- Security  

EC2 is **Infrastructure as a Service (IaaS)**.

---

### 🧱 AMI (Amazon Machine Image)

- Preconfigured OS template
- Includes OS + software + configurations
- Region-specific
- Can create custom AMIs
- Can be copied across regions
- Can be shared between AWS accounts

---

### 🖥 Instance Types

Grouped by workload category:

| Category | Use Case |
|-----------|----------|
| General Purpose (t, m) | Balanced workloads |
| Compute Optimized (c) | CPU-intensive apps |
| Memory Optimized (r, x) | Databases & caching |
| Storage Optimized (i, d) | High IOPS workloads |
| Accelerated (p, g) | Machine Learning & GPU |

---

### 💾 Storage Options

- **EBS** – Persistent block storage (AZ-specific)
- **Instance Store** – Ephemeral storage (data lost on stop/terminate)
- **EFS** – Shared file storage (multi-AZ)
- **FSx** – Specialized file systems (Windows, Lustre)

---

### 🌐 Networking

- Runs inside a VPC
- Private IP (always assigned)
- Public IP (optional)
- Elastic IP (static public IPv4)
- Security Groups (stateful firewall)
- NACLs (stateless subnet firewall)

---

### 💰 Pricing Models

- **On-Demand** → Pay per second/hour
- **Reserved Instances** → 1–3 year commitment
- **Savings Plans** → Flexible discount model
- **Spot Instances** → Up to 90% cheaper (interruptible)
- **Dedicated Hosts** → Physical server isolation
- **Capacity Reservations** → Reserve capacity in a specific AZ

---

### 🔁 High Availability & Scaling

- Auto Scaling Groups
- Elastic Load Balancer integration
- Multi-AZ deployment
- Placement Groups:
  - Cluster → Low latency
  - Spread → High availability
  - Partition → Big data workloads

---

### 📌 Important Exam Concepts

- Security Groups are **stateful**
- NACLs are **stateless**
- Public IP changes on stop/start
- Elastic IP remains static
- Spot instances can terminate anytime
- EBS volumes are AZ-specific
- Hibernation preserves RAM state
- Root volume delete-on-termination setting matters

---

### 🌍 Real-World Example

E-commerce application:

- EC2 web servers across 3 AZs
- Auto Scaling adjusts based on traffic
- ALB distributes traffic
- RDS in private subnet
- NAT Gateway for outbound internet access

---

---

## 🔹 Amazon ECS (Elastic Container Service)

Amazon ECS is AWS-native container orchestration.

Runs Docker containers without managing Kubernetes.

---

### 🚀 Launch Types

- **EC2 Launch Type** → You manage EC2 infrastructure
- **Fargate Launch Type** → Serverless containers (no server management)

---

### 🏗 Core Concepts

- **Cluster** – Logical grouping of compute resources
- **Task Definition** – Blueprint for container configuration
- **Task** – Running container
- **Service** – Maintains desired number of tasks

---

### 🔐 Security

- IAM roles per task
- Security groups per task (awsvpc mode)
- Integration with VPC networking

---

### 📌 Exam Focus

- ECS simpler than EKS
- Fargate = no infrastructure management
- Integrates tightly with ECR
- Often used with ALB
- Supports Auto Scaling of tasks

---

### 🌍 Real-World Example

Microservices application:

- User Service
- Payment Service
- Notification Service

Each runs as container in ECS Fargate.
ALB routes traffic based on path.

---

---

## 🔹 Amazon EKS (Elastic Kubernetes Service)

Amazon EKS is a managed Kubernetes service.

AWS manages the control plane.

---

### 🏗 Architecture

- Managed control plane
- Worker nodes (EC2 or Fargate)
- Pods
- Services
- Ingress

---

### 🔄 Scaling

- Cluster Autoscaler
- Horizontal Pod Autoscaler
- Fargate Profiles

---

### 🌐 Networking

- Uses VPC CNI
- Each pod receives its own IP
- Integrates with ALB Ingress Controller

---

### 📌 Exam Focus

- EKS = Kubernetes standard
- Best when portability required
- Supports hybrid deployments
- More complex than ECS
- Good for enterprises using Kubernetes already

---

### 🌍 Real-World Example

Enterprise migrating on-prem Kubernetes to AWS.
Maintains same kubectl and Helm workflows.

---

---

## 🔹 AWS Lambda

AWS Lambda is a serverless compute service.

Runs code in response to events.

---

### ⚙️ Key Characteristics

- Max execution time → 15 minutes
- Auto scaling
- Pay per request + duration
- Memory configurable (128MB – 10GB)
- Supports container images (up to 10GB)

---

### 🔄 Event Sources

- S3
- API Gateway
- DynamoDB Streams
- EventBridge
- SNS / SQS
- CloudWatch

---

### ❄ Cold Start

- First invocation may have delay
- Provisioned Concurrency reduces latency

---

### 📌 Exam Focus

- Stateless
- Event-driven architecture
- Ideal for unpredictable workloads
- Works well with API Gateway
- Runs inside VPC if required

---

### 🌍 Real-World Example

User uploads image → S3 triggers Lambda → image resized → stored back.

---

---

## 🔹 Amazon Lightsail

Amazon Lightsail is a simplified VPS hosting service.

Designed for easy deployment and predictable pricing.

---

### 🏗 Includes

- Compute
- Storage
- Static IP
- Built-in DNS
- Simple load balancing

---

### 📌 Exam Focus

- Best for simple applications
- Fixed monthly pricing
- Limited flexibility compared to EC2
- Good for beginners or small businesses

---

### 🌍 Real-World Example

Freelancer hosting WordPress blog with fixed monthly cost.

---

---

## 🔹 AWS Elastic Beanstalk

Elastic Beanstalk is a Platform as a Service (PaaS).

Deploy code → AWS manages infrastructure.

---

### 🏗 Supports

- Java
- Python
- Node.js
- .NET
- Docker
- PHP
- Ruby
- Go

---

### 🚀 Deployment Strategies

- All-at-once
- Rolling
- Rolling with additional batch
- Immutable

---

### 📌 Exam Focus

- Manages EC2, ELB, Auto Scaling automatically
- RDS should be created separately
- Suitable for long-running web applications
- Environment types: Web Server & Worker

---

### 🌍 Real-World Example

Startup deploying Node.js backend with automatic scaling and load balancing.

---

---

## 🔹 AWS Batch

AWS Batch is a managed batch processing service.

Runs containerized batch jobs at scale.

---

### 🏗 Core Components

- Job Definition
- Job Queue
- Compute Environment
- Managed or Unmanaged

---

### 💰 Cost Optimization

- Uses Spot Instances
- Auto scales compute resources

---

### 📌 Exam Focus

- For long-running compute workloads
- High-performance computing
- Simulations and rendering
- Not real-time like Lambda

---

### 🌍 Real-World Example

Movie studio rendering thousands of animation frames automatically.

---

# ✅ Compute Section Complete
