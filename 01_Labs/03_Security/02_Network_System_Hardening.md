# ◈ Network and System Hardening
**Course ID**: `276/277-[SF]-Lab`

## 🎯 Security Objective
This lab emphasized a "Defense-in-Depth" strategy. The objective was to mitigate system vulnerabilities by hardening the network perimeter and enforcing automated OS-level patch compliance, effectively neutralizing potential exploit vectors.



## 🛡️ Governance & Access Logic
* **Network Hardening:** Implemented restrictive Security Group (SG) rules and Network ACLs (NACLs) to enforce a "least privilege" traffic model, permitting only essential ingress/egress ports.
* **System Hardening:** Utilized **Amazon Inspector** for continuous vulnerability assessment (CVE scanning) and **AWS Systems Manager (SSM) Patch Manager** to enforce standardized patch baselines across Linux and Windows fleets, ensuring all instances meet security compliance requirements.

## 📷 Lab Evidence
| Task | Security Audit | Evidence |
| :--- | :--- | :--- |
| **1** | Automated Vulnerability Scanning (Inspector) | ![Vuln_Scan](./images/276_277_Scan_Results.png) |
| **2** | Patch Baseline & Group Configuration | ![Patch_Baseline](./images/276_277_Patch_Manager.png) |
| **3** | Compliance Status Verification | ![Compliance](./images/276_277_Compliance_Report.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Tightening security policies inadvertently caused a "false positive" vulnerability report in legacy application dependencies.
* **Diagnostic Steps:** 1. Analyzed Inspector findings to identify the specific `requests` package version CVE.
    2. Used Systems Manager to verify instance patch group membership and scan execution logs.
* **Engineering Resolution:** Updated `requirements.txt` to pull the latest patched package versions and triggered a re-scan via Inspector to confirm `Closed` finding status.
* **"What If" Scenario:** In a production environment, I would integrate these security scans into the CI/CD pipeline, failing deployments if high-severity CVEs are detected, and use AWS Config to remediate non-compliant Security Groups automatically.

## 📊 Technical Competence
* **Demonstrated Skills:** Vulnerability Assessment (Amazon Inspector), Patch Orchestration (SSM Patch Manager), Patch Baseline/Group Design, Compliance Auditing, CVE Remediation, Defense-in-Depth Principles.
