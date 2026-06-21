# ◈ Secure VPC Web Server Deployment
**Course ID**: `267-[NF]-Lab`

## 🎯 Network Objective
This lab focused on the end-to-end architectural deployment of a production-ready web infrastructure. The objective was to build a custom VPC from the ground up, ensuring high availability through multi-AZ distribution and securing public-facing resources with granular security controls.



## 🚦 Traffic & Flow Logic
* **Network Isolation:** Architected a segmented VPC with Public and Private subnets across multiple Availability Zones. Used an Internet Gateway (IGW) for public edge routing and NAT Gateways for secure, outbound-only connectivity for the private tier.
* **Traffic Security:** Implemented "Defense in Depth" by combining stateful **Security Groups** (permitting HTTP/80 traffic at the instance level) with stateless **Network ACLs** to harden the subnet perimeter.

## 📷 Lab Evidence
| Task | Connectivity Check | Evidence |
| :--- | :--- | :--- |
| **1** | Multi-AZ VPC & Subnet Provisioning | ![VPC_Build](./images/267_VPC_Infrastructure.png) |
| **2** | Web Server Deployment (User Data) | ![Web_Deploy](./images/267_Web_Server_Running.png) |
| **3** | Secure HTTP Access Verification | ![HTTP_Test](./images/267_Public_Access.png) |

## 🛠️ Troubleshooting (The "Ping" Mindset)
* **Connectivity Roadblock:** The web server instance launched successfully, but the Apache test page failed to load when accessing the public DNS.
* **Diagnostic Steps:** 1. Validated the Security Group ingress rule for TCP Port 80.
    2. Inspected the Route Table to ensure the `0.0.0.0/0` route was pointed to the IGW.
    3. Confirmed the instance had an associated Public IP address.
* **"What If" Scenario:** In a high-traffic production environment, I would decouple the static web content by utilizing Amazon S3 with CloudFront, and place the compute layer (EC2) behind an Application Load Balancer (ALB) within an Auto Scaling Group to ensure elastic performance.

## 📊 Technical Competence
* **Skills:** VPC Infrastructure as Code (Wizard-based), Subnet/Route Table Association, Security Group Orchestration, Apache Web Server Automation (User Data), Multi-AZ/High Availability Design.
