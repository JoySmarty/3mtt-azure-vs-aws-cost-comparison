# AWS vs Azure Cost Comparison Report

## 📌 Project Objective
This project evaluates the cost of hosting a small web application on AWS and Azure using equivalent infrastructure configurations. The goal is to understand cloud pricing models, identify cost drivers, and compare provider efficiency under identical workloads.

---

# 🏗️ Architecture Overview

Both cloud environments were designed to be equivalent in terms of:

## Compute
- AWS: EC2 t3.micro (Linux)
- Azure: B1s Virtual Machine (Linux & Windows with Azure Hybrid Benefit)

## Storage
- AWS: 32 GB EBS + 50 GB S3 Standard
- Azure: 32 GB Managed Disk + 50 GB Blob Storage

## Network
- Both platforms: 100 GB outbound internet traffic per month

---

# ☁️ AWS Cost Breakdown

| Component | Cost |
|----------|------|
| EC2 Compute (t3.micro) | $7.59 |
| EBS Storage (32 GB) | $2.56 |
| S3 Storage (50 GB) | $1.15 |
| Data Transfer (100 GB outbound) | $9.00 |
| **Total AWS Cost** | **$19.15/month** |

---

# ☁️ Azure Cost Breakdown

## Linux Scenario
| Component | Cost |
|----------|------|
| VM (B1s Linux) | $7.59 |
| Managed Disk (32 GB) | $2.40 |
| Blob Storage (50 GB) | $2.08 |
| **Total Azure Cost** | **$12.07/month** |

## Windows Scenario (Azure Hybrid Benefit)
| Component | Cost |
|----------|------|
| VM (B1s Windows + AHB) | $7.59 |
| Managed Disk (32 GB) | $2.40 |
| Blob Storage (50 GB) | $2.08 |
| **Total Azure Cost** | **$12.07/month** |

---

# 📊 Cost Comparison Summary

| Cloud Provider | Monthly Cost |
|----------------|-------------|
| AWS | $19.15 |
| Azure (Linux) | $12.07 |
| Azure (Windows AHB) | $12.07 |

---

# 🔍 Key Findings

## 1. AWS is more expensive for this workload
The main cost driver in AWS is **data transfer (network egress)**, which accounts for a significant portion of the total bill.

## 2. Azure provides more cost efficiency at small scale
Azure demonstrates lower total cost due to:
- Lower storage pricing
- Simplified billing model
- No significant network cost impact in this configuration

## 3. Compute cost is similar across both platforms
At small instance sizes, compute costs remain nearly identical.

---

# 🌐 Networking Cost Insight

AWS charges separately for outbound data transfer, which significantly increases total cost.

Azure includes network routing within the platform with minimal visible additional cost in this small-scale configuration.

---

# 💡 Discount Mechanisms

## AWS
- Savings Plans
- Reserved Instances
- Spot Instances

## Azure
- Reserved VM Instances
- Savings Plans for Compute
- Azure Hybrid Benefit (Windows licensing reduction)

---

# 🧠 Cost Optimization Strategies

## Strategy 1: Reduce Data Transfer
- Use CDN (CloudFront / Azure CDN)
- Reduce unnecessary outbound traffic
- Cache static content

## Strategy 2: Use Reserved Pricing
- AWS Savings Plans for EC2
- Azure Reserved Instances for VMs

---

# 📌 Conclusion

This comparison shows that Azure is more cost-effective for small web applications due to lower storage and simplified pricing structure. AWS provides more granular pricing control but results in higher overall cost, mainly driven by network egress charges.

Both platforms are suitable for production workloads, but cost efficiency depends heavily on architecture design and traffic patterns.