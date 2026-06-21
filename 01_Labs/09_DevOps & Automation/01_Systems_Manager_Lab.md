# ◈ AWS Systems Manager Administration
**Course ID**: `169-[JAWS]-Lab`

## 🎯 Operational Objective
This lab focused on achieving operational excellence through centralized management. The objective was to replace insecure, manual SSH-based administration with automated, secure, and auditable AWS Systems Manager (SSM) workflows, ensuring fleet-wide compliance and consistent configuration.



## ⚙️ Execution & Management Logic
* **Centralized Fleet Control:** Leveraged **Fleet Manager** to establish inventory associations, gaining real-time visibility into software configurations and metadata across the instance fleet without manual connectivity.
* **Operational Automation:** Utilized **SSM Run Command** to deploy a multi-component dashboard application (Apache, PHP, SDKs) in a single, repeatable execution, proving the ability to perform complex fleet-wide software orchestration.
* **Dynamic Configuration:** Implemented **Parameter Store** to manage application "dark features," enabling real-time toggling of beta functionalities via external configuration values rather than code deployments.
* **Secure Remote Access:** Replaced traditional bastion hosts and SSH keys with **Session Manager**, providing an interactive, browser-based shell access that is fully compliant with modern security and auditing policies.

## 📷 Lab Evidence
| Task | Management Output | Evidence |
| :--- | :--- | :--- |
| **1** | Instance Inventory & Fleet Registration | ![SSM_Agent](./images/169_SSM_Register.png) |
| **2** | Run Command App Deployment | ![Run_Command](./images/169_Run_Command.png) |
| **3** | Parameter Store Feature Toggle | ![Param_Store](./images/169_SSM_Param.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Instances were not appearing in the 'Managed Instances' console, which prevented the execution of any automated tasks.
* **Engineering Resolution:** Diagnosed the issue by verifying the IAM Instance Profile; discovered that the instance lacked the `AmazonSSMManagedInstanceCore` policy. Updated the role, confirmed the SSM Agent service was active, and re-registered the instance, successfully restoring communication with the Systems Manager service.
* **"What If" Scenario:** In a large-scale production environment, I would utilize **SSM Maintenance Windows** to schedule non-disruptive, phased patching across the fleet to maintain high availability. Furthermore, I would integrate **CloudTrail** with all SSM actions to provide a complete audit log of every command executed across the infrastructure.

## 📊 Technical Competence
* **Demonstrated Skills:** Fleet Management (Inventory/Fleet Manager), Configuration Automation (Run Command), Secure Parameter/Secret Management, Auditable Remote Access (Session Manager), VPC/Security Troubleshooting.
