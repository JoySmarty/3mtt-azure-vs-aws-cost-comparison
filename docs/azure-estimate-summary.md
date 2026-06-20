# Azure Estimate Summary

## 📌 Project Overview
This document summarizes the Azure cost estimation for hosting a small web application using equivalent cloud services to AWS. The architecture includes compute, storage, and networking components.

---

# 🌍 Region
- East US

---

# 💻 Compute Layer (Azure Virtual Machines)

## Configuration
- Instance Type: B1s
- Operating System: Linux / Windows (comparison scenario)
- VM Size: 1 vCPU, 1 GB RAM
- Usage: 730 hours/month (100% utilization)
- Pricing Model: Pay-as-you-go

## Cost
- Linux VM: **$7.59/month**
- Windows VM (Azure Hybrid Benefit): **$7.59/month**

---

# 💾 Block Storage (Managed Disks)

## Configuration
- Disk Type: Standard SSD (E4)
- Size: 32 GB
- Redundancy: LRS
- Attached to VM

## Cost
- Managed Disk: **$2.40/month (Linux only scenario applied)**

---

# 🪣 Object Storage (Azure Blob Storage)

## Configuration
- Storage Type: Block Blob Storage (General Purpose v2)
- Access Tier: Hot
- Redundancy: LRS
- Capacity: 50 GB
- Flat namespace enabled

## Cost Breakdown
- Storage Capacity: $1.04/month
- Operations (read/write/list): ~$1.04/month

## Total Blob Storage Cost
- **$2.08/month**

---

# 🌐 Networking (Data Transfer)

## Configuration
- Outbound Internet Traffic: 100 GB/month
- Region: East US
- Routing: Microsoft Global Network

## Cost
- Included in VM estimate (no additional charge in this configuration)

---

# 📊 AZURE TOTAL COST SUMMARY

## Linux Scenario
| Component | Cost |
|----------|------|
| VM (B1s Linux) | $7.59 |
| Disk (32 GB) | $2.40 |
| Blob Storage (50 GB) | $2.08 |
| **Total** | **$12.07/month** |

---

## Windows Scenario (Hybrid Benefit)
| Component | Cost |
|----------|------|
| VM (B1s Windows + AHB) | $7.59 |
| Disk (32 GB) | $2.40 |
| Blob Storage (50 GB) | $2.08 |
| **Total** | **$12.07/month** |

---

# 🧠 KEY INSIGHTS

## 1. Compute Dominates Cost Structure
The B1s instance represents the largest portion of cost in Azure at small scale.

## 2. Storage is Predictable and Low Cost
Both managed disks and blob storage remain relatively inexpensive.

## 3. Hybrid Benefit Impact is Minimal at Small Scale
Windows licensing savings are not significantly reflected at the B1s level.

---

# 📌 CONCLUSION

Azure demonstrates a simplified and cost-efficient pricing model for small workloads, with predictable storage pricing and minimal licensing impact at low instance sizes. This makes it suitable for lightweight web applications and development environments.