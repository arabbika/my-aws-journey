# ◈ EC2 Infrastructure Challenge
**Course ID**: `172-[JAWS]-Lab`

## 🎯 Architectural Objective
To design and deploy a secure, web-enabled compute architecture. The objective was to build a complete environment from the ground up, including custom VPC networking, internet connectivity, and automated software deployment via EC2 user data.

## ⚙️ Technical Approach
* **Compute Strategy:** Provisioned an Amazon Linux 2023 `t3.micro` instance. Utilized **User Data** scripts to automate the installation of the `httpd` (Apache) web server and configure directory permissions for web content deployment.
* **Network Configuration:** Designed a custom VPC from scratch, including a VPC, Subnet, and Internet Gateway. Configured custom Route Tables to ensure the subnet had a valid route to the internet, allowing public access.
* **Security Implementation:** Configured Security Groups to permit `SSH` (port 22) for management and `HTTP` (port 80) for web traffic.

## 📷 Lab Evidence
| Task | Description | Evidence |
| :--- | :--- | :--- |
| **1** | VPC & Network Route Configuration | ![Network_Design](./images/172_VPC_Setup.png) |
| **2** | System Log (httpd Installation) | ![Sys_Logs](./images/172_httpd_Logs.png) |
| **3** | Successful Web Page Delivery | ![Web_Display](./images/172_Web_Result.png) |

## 🛠️ Operational Intelligence
* **Real-World Challenge:** The web server was unreachable via browser even though the instance was running and the security group allowed port 80.
* **Engineering Resolution:** Identified that the subnet route table lacked a route to the Internet Gateway. Added the `0.0.0.0/0` route to the IGW, which restored external access to the web server.
* **"What If" Scenario:** If this were a production system, I would use an **Application Load Balancer (ALB)** and an **Auto Scaling Group**. This would eliminate the single point of failure (a single EC2 instance) and provide automatic health checking and traffic distribution.

## 📊 Technical Competence
* **Demonstrated Skills:** Custom VPC Networking, EC2 Lifecycle Management, User Data Automation, HTTP/Apache Web Server Management, Network Troubleshooting.
