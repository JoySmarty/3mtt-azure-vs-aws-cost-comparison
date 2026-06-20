# 3mtt-azure-vs-aws-cost-comparison
Azure and AWS cost comparison


# ☁️ AWS vs Azure Cost Comparison Project

## 📌 Overview
This project compares the cost of hosting a small web application on Amazon Web Services (AWS) and Microsoft Azure. It evaluates compute, storage, and network costs across both providers using equivalent infrastructure configurations.

The goal is to understand cloud pricing models, identify cost drivers, and compare provider efficiency under identical workloads.

---

# 🏗️ Architecture Design

Both cloud environments were built using equivalent resources:

## 💻 Compute
- AWS: EC2 t3.micro (Linux)
- Azure: B1s Virtual Machine (Linux and Windows with Azure Hybrid Benefit)

## 💾 Storage
- AWS: 32 GB EBS + 50 GB S3 Standard
- Azure: 32 GB Managed Disk + 50 GB Blob Storage (Hot Tier)

## 🌐 Networking
- 100 GB outbound internet traffic per month on both platforms

---

# 💰 Final Cost Summary

| Cloud Provider | Monthly Cost |
|----------------|-------------|
| AWS | $19.15 |
| Azure (Linux) | $12.07 |
| Azure (Windows + AHB) | $12.07 |

---

# 🔗 Pricing Calculator Estimates

All estimates were created using official AWS and Azure pricing calculators.

---

## ☁️ AWS Estimates

- EC2 + EBS + Data Transfer  
  https://calculator.aws/#/estimate?id=55f6982aa0968d3aab67b3d28215f100cc59de92

- S3 Standard Storage (50 GB)  
  https://calculator.aws/#/estimate?id=9cbf0fb5a08d8db4cea351c161dd0c79b27b81ab

---

## ☁️ Azure Estimates

- Linux Virtual Machine (B1s)  
  https://azure.com/e/57fa6df226b142d28e37f845ccce6b1b

- Windows Virtual Machine (B1s + Azure Hybrid Benefit)  
  https://azure.com/e/fd30c5b1c6c547d2a19a549b862302c9

- Blob Storage (50 GB Hot Tier)  
  https://azure.com/e/7918d2f4d9db4408a97683c11dc84105

---

# 🔍 Key Insights

- AWS pricing is heavily influenced by data transfer (network egress).
- Azure provides lower overall cost for small workloads.
- Compute pricing is similar at entry-level instance sizes.
- Storage is more cost-efficient on Azure for this configuration.
- Azure Windows cost remains the same as Linux due to Azure Hybrid Benefit.

---

# ⚖️ Discount Mechanisms

## AWS
- Savings Plans
- Reserved Instances
- Spot Instances

## Azure
- Reserved Virtual Machines
- Savings Plans for Compute
- Azure Hybrid Benefit (Windows licensing optimization)

---

# 💡 Cost Optimization Strategies

- Use CDN/caching to reduce outbound data transfer
- Use Reserved Instances or Savings Plans for long-term workloads
- Right-size compute instances based on workload demand

---

# 📁 Project Structure

```

azure-vs-aws-cost-comparison/
│
├── docs/
│   ├── aws-estimate-summary.md
│   ├── azure-estimate-summary.md
│   ├── cost-comparison-report.md
│   ├── justification-summary.md
│
├── screenshots/
└── README.md

```

---

# 📸 Evidence

Screenshots of all pricing calculator configurations are included in the `/screenshots` folder for verification.

---

# 🧠 Conclusion

This project demonstrates that cloud pricing varies significantly based on provider structure and usage patterns. AWS offers detailed granular pricing but becomes more expensive due to data transfer costs. Azure provides a more cost-efficient structure for small-scale applications.

Both platforms are suitable for production workloads, but cost efficiency depends on workload design and architecture decisions.
```
