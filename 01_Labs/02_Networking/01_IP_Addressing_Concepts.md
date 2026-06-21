# ◈ Networking Protocol Fundamentals
**Course ID**: `261/262-[NF]-Lab`

## 🎯 Network Objective
This lab focuses on mastering IP addressing schemes in the cloud. The objective is to distinguish between public and private address spaces and implement both static and dynamic IP configurations to ensure efficient network reachability.

## 🚦 Traffic & Flow Logic
* **Addressing Strategy:** [Describe your approach, e.g., "Assigned private CIDR blocks for internal instances while mapping public IPs for external edge connectivity."]
* **Protocol Implementation:** [E.g., "Configured DHCP sets for dynamic instance provisioning versus assigning Elastic IPs for static endpoint permanence."]

## 📷 Lab Evidence
| Task | Connectivity Check | Evidence |
| :--- | :--- | :--- |
| **1** | Public vs. Private IP Verification | ![IP_Check](./images/261_262_IP_Verification.png) |
| **2** | Dynamic IP Assignment Confirmation | ![DHCP_Config](./images/261_262_DHCP_Status.png) |
| **3** | Static IP/Elastic IP Association | ![EIP_Config](./images/261_262_EIP_Association.png) |

## 🛠️ Troubleshooting (The "Ping" Mindset)
* **Connectivity Roadblock:** [E.g., "Attempted to SSH into an instance using its private IP from a local machine, resulting in a connection timeout."]
* **Diagnostic Steps:** [E.g., "Used `traceroute` to identify the hop failure; verified the Route Table configuration and confirmed the absence of an Internet Gateway connection."]

## 📊 Technical Competence
* **Skills:** VPC Architecture, CIDR Calculation, DHCP/Static IP Lifecycle, Network Diagnostics, Route Table Management.
