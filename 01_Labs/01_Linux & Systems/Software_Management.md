# ◈ Software Management
**Course ID**: `243-[LX]-Lab`

## 🎯 System Objective
This lab focused on software lifecycle management and cloud authentication. The objective was to maintain system integrity through secure package management, demonstrate incident recovery via rollback procedures, and establish secure programmatic access to AWS services via the AWS Command Line Interface (CLI).

## ⚙️ Execution & Scripting
* **Package Lifecycle:** Utilized `yum` to query, update, and upgrade system packages, ensuring the instance remained patched against vulnerabilities.
* **Incident Recovery:** Mastered the `yum` transaction history to identify and revert problematic package installations, ensuring system stability during software changes.
* **Cloud Authentication:** Installed and configured the AWS CLI, establishing secure, credential-based communication between the local Linux environment and AWS service APIs.

## 📷 Lab Evidence
| Task | CLI Output | Evidence |
| :--- | :--- | :--- |
| **1** | System Update Status | ![Update_Status](./images/243_Upgrade_Result.png) |
| **2** | Transaction History Audit | ![History_List](./images/243_History_List.png) |
| **3** | Successful CLI Verification | ![CLI_Verify](./images/243_CLI_Help.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Managing dependency conflicts during software rollbacks and ensuring that the AWS CLI was configured with the correct security tokens to interact with AWS resources.
* **Engineering Resolution:** Leveraged `sudo yum history undo <#>` to perform a safe rollback of packages, and manually configured the `~/.aws/credentials` file to securely inject session tokens required for API interaction.
* **Efficiency Gains:** Mastery of `yum` history allows for rapid system recovery, while proper CLI configuration enables efficient, programmatic management of cloud infrastructure, reducing reliance on the web-based console.

## 📊 Technical Competence
* **Demonstrated Skills:** Linux Package Management (YUM), Transaction History/Rollback, AWS CLI Installation, Cloud Identity/Credential Configuration, API Interaction.
