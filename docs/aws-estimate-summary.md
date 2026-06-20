# AWS Estimate Summary

## 📌 Project Overview
This document summarizes the AWS cost estimation for hosting a small web application using core cloud services: compute, storage, and networking.

---

# 🌍 Region
- US East (N. Virginia) — us-east-1

---

# 💻 Compute Layer (Amazon EC2)

## Configuration
- Instance Type: t3.micro
- Operating System: Linux
- Tenancy: Shared Instances
- Pricing Model: On-Demand
- Number of Instances: 1
- Usage: 730 hours/month (100% utilization)

## Cost
- EC2 Compute Cost: **$7.59/month**

---

# 💾 Block Storage (Amazon EBS)

## Configuration
- Volume Type: gp3 (General Purpose SSD)
- Storage Size: 32 GB
- Snapshot: Not enabled
- Performance: Default gp3 settings

## Cost Breakdown
- EBS Storage Cost: **$2.56/month**

---

# 🪣 Object Storage (Amazon S3)

## Configuration
- Storage Class: S3 Standard
- Data Stored: 50 GB
- Requests: Default (low traffic assumption)
- Data Transfer: Not separately charged in this estimate

## Cost Breakdown
- S3 Storage Cost: **$1.15/month**

---

# 🌐 Data Transfer (Networking)

## Configuration
- Outbound Internet Traffic: 100 GB/month
- Inbound Traffic: 0 GB

## Cost Breakdown
- Data Transfer Cost: **$9.00/month**

---

# 📊 AWS TOTAL COST SUMMARY

| Component | Monthly Cost |
|----------|--------------|
| EC2 Compute | $7.59 |
| EBS Storage (32 GB) | $2.56 |
| S3 Storage (50 GB) | $1.15 |
| Data Transfer (100 GB outbound) | $9.00 |
| **TOTAL** | **$19.30 (rounded AWS estimate: $19.15)** |

---

# 🧠 KEY INSIGHTS

## 1. Compute vs Network Cost
Although compute resources are low-cost, **data transfer (networking) is the largest cost driver**, accounting for nearly half of the total bill.

## 2. Storage Cost Efficiency
Both EBS and S3 remain relatively low-cost at small scale, but combined they contribute to baseline infrastructure cost.

## 3. Cost Structure Pattern
AWS follows a **granular pricing model**, where each component (compute, storage, network) is billed separately.

---

# 📌 CONCLUSION

This AWS configuration represents a small-scale web application with moderate traffic. The total monthly cost is driven primarily by outbound network usage rather than compute or storage resources.

This highlights the importance of optimizing data transfer in cloud architecture to reduce long-term operational costs.