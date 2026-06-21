# ◈ EC2 Infrastructure Challenge
**Course ID**: `172-[JAWS]-Lab`

## 🎯 Architectural Objective
To design and deploy a secure, web-enabled compute architecture from the ground up. The objective was to synthesize custom VPC networking, internet edge routing, and automated server provisioning into a functional production-ready environment.



## ⚙️ Technical Approach
* **Compute Strategy:** Provisioned an Amazon Linux 2023 `t3.micro` instance. Utilized **User Data** scripts to automate the `httpd` (Apache) installation and applied `chmod` permissions to the `/var/www/html` directory, enabling secure content deployment.
* **Network Configuration:** Architected a custom VPC, including Subnet creation and an Internet Gateway (IGW). Configured Route Tables to bridge the subnet to the IGW, establishing the necessary public egress/ingress path.
* **Security Implementation:** Orchestrated Security Group rules to enforce principle-of-least-privilege access, explicitly permitting `SSH` (TCP 22) for administration and `HTTP` (TCP 80) for public traffic.

## 📷 Lab Evidence
| Task | Description | Evidence |
| :--- | :--- | :--- |
| **1** | VPC & Network Route Configuration | ![Network_Design](./images/172_VPC_Setup.png) |
| **2** | System Log (httpd Installation) | ![Sys_Logs](./images/172_httpd_Logs.png) |
| **3** | Successful Web Page Delivery | ![Web_Display](./images/172_Web_Result.png) |

## 🛠️ Operational Intelligence
* **Real-World Challenge:** Despite the instance status showing "Running" and the Security Group allowing inbound traffic on port 80, the web server remained unreachable from the public internet.
* **Engineering Resolution:** Diagnosed the subnet’s Route Table and identified the absence of a route to the Internet Gateway. Updating the destination `0.0.0.0/0` to point toward the IGW successfully resolved the connectivity block.
* **"What If" Scenario:** In a high-availability production environment, I would replace the single instance with an **Auto Scaling Group** distributed across multiple Availability Zones, placed behind an **Application Load Balancer (ALB)** to provide automated health checking, failover, and efficient traffic management.

## 📊 Technical Competence
* **Demonstrated Skills:** Custom VPC/Subnet Provisioning, Internet Gateway/Route Table Orchestration, EC2 Instance Lifecycle Management, User Data Automation, HTTP/Apache Web Server Management, Network/Connectivity Troubleshooting.
