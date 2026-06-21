# ◈ Network and System Hardening
**Course ID**: `276/277-[SF]-Lab`

## 🎯 Security Objective
This lab emphasizes the "Defense-in-Depth" strategy. The objective is to mitigate system vulnerabilities by implementing security layers at both the network perimeter and the OS level to prevent unauthorized access and exposure.

## 🛡️ Governance & Access Logic
* **Network Hardening:** [E.g., "Implemented restrictive Security Group rules and NACLs to permit only necessary traffic, effectively neutralizing external reconnaissance attempts."]
* **System Hardening:** [E.g., "Secured the OS environment by disabling unnecessary services, implementing SSH key-based authentication, and updating critical system packages to patch known CVEs."]

## 📷 Lab Evidence
| Task | Security Audit | Evidence |
| :--- | :--- | :--- |
| **1** | Network Perimeter Security (SG/NACL) | ![Network_Sec](./images/276_277_Network_Hardening.png) |
| **2** | OS Security & SSH Configuration | ![System_Sec](./images/276_277_OS_Hardening.png) |
| **3** | Vulnerability Scan/Status Report | ![Vuln_Scan](./images/276_277_Scan_Results.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Strict hardening policies inadvertently blocked necessary communication between the web and database tiers."]
* **Engineering Resolution:** [How you fixed it: e.g., "Diagnosed the failure using VPC Flow Logs, identified the blocked port, and adjusted Security Group egress/ingress rules to permit internal traffic while maintaining external restriction."]
* **"What If" Scenario:** [In a production environment, I would deploy AWS Config rules to automatically monitor and revert any unauthorized changes to Security Group configurations.]

## 📊 Technical Competence
* **Demonstrated Skills:** Network Hardening (SG/NACL), OS Vulnerability Mitigation, SSH Key Management, Defense-in-Depth Principles, Security Logging & Monitoring.
