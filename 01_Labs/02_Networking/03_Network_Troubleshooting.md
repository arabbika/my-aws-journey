# ◈ Network Troubleshooting and Diagnostics
**Course ID**: `265/266-[NF]-Lab`

## 🎯 Network Objective
This lab focuses on the analytical process of identifying and resolving network failures. The objective is to demonstrate proficiency in tracing packet flow and interpreting route tables to fix complex connectivity issues.

## 🚦 Traffic & Flow Logic
* **Diagnostic Methodology:** [Describe your process, e.g., "Adopted a bottom-up approach: verifying physical/layer 3 connectivity, then inspecting security group/NACL rules."]
* **Traffic Analysis:** [E.g., "Utilized CLI diagnostic tools to map the path between the source instance and target destination, isolating the point of failure."]

## 📷 Lab Evidence
| Task | Diagnostic Output | Evidence |
| :--- | :--- | :--- |
| **1** | Connectivity Tracing (CLI) | ![Trace_Result](./images/265_266_Traceroute.png) |
| **2** | Route Table Analysis | ![Route_Table](./images/265_266_Route_Analysis.png) |
| **3** | Security Policy Validation | ![Policy_Audit](./images/265_266_Security_Audit.png) |

## 🛠️ Troubleshooting (The "Ping" Mindset)
* **Connectivity Roadblock:** [E.g., "Instance unreachable via SSH despite correctly configured Security Groups."]
* **Diagnostic Steps:** [E.g., "Performed a path analysis to discover a misconfigured entry in the subnet's Route Table; corrected the gateway destination."]
* **"What If" Scenario:** [If this were a production system, how would you automate or optimize this differently?]
* **Engineering Resolution:** [Proactively implemented VPC Reachability Analyzer to detect similar configuration drifts in the future.]

## 📊 Technical Competence
* **Skills:** Network Diagnostic CLI (Traceroute, Ping, MTR), Route Table Analysis, VPC Flow Log interpretation, Connectivity Troubleshooting.
