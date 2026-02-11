🖥 Compute Services – Deep Dive
1️⃣ Amazon EC2 (Elastic Compute Cloud)
📖 What It Is

Amazon EC2 provides resizable virtual servers in the cloud.
It gives full control over OS, networking, storage, and security.

It is Infrastructure as a Service (IaaS).

🏗 Architecture Components
AMI (Amazon Machine Image)

Preconfigured OS template

Includes OS + software + configurations

Can create custom AMIs

Region-specific

Instance Types

Grouped by workload category:

Type	Use Case
General Purpose (t, m)	Balanced workloads
Compute Optimized (c)	CPU-intensive apps
Memory Optimized (r, x)	Databases, caching
Storage Optimized (i, d)	High IOPS workloads
Accelerated Computing (p, g)	ML, GPU workloads
⚙️ Storage Options

EBS (Block storage)

Instance Store (Ephemeral)

EFS (Shared file storage)

FSx (Specialized file systems)

🌐 Networking

Must launch inside a VPC

Each instance gets:

Private IP (always)

Public IP (optional)

Elastic IP (static public IP)

Security Groups (stateful firewall)

NACLs (subnet-level firewall)

💰 Pricing Models
Type	Description
On-Demand	Pay per hour/second
Reserved	1–3 year commitment
Savings Plans	Flexible discount model
Spot	Up to 90% cheaper, interruptible
Dedicated Host	Physical server dedicated to you
Capacity Reservation	Reserve capacity in AZ
🔁 Scaling & HA

Use Auto Scaling Groups

Use Elastic Load Balancer

Multi-AZ deployment

Placement Groups:

Cluster (low latency)

Spread (max HA)

Partition (big data workloads)

📌 Important Exam Concepts

Public IP changes on stop/start

Security Groups are stateful

EBS is AZ-specific

Spot instances can terminate anytime

Hibernation preserves RAM

Use Reserved for predictable workloads

Use Spot for fault-tolerant workloads

🌍 Real-World Example

An e-commerce app runs web servers on EC2.

Deployed across 3 AZs

Auto Scaling Group adjusts capacity

ALB distributes traffic

RDS in private subnet

NAT Gateway allows private instances internet access

2️⃣ Amazon ECS (Elastic Container Service)
📖 What It Is

AWS-native container orchestration service.

Manages Docker containers without needing Kubernetes.

🏗 Architecture
Cluster

Logical grouping of compute resources.

Task Definition

Blueprint of container:

Image

CPU

Memory

Port mappings

IAM role

Task

Running instance of a task definition.

Service

Maintains desired number of tasks.
Supports auto-scaling.

🚀 Launch Types
EC2 Launch Type

You manage EC2 cluster

More control

More responsibility

Fargate Launch Type

Serverless containers

No server management

Pay per execution

🔐 Security

Task-level IAM roles

VPC integration

Security groups per task (awsvpc mode)

📌 Exam Highlights

ECS simpler than EKS

Fargate = no infrastructure management

Works tightly with ECR

ALB commonly used with ECS

🌍 Real-World Example

Microservices architecture:

User service

Payment service

Notification service

Each runs as container in ECS Fargate.
ALB routes based on path.

3️⃣ Amazon EKS (Elastic Kubernetes Service)
📖 What It Is

Managed Kubernetes service.

AWS manages control plane.

🏗 Components

Control Plane (managed by AWS)

Worker Nodes (EC2 or Fargate)

Pods

Services

Ingress

🔄 Scaling

Cluster Autoscaler

Horizontal Pod Autoscaler

Fargate profiles

🔐 Security

IAM Roles for Service Accounts (IRSA)

Kubernetes RBAC

VPC CNI networking

📌 Exam Focus

EKS = portability

Supports hybrid cloud

15 read replicas not related (Aurora trick)

Pod gets its own IP (VPC CNI)

🌍 Example

Fintech running K8s on-prem migrates to EKS.
Maintains same kubectl workflows.

4️⃣ AWS Lambda
📖 What It Is

Serverless compute.
Runs code in response to events.

⚙️ Characteristics

Max execution: 15 minutes

Memory: 128MB–10GB

Auto scaling

Pay per request + duration

Supports container images (up to 10GB)

🔄 Triggers

S3

DynamoDB Streams

API Gateway

EventBridge

SNS/SQS

CloudWatch

❄ Cold Start

First invocation delay

Use Provisioned Concurrency to reduce

📌 Exam Focus

Stateless

Best for event-driven

No server management

Great with API Gateway

🌍 Example

S3 upload triggers Lambda → image resized → saved back.

5️⃣ Amazon Lightsail
📖 What It Is

Simplified VPS hosting.

Bundled pricing model.

🏗 Includes

Compute

Storage

Static IP

DNS

Load balancer

📌 Exam Clue

If question says:

“Simple”

“Predictable cost”

“No AWS expertise”

Answer = Lightsail.

🌍 Example

Freelancer hosts WordPress blog.

6️⃣ AWS Elastic Beanstalk
📖 What It Is

Platform as a Service (PaaS).

Deploy code → AWS handles infrastructure.

🏗 Supports

Java

Node.js

Python

.NET

Docker

🔄 Deployment Types

All-at-once

Rolling

Rolling with extra batch

Immutable

📌 Exam Focus

Beanstalk manages EC2, ELB, ASG

RDS best created separately

Good for long-running apps

🌍 Example

Startup deploys Node API.
Auto scaling handled by Beanstalk.

7️⃣ AWS Batch
📖 What It Is

Managed batch processing service.

Runs containerized batch jobs at scale.

🏗 Components

Job Definition

Job Queue

Compute Environment

Managed or Unmanaged

💰 Cost Optimization

Uses Spot Instances

Auto scales compute

📌 Exam Focus

Long-running workloads

HPC, simulations

Not real-time

Not event-based like Lambda

🌍 Example

Movie studio renders 10,000 frames.
Batch provisions compute automatically.

✅ Compute Section Complete
