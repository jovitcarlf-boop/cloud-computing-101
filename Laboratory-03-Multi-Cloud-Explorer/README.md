# Laboratory-03: Multi-Cloud Explorer

## 📋 Mission Overview

This laboratory activity is part of CCM101 - Cloud Computing course. The mission is to explore and compare three major cloud platforms: Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP). As a Cloud Solutions Architect, I researched these platforms, analyzed their capabilities, and provided recommendations for different business scenarios.

---

## 🎯 Mission Objectives Completed

- ✅ Explored the major public cloud platforms (AWS, Azure, GCP)
- ✅ Identified the core services offered by each platform
- ✅ Compared cloud services across different providers
- ✅ Analyzed business requirements and recommended appropriate cloud solutions
- ✅ Created professional technical documentation using Markdown
- ✅ Developed a well-organized GitHub Cloud Computing Portfolio

---

## 📂 Repository Structure

```
Laboratory-03-Multi-Cloud-Explorer/
├── README.md (this file)
├── aws-research.md (AWS investigation)
├── azure-research.md (Azure investigation)
├── gcp-research.md (GCP investigation)
├── cloud-platform-comparison.md (Comparison tables and analysis)
├── client-recommendations.md (Business scenario solutions)
├── reflection.md (Personal reflection on learning)
└── screenshots/ (Evidence and documentation)
    ├── aws-homepage.png
    ├── azure-homepage.png
    ├── gcp-homepage.png
    └── killercoda-terminal.png
```

---

## 🔍 Linux Investigation - Server Migration Analysis

### Operating System Information

When investigating a Linux server using the following commands:

```bash
uname -a
```

**Result:** Linux server running on x86_64 architecture with kernel version 5.15 or higher. This identifies the operating system type and version needed for cloud migration planning.

### CPU Information

```bash
lscpu
```

**Result:** Processor cores and thread count determine which cloud VM size is appropriate. A typical investigation shows processors with 2-8 cores, helping determine AWS t3.medium, Azure Standard_B2s, or GCP e2-medium equivalent VM sizes.

### Memory Analysis

```bash
free -h
```

**Result:** RAM availability typically ranges from 2GB to 16GB. This information is critical for selecting the correct cloud instance type that matches current workload requirements.

### Disk Space Capacity

```bash
df -h
```

**Result:** Storage requirements guide decisions on object storage (S3, Blob Storage, Cloud Storage) versus block storage (EBS, Managed Disks, Persistent Disks).

---

## ☁️ Cloud Migration Mapping

### If this Linux server were migrated to the cloud:

**AWS Services Available:**
- EC2 (Elastic Compute Cloud) would host the Linux virtual machine
- EBS (Elastic Block Store) would provide persistent block storage
- S3 (Simple Storage Service) would store backups and data
- Security Groups would manage network access and firewall rules

**Microsoft Azure Services Available:**
- Virtual Machines with Linux images would host the server
- Managed Disks would provide storage with automatic redundancy
- Azure Storage Accounts would store backups and files
- Network Security Groups would control network traffic

**Google Cloud Platform Services Available:**
- Compute Engine would provide Linux virtual machine instances
- Persistent Disks would offer block storage with automatic snapshots
- Cloud Storage would store backups and large data files
- Firewall rules would manage network security and access control

---

## 📊 Key Findings

### Recommended Cloud Platform by Use Case:

| Use Case | Best Platform | Reason |
|----------|---------------|--------|
| **Startup** | AWS | Free tier, broadest services, largest community |
| **Microsoft Organization** | Azure | Seamless integration with Windows and Office 365 |
| **AI/ML Development** | GCP | Superior machine learning tools and expertise |
| **Global E-Commerce** | AWS | 30+ regions with CloudFront content delivery |

---

## 💡 Learning Outcomes

Through this mission, I have learned to:
1. Think like a Cloud Solutions Architect by matching business requirements to cloud services
2. Compare cloud platforms objectively based on features and cost
3. Recommend appropriate solutions for different organizational needs
4. Understand how Linux infrastructure maps to cloud services
5. Document technical decisions using professional Markdown

---

## 🚀 How to Use This Repository

1. Review the individual research files (aws-research.md, azure-research.md, gcp-research.md)
2. Study the cloud-platform-comparison.md for detailed service comparisons
3. Read client-recommendations.md to see real-world scenario analysis
4. Check the reflection.md for learning insights
5. View screenshots folder for evidence of research

---

## 📝 Submission Details

- **Course:** CCM101 - Cloud Computing
- **Laboratory:** 03 - Multi-Cloud Explorer
- **Student:** Fulgencio, Jovit Carl N
- **Repository:** GitHub Cloud Computing Portfolio
- **Submission Date:** 09/03/2026

---

**Status:** ✅ COMPLETE

This mission has been successfully completed with all required checkpoints addressed and documented.
