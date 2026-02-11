# 🖥 Compute Services – Deep Dive

A detailed and exam-focused breakdown of AWS Compute services.

---

## 🔹 Amazon EC2

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
- Can be shared across accounts

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
- **Instance Store** – Ephemeral storage (data lost on stop)
- **EFS** – Shared file system across instances
- **FSx** – Managed specialized file systems

---

### 🌐 Networking

- Runs inside a VPC
- Private IP (always assigned)
- Public IP (optional)
- Elastic IP (static public IP)
- Security Groups (stateful)
- NACLs (stateless)

---

### 💰 Pricing Models

- **On-Demand** → Pay per usage
- **Reserved Instances** → 1–3 year commitment
- **Savings Plans** → Flexible commitment model
- **Spot Instances** → Up to 90% cheaper (interruptible)
- **Dedicated Hosts** → Physical server isolation
- **Capacity Reservations** → Reserve AZ capacity

---

### 📌 Important Exam Concepts

- Security Groups are **stateful**
- NACLs are **stateless**
- Public IP changes on stop/start
- Elastic IP remains static
- Spot instances can terminate anytime
- EBS volumes are AZ-specific
- Placement Groups:
  - Cluster → Low latency
  - Spread → High availability
  - Partition → Big data workloads
- Hibernation preserves RAM state

---

### 🌍 Real-World Example

An e-commerce application:

- EC2 web servers across 3 AZs
- Auto Scaling Group adjusts capacity
- Application Load Balancer distributes traffic
- RDS in private subnet
- NAT Gateway for outbound internet access
