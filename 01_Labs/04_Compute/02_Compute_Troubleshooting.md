# ◈ Troubleshooting EC2 Instance Provisioning
**Course ID**: `173-[JAWS]-Activity`

## 🎯 Architectural Objective
This activity centers on the automated deployment of a LAMP stack (Linux, Apache, MySQL, PHP) via AWS CLI and shell scripts. The objective is to apply diagnostic methodologies—using logs and network scanning tools—to identify and remediate configuration failures in automated infrastructure.



## ⚙️ Execution & Debugging Logic
* **Automated Deployment:** Executed CLI-based `run-instances` commands to provision EC2 instances, leveraging user data for automated application stack configuration.
* **Diagnostic Workflow:** Utilized `nmap` for port verification and `cloud-init` logs (`/var/log/cloud-init-output.log`) to debug service failures and verify the successful deployment of the Café Web Application.

## 📷 Lab Evidence
| Task | Debugging Milestone | Evidence |
| :--- | :--- | :--- |
| **1** | AWS CLI Troubleshooting & Fix | ![CLI_Fix](./images/173_CLI_Debug.png) |
| **2** | Network Scanning (nmap) Results | ![Nmap_Scan](./images/173_Nmap_Results.png) |
| **3** | Successful LAMP Stack Validation | ![Web_Validation](./images/173_Cafe_App.png) |

## 🛠️ Operational Intelligence
* **Real-World Challenge:** Encountered `InvalidAMIID.NotFound` errors during initial script execution and subsequent connectivity issues where port 80 was closed despite the service being installed.
* **Engineering Resolution:** 1. **AMI Issue:** Updated the shell script to reference the correct AMI ID compatible with the lab's current region.
    2. **Connectivity Issue:** Used `nmap` to confirm TCP port 80 was unreachable. Investigated Security Group ingress rules, corrected the port mapping, and verified service status using `systemctl status httpd`.
* **"What If" Scenario:** If this were a production system, I would use **AWS CloudFormation or Terraform** to manage the infrastructure state declaratively, which prevents the manual "configuration drift" often associated with shell-script-based deployments.

## 📊 Technical Competence
* **Demonstrated Skills:** AWS CLI Administration, Linux System Administration (LAMP stack), Network Troubleshooting (`nmap`), Log-based Diagnostic Analysis (`cloud-init`), Security Group Remediation.
