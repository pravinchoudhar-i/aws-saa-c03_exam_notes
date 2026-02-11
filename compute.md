# 🖥 Compute Services – Deep Dive

A detailed breakdown of AWS Compute services for exam-focused understanding.

---

## 🔹 Amazon EC2

Amazon EC2 provides resizable virtual servers in the cloud.

It gives full control over:

- Operating System  
- Networking  
- Storage  
- Security  

EC2 is **Infrastructure as a Service (IaaS)**.

### Core Components

- **AMI (Amazon Machine Image)**  
  - Preconfigured OS template  
  - Includes OS + software + configuration  
  - Region-specific  
  - Can create custom AMIs  

- **Instance Types**
  - General Purpose → Balanced workloads  
  - Compute Optimized → CPU-intensive workloads  
  - Memory Optimized → Databases & caching  
  - Storage Optimized → High IOPS workloads  
  - Accelerated Computing → ML & GPU workloads  

- **Storage Options**
  - EBS (Persistent block storage)  
  - Instance Store (Temporary storage)  
  - EFS (Shared file storage)  
  - FSx (Specialized file systems)  

### Pricing Models

- On-Demand  
- Reserved Instances  
- Savings Plans  
- Spot Instances  
- Dedicated Hosts  
- Capacity Reservations  

### Exam Focus

- Security Groups are **stateful**
- Public IP changes after stop/start
- Spot instances can terminate anytime
- EBS is AZ-specific
- Placement Groups:
  - Cluster → Low latency
  - Spread → High availability
  - Partition → Big data workloads

### Real-World Example

E-commerce application running across multiple AZs with:
- Auto Scaling
- Application Load Balancer
- RDS in private subnet

---

## 🔹 Amazon ECS

Amazon ECS is AWS-native container orchestration.

It allows you to run Docker containers without managing Kubernetes.

### Launch Types

- **EC2 Launch Type** → You manage EC2 infrastructure  
- **Fargate Launch Type** → Serverless containers  

### Core Concepts

- Cluster  
- Task Definition  
- Task  
- Service  

### Exam Focus

- ECS is simpler than EKS
- Fargate = No infrastructure management
- Integrates tightly with ECR
- Commonly used with ALB

### Real-World Example

Microservices architecture:
- User Service  
- Payment Service  
- Notification Service  

Each service runs in containers on ECS Fargate.

---

## 🔹 Amazon EKS

Amazon EKS is a managed Kubernetes service.

AWS manages the control plane.

### Key Characteristics

- Kubernetes standard
- Portable across environments
- Supports EC2 or Fargate worker nodes
- Uses VPC CNI networking

### Exam Focus

- Choose EKS when Kubernetes compatibility is required
- Good for hybrid or multi-cloud
- More complex than ECS

### Real-World Example

Fintech company migrating on-prem Kubernetes clusters to AWS.

---

## 🔹 AWS Lambda

AWS Lambda is a serverless compute service.

Runs code in response to events.

### Key Characteristics

- Max execution time: 15 minutes  
- Automatic scaling  
- Pay per request + duration  
- Event-driven architecture  

### Common Triggers

- S3  
- API Gateway  
- DynamoDB Streams  
- EventBridge  
- SNS / SQS  

### Exam Focus

- Stateless
- Ideal for unpredictable workloads
- Often paired with API Gateway

### Real-World Example

Image uploaded to S3 triggers Lambda → resized → stored back.

---

## 🔹 Amazon Lightsail

Amazon Lightsail is a simplified VPS service.

Designed for easy deployment and predictable pricing.

### Includes

- Compute
- Storage
- Static IP
- Built-in DNS
- Simple load balancing

### Exam Focus

- Best when simplicity is required
- Fixed monthly pricing
- Limited flexibility compared to EC2

### Real-World Example

Developer hosting a WordPress portfolio site.

---

## 🔹 AWS Elastic Beanstalk

Elastic Beanstalk is a Platform as a Service (PaaS).

Deploy code → AWS manages infrastructure.

### Supports

- Java
- Python
- Node.js
- .NET
- Docker

### Deployment Strategies

- All-at-once  
- Rolling  
- Rolling with additional batch  
- Immutable  

### Exam Focus

- Manages EC2, ELB, Auto Scaling automatically
- RDS should be created separately for safety
- Good for long-running applications

### Real-World Example

Startup deploying Node.js backend with automatic scaling.

---

## 🔹 AWS Batch

AWS Batch is a managed batch processing service.

Runs containerized jobs at scale.

### Key Characteristics

- Job Queues
- Compute Environments
- Uses Spot for cost optimization
- Scales automatically

### Exam Focus

- For long-running compute jobs
- HPC workloads
- Not event-driven like Lambda

### Real-World Example

Rendering thousands of animation frames automatically.
