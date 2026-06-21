# ◈ VPC Subnet Architecture
**Course ID**: `263/264-[NF]-Lab`

## 🎯 Network Objective
This lab focuses on designing a robust VPC architecture. The objective is to organize cloud resources into logical subnets and establish internal network routing to ensure secure, scalable communication between tiers.

## 🚦 Traffic & Flow Logic
* **Logical Segmentation:** [Describe your approach, e.g., "Defined distinct public and private subnets across multiple Availability Zones to ensure high availability."]
* **Routing Path:** [E.g., "Configured custom route tables to direct public traffic through an Internet Gateway and isolated private traffic for internal-only access."]

## 📷 Lab Evidence
| Task | Connectivity Check | Evidence |
| :--- | :--- | :--- |
| **1** | VPC and Subnet Creation | ![Subnet_Config](./images/263_264_VPC_Subnets.png) |
| **2** | Route Table Association | ![Route_Table](./images/263_264_Route_Table.png) |
| **3** | Internal Resource Isolation | ![Isolation](./images/263_264_Private_Subnet.png) |

## 🛠️ Troubleshooting (The "Ping" Mindset)
* **Connectivity Roadblock:** [E.g., "Resources in the private subnet were unable to reach the internet for updates, even though the Route Table was configured."]
* **Diagnostic Steps:** [E.g., "Verified that the private subnet lacked a NAT Gateway association; validated that traffic was being routed to the local network only."]

## 📊 Technical Competence
* **Skills:** VPC Design, Subnetting (CIDR), Route Table Management, Multi-AZ Deployment, Network Security Principles.
