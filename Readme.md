# Azure Hybrid Infrastructure Lab
![Azure](https://img.shields.io/badge/Azure-Hybrid%20Lab-blue)
![Linux](https://img.shields.io/badge/Linux-Ubuntu-green)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Project Type](https://img.shields.io/badge/Type-Hybrid%20Infrastructure-orange)
## 📌 Overview

This project demonstrates the deployment of a hybrid cloud infrastructure using Microsoft Azure. It simulates an on-premises environment connected to Azure resources, incorporating networking, monitoring, and hybrid management concepts.

---

## Table of Contents

- Overview
- Objectives
- Architecture
- Technologies Used
- Deployment Summary
- Challenges & Solutions
- Key Learnings
- Resume Value
- Future Improvements
---

## 🎯 Objectives

* Deploy and configure Azure infrastructure components
* Simulate hybrid architecture using cloud-based resources
* Enable monitoring and observability
* Understand Azure Arc use cases and limitations
* Demonstrate real-world troubleshooting and adaptability

---
## Architecture Overview

![Hybrid Architecture](architecture/architecture-diagram.png)

## Azure Resource Deployment

![Azure Resource Layout](architecture/resource-layout.png)

## Network Traffic Flow

![Network Traffic Flow](architecture/network-traffic-flow.png)
---

## ⚙️ Technologies Used

* Microsoft Azure
* Azure Virtual Machines (Linux)
* Azure Virtual Network (VNet)
* Network Security Groups (NSG)
* Log Analytics Workspace
* Azure Monitor (VM Insights)
* Azure Arc (conceptual implementation)

---

## 🚀 Deployment Summary

### 1. Resource Group

* Created `rg-hybrid-lab` to organize all resources

### 2. Networking

* Configured VNet: 10.0.0.0/16
* Subnet: 10.0.1.0/24
* Enabled internal VM communication

### 3. Virtual Machines

* `vm-azure-01` (cloud workload)
* `vm-onprem-01` (on-prem simulation)
* Ubuntu 24.04 LTS
* Deployed using available DC-series SKU due to regional constraints

### 4. Hybrid Architecture Simulation

* Simulated on-prem environment within Azure
* Validated internal communication via private IPs

### 5. Azure Arc (Conceptual Implementation)

* Attempted onboarding of Azure VM
* Identified limitation: Azure Arc does not support Azure-native VMs
* Documented real-world use case for external/on-prem systems

### 6. Monitoring & Observability

* Created Log Analytics Workspace: `law-hybrid-lab`
* Enabled VM Insights for both VMs
* Verified telemetry and performance metrics

---

## 📸 Screenshots

Stored in `/screenshots/`:

* Resource Group creation
* Virtual Network configuration
* VM deployment
* SSH connectivity
* Monitoring enabled
* Network validation

---

## ⚠️ Challenges & Solutions

### Challenge 1: VM Size Restrictions

* Limited SKU availability across regions
* B-series and A-series unavailable

**Solution:**

* Adapted to available DC-series VM sizes

---

### Challenge 2: Region Inconsistencies

* Different regions exposed different VM capabilities

**Solution:**

* Standardized deployment within a single region

---

### Challenge 3: Azure Arc Limitation

* Azure Arc agent cannot be installed on Azure VMs

**Solution:**

* Documented limitation
* Positioned Arc as hybrid/multi-cloud solution

---

## 🧠 Key Learnings

* Azure resource availability varies by region and subscription state
* Real-world cloud deployments require adaptability
* Azure Arc is designed for non-Azure environments
* Monitoring is critical for visibility and operations
* Troubleshooting is a core cloud engineering skill

---

## 🔥 Resume Value

This project demonstrates:

* Cloud infrastructure deployment
* Hybrid architecture design
* Azure networking fundamentals
* Monitoring and observability
* Real-world troubleshooting experience

---

## 🚀 Future Improvements

Possible enhancements for this project include:

* Deploying a real on-premises VM using VMware or VirtualBox
* Connecting environments using a Site-to-Site VPN
* Automating deployment with Terraform
* Adding Azure Bastion for secure VM access
* Implementing Azure Policy for governance
