# ◈ Troubleshooting EC2 Instance Provisioning
**Course ID**: `173-[JAWS]-Activity`

## 🎯 Architectural Objective
This activity centered on the automated deployment of a LAMP stack (Linux, Apache, MySQL, PHP) via the AWS CLI. The objective was to apply professional diagnostic methodologies—leveraging CLI logging, network port scanning, and service state inspection—to remediate configuration failures in automated infrastructure.



## ⚙️ Execution & Debugging Logic
* **Automated Deployment:** Provisioned EC2 resources via `aws ec2 run-instances`, utilizing `user-data` scripts to bootstrap the application stack.
* **Diagnostic Workflow:** Adopted a systematic "Stack-Trace" methodology:
    1. **Provisioning:** Used CLI error messages to identify AMI/Region mismatches.
    2. **Network/Connectivity:** Used `nmap` to probe instance port availability and validate Security Group rules.
    3. **Service State:** Inspected `/var/log/cloud-init-output.log` to audit the application bootstrapping process and verify database/web service initialization.

## 📷 Lab Evidence
| Task | Debugging Milestone | Evidence |
| :--- | :--- | :--- |
| **1** | AWS CLI Troubleshooting & AMI Fix | ![CLI_Fix](./images/173_CLI_Debug.png) |
| **2** | Network Scanning (nmap) Analysis | ![Nmap_Scan](./images/173_Nmap_Results.png) |
| **3** | Café Web App LAMP Validation | ![Web_Validation](./images/173_Cafe_App.png) |

## 🛠️ Operational Intelligence
* **Real-World Challenge:** Encountered `InvalidAMIID.NotFound` errors and persistent connection timeouts on port 80 despite the instance showing a "running" status.
* **Engineering Resolution:** 1. **AMI Remediation:** Corrected the shell script’s AMI reference to ensure compatibility with the current AWS region.
    2. **Connectivity Fix:** Used `nmap -Pn` to identify that the web server port was closed; audited the Security Group and discovered a firewall misconfiguration, then verified the `httpd` service status via `systemctl` on the instance.
* **"What If" Scenario:** If deploying this for production, I would transition from shell-script bootstrapping to **Infrastructure as Code (IaC)** using Terraform or CloudFormation. This move to declarative management eliminates configuration drift and ensures that the infrastructure state is version-controlled and reproducible.

## 📊 Technical Competence
* **Demonstrated Skills:** AWS CLI Administration, Linux System Administration (LAMP stack), Network Troubleshooting (`nmap`), Log-based Diagnostic Analysis (`cloud-init`), Security Group/Firewall Remediation.
