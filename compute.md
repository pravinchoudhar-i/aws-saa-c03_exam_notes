🖥 Compute Services – Deep Dive
1️⃣ Amazon EC2
📖 What It Is

Amazon EC2 provides resizable virtual servers in the cloud.

It gives full control over:

Operating System

Networking

Storage

Security

EC2 is Infrastructure as a Service (IaaS).

🏗 Core Components
🧱 AMI (Amazon Machine Image)

Preconfigured OS template

Includes OS + software + configurations

Can create custom AMIs

Region-specific

🖥 Instance Types

Grouped by workload category:

General Purpose (t, m) → Balanced workloads

Compute Optimized (c) → CPU-intensive apps

Memory Optimized (r, x) → Databases & caching

Storage Optimized (i, d) → High IOPS workloads

Accelerated (p, g) → ML & GPU workloads

💾 Storage Options

EBS – Persistent block storage

Instance Store – Temporary storage

EFS – Shared file storage

FSx – Specialized file systems

💰 Pricing Models

On-Demand

Reserved Instances

Savings Plans

Spot Instances

Dedicated Hosts

Capacity Reservations

📌 Exam Focus

Security Groups are stateful

Public IP changes after stop/start

Spot instances can terminate anytime

Placement Groups:

Cluster → Low latency

Spread → High availability

Partition → Big data workloads

EBS is AZ-specific
