# Justification Summary

This project compares the cost of hosting a small web application on Amazon Web Services (AWS) and Microsoft Azure using equivalent infrastructure configurations. The goal is to evaluate pricing differences, identify key cost drivers, and understand how architectural decisions affect cloud expenses.

The AWS environment was configured using a t3.micro EC2 instance running Linux, with 32 GB of EBS storage, 50 GB of S3 object storage, and 100 GB of outbound internet traffic. The Azure environment used a B1s virtual machine with equivalent storage using Managed Disks and Blob Storage, including both Linux and Windows (with Azure Hybrid Benefit) scenarios.

The results show that AWS has a higher monthly cost of approximately $19.15, while Azure costs approximately $12.07 for the same workload. The primary reason for this difference is AWS’s separate and higher pricing for outbound data transfer, which significantly increases the total monthly bill. Azure, on the other hand, has more consolidated pricing for small workloads, with lower storage costs and less impact from networking charges in this configuration.

Both providers offer similar compute pricing at the entry level; however, AWS provides more granular billing across services, while Azure offers a simpler and more predictable pricing structure.

From a cost optimization perspective, both platforms provide discount mechanisms such as AWS Savings Plans and Azure Reserved Instances. Additionally, Azure Hybrid Benefit reduces Windows licensing costs, although its impact is minimal at small instance sizes.

In conclusion, Azure is more cost-effective for small-scale web applications, while AWS offers greater flexibility and service granularity for more complex or large-scale architectures. The choice between both providers should depend on workload size, traffic patterns, and long-term scalability requirements.