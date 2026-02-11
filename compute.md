🖥 Compute Services – Deep Dive
🔹 1. Amazon EC2
📖 What It Is

Amazon EC2 provides resizable virtual servers in the cloud.

🏗 Core Components
🧱 AMI (Amazon Machine Image)

Preconfigured OS template

Includes OS + software + configurations

Region-specific

🖥 Instance Types
Type	Use Case
General Purpose	Balanced workloads
Compute Optimized	CPU-intensive
Memory Optimized	Databases
Storage Optimized	High IOPS
Accelerated	ML & GPU
📌 Exam Focus

Security Groups are stateful

Public IP changes after stop/start

Spot can terminate anytime

EBS is AZ-specific

🌍 Real-World Example

E-commerce app running across 3 AZs with ALB + Auto Scaling.
