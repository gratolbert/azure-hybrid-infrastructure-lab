# Azure Hybrid Infrastructure Lab

## 📌 Overview

This project demonstrates the design and implementation of a hybrid cloud environment using Microsoft Azure. It simulates an on-premises infrastructure connected to Azure resources using VPN and Azure Arc.

## 🎯 Objectives

* Build a hybrid network architecture
* Deploy Azure Virtual Machines
* Configure secure connectivity (VPN)
* Onboard servers into Azure using Azure Arc
* Enable monitoring and observability

---

## 🏗️ Architecture

![Architecture Diagram](architecture/diagram.png)

---

## ⚙️ Technologies Used

* Microsoft Azure
* Azure Virtual Network (VNet)
* VPN Gateway (Point-to-Site)
* Azure Virtual Machines
* Azure Arc
* Log Analytics

---

## 🚀 Deployment Steps

### 1. Resource Group

* Created `rg-hybrid-lab` in Azure

### 2. Networking

* Configured VNet: `10.0.0.0/16`
* Subnets:

  * Default: `10.0.1.0/24`
  * GatewaySubnet

### 3. Virtual Machines

* Azure VM: `vm-azure-01`
* On-Prem Simulation: `vm-onprem-01`

### 4. Connectivity

* Configured VPN Gateway
* Enabled Point-to-Site VPN

### 5. Azure Arc

* Onboarded on-prem VM into Azure

### 6. Monitoring

* Enabled Log Analytics workspace
* Connected VMs for monitoring

---

## 📸 Screenshots

| Step | Description       |
| ---- | ----------------- |
| 1    | Resource Group    |
| 2    | Virtual Network   |
| 3    | Virtual Machines  |
| 4    | VPN Configuration |
| 5    | Azure Arc         |
| 6    | Monitoring        |

---

## 📚 Key Learnings

* Hybrid cloud architecture design
* Secure connectivity using VPN
* Managing on-prem resources with Azure Arc
* Monitoring cloud + hybrid workloads

---

## 🔥 Resume Value

This project demonstrates:

* Cloud engineering skills
* Hybrid infrastructure knowledge
* Real-world enterprise architecture patterns

---

## 📎 Future Enhancements

* Terraform deployment
* Site-to-Site VPN
* Azure Firewall integration
* CI/CD pipeline integration

---

## 👤 Author

Grant Tolbert

---
