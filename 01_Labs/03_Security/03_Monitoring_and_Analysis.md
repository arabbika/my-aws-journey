# ◈ Security Monitoring and Data Analysis
**Course ID**: `280/281-[SF]-Lab`

## 🎯 Security Objective
This lab focused on establishing persistent visibility across the cloud environment. The objective was to leverage AWS monitoring and observability tools to detect security anomalies, analyze access logs, and respond effectively to potential malware or unauthorized resource activity.



## 🛡️ Governance & Access Logic
* **Detection & Logging:** Configured **CloudTrail** for centralized API auditing, creating an immutable record of all management plane activities. 
* **Monitoring & Alerting:** Designed **CloudWatch Alarms** to monitor instance health metrics (CPU utilization) and integrated them with **Amazon SNS** to ensure real-time delivery of critical security notifications.
* **Perimeter Security:** Implemented **AWS Network Firewall** with stateful **Suricata** rule groups to perform deep packet inspection (DPI) and block egress traffic to identified malicious C2 (Command & Control) servers.

## 📷 Lab Evidence
| Task | Diagnostic Output | Evidence |
| :--- | :--- | :--- |
| **1** | Malware Access Blocking (Network Firewall) | ![Firewall_Test](./images/280_281_Firewall_Block.png) |
| **2** | CloudWatch Metric/Alarm Configuration | ![Alarm_Config](./images/280_281_CloudWatch.png) |
| **3** | CPU Stress Test & Security Alerting | ![Alert_Log](./images/280_281_Alert_Output.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Distinguishing between legitimate high-performance computing tasks and malicious activities (like crypto-mining malware) that cause CPU spikes.
* **Engineering Resolution:** Created a **CloudWatch Dashboard** to aggregate metrics for rapid visualization and established a 60% CPU utilization threshold alarm to provide early warning of potential compromise.
* **"What If" Scenario:** In a production environment, I would configure **Amazon GuardDuty** for intelligent, AI-driven threat detection and use **AWS Lambda** to automatically isolate an EC2 instance into a "sandbox" Security Group the moment a critical CloudWatch alert is triggered.

## 📊 Technical Competence
* **Demonstrated Skills:** Network Firewall Policy Management (Suricata/Stateful Rules), CloudWatch Observability (Dashboards/Alarms), SNS Pub/Sub Messaging, CloudTrail Governance, Log Analysis, Security Event Response.
