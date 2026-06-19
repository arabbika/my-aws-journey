# ◈ EC2 Foundations and Provisioning
**Course ID**: `11-[CF]-Lab`

## 🎯 Architectural Objective
Designing a fundamental compute environment to host a scalable web application. The goal was to master instance lifecycle management while implementing secure network boundaries to protect workload integrity.

## ⚙️ Technical Implementation
* **Compute:** Provisioned a `t2.micro` Linux-based instance using the Amazon Linux 2 AMI, chosen for its compatibility and low-resource overhead.
* **Network:** Deployed the instance within a VPC subnet, ensuring proper isolation from the default public environment.
* **Security:** Configured a granular Security Group (SG) architecture. Implemented the "Principle of Least Privilege" by restricting inbound SSH (port 22) traffic exclusively to my local machine's CIDR block.

## 🛠️ Operational Intelligence (Troubleshooting)
* **Real-World Challenge:** Encountered a "Connection Timeout" error during the initial SSH attempt.
* **Engineering Resolution:** Diagnosed the issue by auditing the VPC Route Table and Security Group ingress rules. Identified that the default SG ingress allowed `0.0.0.0/0` (too permissive) but the instance lacked an Internet Gateway route, or had conflicting NACL rules. Corrected the SG and verified local IP routing to establish a stable connection.
* **"What If" Scenario:** If this were a production-grade workload, I would have integrated **AWS Systems Manager (SSM) Session Manager** instead of SSH to eliminate the need for open inbound ports (port 22), further reducing the attack surface.

## 📊 Technical Competence
* **Demonstrated Skills:** Infrastructure Hardening, Network Segmentation, and Cloud Resource Troubleshooting.
