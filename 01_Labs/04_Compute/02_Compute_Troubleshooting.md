# ◈ Troubleshooting EC2 Instances
**Course ID**: `173-[JAWS]-Activity`

## 🎯 Architectural Objective
Diagnose and resolve common configuration failures during the automated provisioning of Amazon EC2 instances, ensuring correct service initialization and operational readiness.

## ⚙️ Technical Implementation
* **Diagnostic Analysis:** Analyzed system logs, including `/var/log/cloud-init-output.log`, to pinpoint specific failure points during the instance initialization phase.
* **Remediation:** Corrected user data scripts and configuration parameters, ensuring essential services (e.g., Apache, MariaDB) successfully initialize upon launch.
* **Service Validation:** Verified process status and end-to-end connectivity following the troubleshooting and configuration remediation.

## 📷 Lab Evidence
| Task | Description | Evidence |
| :--- | :--- | :--- |
| **1** | Deployment Error Analysis | ![Log_Analysis](./images/173_Troubleshoot_Logs.png) |
| **2** | User Data Script Correction | ![Script_Fix](./images/173_Script_Fix.png) |
| **3** | Service Verification | ![Service_Check](./images/173_Success.png) |

## 🛠️ Operational Intelligence
* **Real-World Challenge:** Instances failed to initialize required web services despite successfully reaching the `running` state.
* **Engineering Resolution:** Investigated the logs to find script execution errors; identified syntax errors in the bash initialization commands, corrected them, and re-triggered the instance launch to restore functionality.
* **"What If" Scenario:** In a production system, I would implement `cfn-init` and `cfn-signal` with Auto Scaling groups to ensure instances only join the load balancer if the software configuration is 100% successful, preventing "zombie" instances from serving traffic.

## 📊 Technical Competence
* **Demonstrated Skills:** Cloud-init Log Analysis, Linux Service Management, User Data Debugging, Automated Provisioning Troubleshooting.
