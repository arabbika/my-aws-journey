# ◈ AWS Systems Manager Administration
**Course ID**: `169-[JAWS]-Lab`

## 🎯 Operational Objective
This lab focuses on operational excellence through centralized management. The objective is to utilize AWS Systems Manager (SSM) to gain visibility and control over infrastructure, moving away from manual SSH access toward secure, automated resource management and patch compliance.



## ⚙️ Execution & Management Logic
* **Centralized Control:** [E.g., "Configured SSM Agent on EC2 instances to enable remote management, eliminating the need for open inbound SSH ports."]
* **Operational Automation:** [E.g., "Deployed SSM Run Command and State Manager to automate configuration drifts, ensuring all instances adhere to a consistent security and software baseline."]

## 📷 Lab Evidence
| Task | Management Output | Evidence |
| :--- | :--- | :--- |
| **1** | Instance Registration & SSM Agent Status | ![SSM_Agent](./images/169_SSM_Register.png) |
| **2** | Run Command Execution (Automation) | ![Run_Command](./images/169_Run_Command.png) |
| **3** | Patch Compliance & Inventory Report | ![Patch_Audit](./images/169_SSM_Patch.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Instances were not appearing in the 'Managed Instances' console, preventing automated patching tasks."]
* **Engineering Resolution:** [How you fixed it: e.g., "Verified that the IAM instance profile lacked the `AmazonSSMManagedInstanceCore` policy; updated the profile, restarted the SSM Agent, and confirmed communication with the SSM service."]
* **"What If" Scenario:** [In a production system, I would use SSM Maintenance Windows to schedule non-disruptive patching across the entire fleet and use Parameter Store to securely inject configuration data into applications at runtime.]

## 📊 Technical Competence
* **Demonstrated Skills:** Fleet Management (SSM), Infrastructure-as-Code (SSM Documents), Automated Patch Compliance, Secure Remote Access (Session Manager).
