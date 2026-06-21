# ◈ Automated Deployment Troubleshooting
**Course ID**: `191-[JAWS]-Activity`

## 🎯 Architectural Objective
This activity focused on the "Debugging Lifecycle" of infrastructure-as-code (IaC). The objective was to move beyond successful provisioning by identifying, isolating, and remediating complex deployment failures, detecting configuration drift, and mastering the recovery of stack states in non-standard scenarios.



## ⚙️ Debugging & Resolution Logic
* **Fault Isolation:** Analyzed stack events via the AWS CLI and queried granular error logs (`cloud-init-output.log`) on the EC2 instances to pinpoint root causes. Identified a critical syntax error in the UserData script where a non-existent package (`http` instead of `httpd`) halted the deployment.
* **Drift Detection:** Executed drift detection to identify manual, "out-of-band" modifications made to Security Group rules, demonstrating the ability to verify infrastructure integrity against the source-of-truth CloudFormation template.
* **Lifecycle Reconciliation:** Solved failed deletion states caused by non-empty S3 buckets. Performed targeted resource cleanup to reconcile the stack state, ensuring that immutable storage policies were respected while enabling environment teardown.

## 📷 Lab Evidence
| Task | Debugging Milestone | Evidence |
| :--- | :--- | :--- |
| **1** | Deployment Failure & Event Analysis | ![Fail_Log](./images/191_CF_Error_Log.png) |
| **2** | Template Refactoring (Userdata Fix) | ![Fix_Code](./images/191_CF_Fix.png) |
| **3** | Drift Analysis & Reconciliation | ![Drift_Detect](./images/191_CF_Drift.png) |

## 🛠️ Operational Intelligence
* **Challenge:** The stack entered a `DELETE_FAILED` state because an S3 bucket containing objects could not be removed, creating an "orphaned" resource environment.
* **Engineering Resolution:** Recognized that AWS CloudFormation prevents the deletion of non-empty buckets as a data-safety feature. Managed the lifecycle by manually clearing the S3 bucket contents and subsequently re-triggering the `delete-stack` command to achieve a clean environment tear-down.
* **"What If" Scenario:** In a production system, I would implement **Delete Policy** management (e.g., `DeletionPolicy: Retain` or `Delete`) within the template to explicitly handle bucket cleanup, or use S3 Lifecycle Rules to automatically expire objects, preventing manual intervention during automated environment decommissioning.

## 📊 Technical Competence
* **Demonstrated Skills:** IaC Troubleshooting (CLI/CloudWatch), JMESPath Querying (for CLI filtering), Drift Detection, Stack Lifecycle Management, UserData Script Debugging.
