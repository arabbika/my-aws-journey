# ◈ VPC Subnet Architecture
**Course ID**: `263/264-[NF]-Lab`

## 🎯 Network Objective
This lab focused on designing a robust, production-grade VPC architecture. The objective was to organize cloud resources into logical subnets and establish internal/external network routing to ensure secure, scalable communication between application tiers.



## 🚦 Traffic & Flow Logic
* **Logical Segmentation:** Designed a VPC with distinct CIDR blocks to accommodate 15,000+ internal IPs. Segmented the environment into a Public Subnet (for edge connectivity) and Private Subnets (for backend resource isolation).
* **Routing Path:** Configured a custom Route Table for the public subnet, associating it with an Internet Gateway (IGW) via a `0.0.0.0/0` route. Implemented stateful/stateless security layers to control ingress and egress traffic.

## 📷 Lab Evidence
| Task | Connectivity Check | Evidence |
| :--- | :--- | :--- |
| **1** | VPC & CIDR Subnet Allocation | ![Subnet_Config](./images/263_264_VPC_Subnets.png) |
| **2** | Route Table & IGW Association | ![Route_Table](./images/263_264_Route_Table.png) |
| **3** | NACL/Security Group Verification | ![Security_Audit](./images/263_264_Private_Subnet.png) |

## 🛠️ Troubleshooting (The "Ping" Mindset)
* **Connectivity Roadblock:** After deploying the VPC and EC2 instance, the instance could not reach the internet (failed `ping` tests), despite being in a "Public" subnet.
* **Diagnostic Steps:** 1.  Verified the Route Table lacked a default route to the Internet Gateway.
    2.  Confirmed the Subnet was correctly associated with the configured Route Table.
    3.  Validated that both the Security Group (stateful) and NACL (stateless) permitted necessary traffic.
* **Engineering Resolution:** Added the IGW as the target for the `0.0.0.0/0` route and enabled "Auto-assign Public IP" for the instance, restoring full internet connectivity.

## 📊 Technical Competence
* **Skills:** VPC Design, CIDR/Subnetting Calculations, Route Table Management, IGW Configuration, NACL/Security Group Hardening, Multi-Tier Network Architecture.
