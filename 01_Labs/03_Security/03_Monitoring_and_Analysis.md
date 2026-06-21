# ◈ Security Monitoring and Data Analysis
**Course ID**: `280/281-[SF]-Lab`

## 🎯 Security Objective
This lab focuses on establishing persistent visibility across the cloud environment. The objective is to leverage AWS monitoring tools to detect security anomalies, analyze access logs, and respond effectively to potential malware or unauthorized activity.

## 🛡️ Governance & Access Logic
* **Detection & Logging:** [E.g., "Enabled CloudTrail to track all API activity and configured CloudWatch alarms to notify of unauthorized attempts or suspicious patterns."]
* **Analysis & Response:** [E.g., "Utilized monitoring dashboards to analyze resource metrics and security logs, enabling rapid identification and isolation of security events."]

## 📷 Lab Evidence
| Task | Diagnostic Output | Evidence |
| :--- | :--- | :--- |
| **1** | CloudTrail API Event Tracking | ![Trail_Log](./images/280_281_CloudTrail.png) |
| **2** | CloudWatch Alarm/Metric Config | ![Alarm_Config](./images/280_281_CloudWatch.png) |
| **3** | Security Event Log Analysis | ![Log_Audit](./images/280_281_Event_Analysis.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Received an excessive number of 'False Positive' alerts from CloudWatch, obscuring genuine security threats."]
* **Engineering Resolution:** [How you fixed it: e.g., "Refined alarm thresholds and implemented metric filters to focus on high-fidelity security events (e.g., failed console logins or root account usage)."]
* **"What If" Scenario:** [In a production environment, I would integrate these logs with Amazon GuardDuty for automated, intelligent threat detection and use Lambda to trigger automatic remediation of security misconfigurations.]

## 📊 Technical Competence
* **Demonstrated Skills:** CloudTrail Governance, CloudWatch Monitoring & Alerting, Log Analysis, Security Event Response, Proactive Threat Detection.
