# ◈ Identity and Access Management (IAM) Basics
**Course ID**: `279-[SF]-Lab`

## 🎯 Security Objective
This lab focused on the implementation of the Principle of Least Privilege. The objective was to design and configure granular IAM policies that restrict user and service account access to only the resources necessary for their specific roles, minimizing the attack surface and ensuring clear separation of duties.



## 🛡️ Governance & Access Logic
* **Policy Design:** Analyzed Managed Policies (`AmazonEC2ReadOnlyAccess`, `AmazonS3ReadOnlyAccess`) versus custom Inline Policies to fulfill specific operational requirements.
* **Identity Control:** Organized identities into functional groups (`EC2-Admin`, `EC2-Support`, `S3-Support`) to streamline permissions management and improve scalability.
* **Governance:** Configured account-wide security posture by enforcing a custom Password Policy (10-character minimum, rotation/reuse constraints).

## 📷 Lab Evidence
| Task | Security Audit | Evidence |
| :--- | :--- | :--- |
| **1** | IAM Password Policy Configuration | ![IAM_Policy](./images/279_Password_Policy.png) |
| **2** | Group Policy Attachment Audit | ![Policy_Attach](./images/279_Policy_Attach.png) |
| **3** | RBAC Access Verification (User 1-3) | ![Access_Test](./images/279_Access_Verification.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Encountered 'Access Denied' errors during permission testing.
* **Diagnostic Steps:** Utilized cross-account sign-in testing to validate that the assigned Group policies strictly adhered to the requirements—verifying that `user-2` could describe EC2 instances but was correctly denied the `StopInstances` action.
* **Engineering Resolution:** Confirmed that the `EC2-Admin` inline policy provided the necessary elevated privileges, while support users were successfully restricted by their respective Read-Only managed policies.
* **Security Best Practice:** This lab reinforces that administrative tasks should always be performed by identities with the minimum scope of authority, preventing accidental or malicious infrastructure disruption.

## 📊 Technical Competence
* **Demonstrated Skills:** IAM Policy Creation (JSON), Principle of Least Privilege (PoLP), Role-Based Access Control (RBAC), Account Security Hardening, Identity-based Permission Testing.
