# ◈ IAM Foundations
**Course ID**: `279-[SF]-Lab`

## 🎯 Project Goals
Establishing identity-based access controls and enforcing the principle of least privilege across an enterprise AWS environment to secure resource access and mitigate unauthorized operational actions.

## ⚙️ Technical Implementation
* **Identity Management:** Analyzed pre-created IAM users (`user-1`, `user-2`, `user-3`) and IAM user groups (`S3-Support`, `EC2-Support`, `EC2-Admin`) to evaluate existing permission structures.
* **Access Control:** Assigned users to designated functional groups based on role requirements, implementing strict segregation of duties for storage and compute management.
* **Policy Validation:** Authenticated as individual IAM users via the AWS account sign-in URL to perform multi-persona testing and verify granular permission boundaries across S3 and EC2 services.

## 🛠️ Operational Intelligence (Troubleshooting)
* **Real-World Challenge:** Attempted to execute an EC2 instance termination while authenticated under the `EC2-Support` role, which returned an explicit `Access Denied` authorization error.
* **Engineering Resolution:** Identified that the attached policy for `EC2-Support` grants read-only visibility to compute resources without write or lifecycle execution rights; validated that administrative rights were restricted strictly to members of the `EC2-Admin` group.
* **"What If" Scenario:** In a production setting, I would implement **AWS IAM Roles with Service Control Policies (SCPs)** via AWS Organizations and mandate **Multi-Factor Authentication (MFA)**, ensuring temporary security credentials replace long-term user access and centralized guardrails prevent privilege escalation.

## 📸 Lab Evidence
| Step / Validation | Description | Artifact |
|---|---|---|
| Initial IAM State | Pre-created users setup | `01-iam-initial-users.png` |
| Group Memberships | Assigning users to functional groups | `02-iam-group-memberships.png` |
| Authorization Boundary | `user-1` EC2 Access Denied error | `03-user1-ec2-access-denied.png` |
| Read-Only Restriction | `user-2` EC2 Instance Stop error | `04-user2-ec2-stop-denied.png` |
| Elevated Execution | `user-3` EC2 Admin access verified | `05-user3-ec2-admin-access.png` |

## 📊 Technical Competence
* **Demonstrated Skills:** Identity & Access Management (IAM), Least Privilege Enforcement, Policy Validation, Multi-Factor Authentication/Persona Testing, and Governance.
