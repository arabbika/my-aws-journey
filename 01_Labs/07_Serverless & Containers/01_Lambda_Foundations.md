# ◈ AWS Lambda Event-Driven Foundations
**Course ID**: `178-[JAWS]-Activity`

## 🎯 Serverless Objective
This project demonstrates the transition from traditional server-based compute to a fully serverless, event-driven paradigm. The objective was to decouple business logic into modular Lambda functions, utilizing automated triggers (EventBridge) to execute analytical workflows on demand, thereby optimizing for operational efficiency and cost.



## ⚡ Execution & Logic Flow
* **Event Integration:** Architected a multi-stage event flow where Amazon EventBridge (formerly CloudWatch Events) triggers the `salesAnalysisReport` Lambda on a Cron-based schedule.
* **Logic Decoupling:** Implemented a two-tier function pattern: 
    * `salesAnalysisReportDataExtractor`: Handles secure database interactions (via Parameter Store) within a VPC.
    * `salesAnalysisReport`: Handles orchestration, report formatting, and downstream notification via SNS.
* **Dependency Management:** Optimized deployment packages by moving external Python libraries (PyMySQL) into **Lambda Layers**, significantly reducing function execution cold starts and promoting code reusability.

## 📷 Lab Evidence
| Task | Execution Output | Evidence |
| :--- | :--- | :--- |
| **1** | Lambda Function & Layer Creation | ![Lambda_Setup](./images/178_Lambda_Config.png) |
| **2** | Event Source (EventBridge) Mapping | ![Event_Source](./images/178_Lambda_Trigger.png) |
| **3** | Troubleshooting & Log Analysis | ![Log_Output](./images/178_Lambda_Logs.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Encountered a `Task timed out` error during initial testing of the data extractor function due to VPC networking latency and network interface attachment delays.
* **Engineering Resolution:** Identified that the function required sufficient time to establish a secure database connection within the private subnet. Adjusted the function's execution timeout from 3 seconds to a more robust threshold and verified Security Group ingress rules to permit MySQL traffic (Port 3306) between the Lambda and the DB host.
* **"What If" Scenario:** In a production environment, I would implement **Dead Letter Queues (DLQ)** on the Lambda functions to capture and alert on failed executions for manual inspection or automated retries. I would also move static configuration (like the SNS Topic ARN) into a dedicated service discovery mechanism or SSM Parameter Store to improve environment portability.

## 📊 Technical Competence
* **Demonstrated Skills:** Serverless Architecture Design (FaaS), EventBridge/CloudWatch Scheduling (Cron), VPC Networking/Security Groups for Lambda, Lambda Layer Management, IAM Role/Trust Policy configuration, SNS Topic Orchestration.
