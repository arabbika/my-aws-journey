# ◈ Identity and Access Management (IAM) Basics
**Course ID**: `279-[SF]-Lab`

## 🎯 Security Objective
This lab focuses on the implementation of the Principle of Least Privilege. The objective is to design and configure granular IAM policies that restrict user and service account access to only the resources necessary for their specific roles, minimizing the attack surface.

## 🛡️ Governance & Access Logic
* **Policy Design:** [E.g., "Constructed custom JSON IAM policies to provide fine-grained, conditional access to specific S3 buckets."]
* **Identity Control:** [E.g., "Created IAM Users and Groups, mapping policies to roles to ensure clear separation of duties within the AWS environment."]

## 📷 Lab Evidence
| Task | Security Audit | Evidence |
| :--- | :--- | :--- |
| **1** | IAM User/Group Creation | ![IAM_Identity](./images/279_IAM_Users.png) |
| **2** | Policy Application & Attachment | ![Policy_Attach](./images/279_Policy_Attach.png) |
| **3** | Access Denied/Granted Verification | ![Access_Test](./images/279_Policy_Test.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Encountered 'Access Denied' errors even after assigning administrative policies due to conflicting SCPs or existing permission boundaries."]
* **Engineering Resolution:** [How you fixed it: e.g., "Utilized the IAM Policy Simulator to identify the specific rule causing the conflict and refined the policy JSON for proper evaluation."]
* **Efficiency Gains:** [Why is this approach better? e.g., "Regular IAM audits and simulator testing prevent unauthorized privilege escalation and ensure compliance with security best practices."]

## 📊 Technical Competence
* **Demonstrated Skills:** IAM Policy Creation (JSON), Principle of Least Privilege, Role-Based Access Control (RBAC), Policy Simulator Troubleshooting.
