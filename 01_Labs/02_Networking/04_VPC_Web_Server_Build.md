# ◈ Secure VPC Web Server Deployment
**Course ID**: `267-[NF]-Lab`

## 🎯 Network Objective
This lab demonstrates the architectural deployment of a production-ready web server. The objective is to build a custom VPC from the ground up, ensuring public-facing components are appropriately gated by security controls and network routing.

## 🚦 Traffic & Flow Logic
* **Network Isolation:** [Describe your approach, e.g., "Deployed web servers in a public subnet with an Internet Gateway, while keeping data-tier components in a private subnet."]
* **Traffic Security:** [E.g., "Enforced security via layered defense: Security Groups for instance-level stateful filtering and Network ACLs for subnet-level stateless hardening."]

## 📷 Lab Evidence
| Task | Connectivity Check | Evidence |
| :--- | :--- | :--- |
| **1** | VPC Infrastructure Build | ![VPC_Build](./images/267_VPC_Infrastructure.png) |
| **2** | Web Server Deployment (User Data) | ![Web_Deploy](./images/267_Web_Server_Running.png) |
| **3** | Secure HTTP Access Verification | ![HTTP_Test](./images/267_Public_Access.png) |

## 🛠️ Troubleshooting (The "Ping" Mindset)
* **Connectivity Roadblock:** [E.g., "Instance launched successfully, but the web page was unreachable from the public internet."]
* **Diagnostic Steps:** [E.g., "Verified the IGW route was correctly attached to the public subnet's Route Table; confirmed the Security Group allowed inbound traffic on port 80."]
* **"What If" Scenario:** [In a production environment, I would replace the single instance with an Auto Scaling Group behind an Application Load Balancer (ALB) to handle traffic spikes and health checks.]

## 📊 Technical Competence
* **Skills:** VPC Construction, Security Group Orchestration, User Data Automation, HTTP/Traffic Management, Production Architecture Design.
