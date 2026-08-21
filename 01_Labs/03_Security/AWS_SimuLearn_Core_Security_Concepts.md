# 🔒 AWS SimuLearn: Core Security Concepts

## 🎯 Objective
Implement the Principle of Least Privilege across enterprise IAM identities by configuring job-function user groups, enforcing read-only service policies, and auditing restricted resource access controls.

---

## 🏗️ Architecture & Configuration
* **Identity & Access Management (IAM):**
  * **User Group:** `SupportEngineers`
  * **Managed Policies:** `AmazonEC2ReadOnlyAccess`, `AmazonRDSReadOnlyAccess`
  * **Identities:** `support-engineer-1`
* **Access Control Enforcement:** 
  * Explicit denial of mutating API calls (`ec2:TerminateInstances`)
  * Role-based access control (RBAC) scoping for infrastructure support personnel

---

## 🛠️ Key Implementation Steps
1. **User Group Setup:** Created the `SupportEngineers` IAM user group to establish centralized authorization boundaries for database and compute operations.
2. **Managed Policy Attachment:** 
   * Practice Task: Attached `AmazonEC2ReadOnlyAccess` to grant visibility over EC2 computing instances without administrative write permissions.
   * DIY Challenge Task: Extended authorization by attaching `AmazonRDSReadOnlyAccess` to grant read-only visibility into relational database cluster states.
3. **Identity Provisioning & Tagging:** Created IAM user `support-engineer-1` with custom login credentials and applied ABAC tags (`job-title: Support Engineer`).
4. **Least Privilege Verification:** Logged in as `support-engineer-1` via a secondary browser session to test permission boundaries—verifying successful read operations on running web instances and confirming explicit authorization failures when attempting instance termination.

---

## 💡 Key Architectural Takeaway
Securing cloud environments relies on assigning permissions based on job roles rather than individual users. By managing authorization at the user group level and attaching AWS-managed least-privilege policies (`*ReadOnlyAccess`), operational teams maintain full visibility needed for troubleshooting while preventing accidental or malicious resource modification.

---

## 📜 Certification & Verification

<p align="center">
  <a href="https://github.com/arabbika/my-aws-journey/blob/main/Certifications/Core%20Security%20Concepts.png" target="_blank">
    <img src="https://raw.githubusercontent.com/arabbika/my-aws-journey/main/Certifications/Core%20Security%20Concepts.png" alt="AWS SimuLearn - Core Security Concepts Badge" width="350" />
  </a>
</p>
