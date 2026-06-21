# ◈ Network Troubleshooting and Diagnostics
**Course ID**: `265/266-[NF]-Lab`

## 🎯 Network Objective
This lab focused on the analytical process of identifying and resolving network failures. The objective was to demonstrate proficiency in tracing packet flow across the OSI model and interpreting security policies to remediate connectivity bottlenecks.



## 🚦 Traffic & Flow Logic
* **Diagnostic Methodology:** Adopted a structured, top-down and bottom-up hybrid approach: 
    1. **Reachability:** Verified Internet Gateway (IGW) and Route Table entries.
    2. **Security:** Audited Security Groups (stateful) and NACLs (stateless) for port/protocol restrictions.
    3. **Application:** Confirmed service state (`httpd`) and listener status.
* **Traffic Analysis:** Utilized standard Linux CLI tools (`ping`, `traceroute`, `netstat`, `curl`) to isolate the "hop" where traffic was dropped.

## 📷 Lab Evidence
| Task | Diagnostic Output | Evidence |
| :--- | :--- | :--- |
| **1** | Connectivity Tracing (Traceroute) | ![Trace_Result](./images/265_266_Traceroute.png) |
| **2** | Route Table & Policy Analysis | ![Route_Table](./images/265_266_Route_Analysis.png) |
| **3** | Security Policy/Service Audit | ![Policy_Audit](./images/265_266_Security_Audit.png) |

## 🛠️ Troubleshooting (The "Ping" Mindset)
* **Connectivity Roadblock:** Customer reported that an Apache web server was active, yet the site was unreachable via browser and unresponsive to `ping` requests.
* **Diagnostic Steps:** * Performed `netstat -tlp` to verify the Apache process was listening on the expected port.
    * Used `curl -v` to observe handshake failure at the application level.
    * Reviewed Security Group ingress rules, identifying a missing permit rule for TCP port 80.
* **Engineering Resolution:** Applied the necessary Ingress rule to the Security Group and validated the route back to the IGW, successfully restoring web traffic.

## 📊 Technical Competence
* **Skills:** Network Diagnostic CLI (Traceroute, Ping, MTR, Netstat, Telnet, Curl), OSI Model Troubleshooting, VPC Route Table Analysis, Security Group/NACL Policy Auditing.
