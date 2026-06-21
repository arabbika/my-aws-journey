# ◈ AWS Lambda Event-Driven Foundations
**Course ID**: `178-[JAWS]-Activity`

## 🎯 Serverless Objective
This lab introduces the paradigm of serverless architecture. The objective is to decouple compute logic from infrastructure, utilizing AWS Lambda to execute code in response to specific system events, thereby eliminating the need for server management.



## ⚡ Execution & Logic Flow
* **Event Integration:** [E.g., "Configured S3 'Object Created' events to trigger Lambda functions, enabling automated image processing upon file upload."]
* **Logic Decoupling:** [E.g., "Deployed modular code logic that executes only during event triggers, optimizing for cost and compute-on-demand requirements."]

## 📷 Lab Evidence
| Task | Execution Output | Evidence |
| :--- | :--- | :--- |
| **1** | Lambda Function Creation & Config | ![Lambda_Setup](./images/178_Lambda_Config.png) |
| **2** | Event Source Mapping (Trigger) | ![Event_Source](./images/178_Lambda_Trigger.png) |
| **3** | Execution Logs (CloudWatch) | ![Log_Output](./images/178_Lambda_Logs.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Lambda function timed out during execution because the processing task exceeded the default 3-second limit."]
* **Engineering Resolution:** [How you fixed it: e.g., "Analyzed execution duration in CloudWatch, identified the bottleneck, and increased the function timeout configuration to 30 seconds to ensure successful completion."]
* **"What If" Scenario:** [In a production system, I would implement Dead Letter Queues (DLQ) to capture failed events for asynchronous retry and use environment variables to manage configuration values without hard-coding.]

## 📊 Technical Competence
* **Demonstrated Skills:** Serverless Architecture Design, Event-Driven Programming, AWS Lambda Lifecycle & Triggers, CloudWatch Log Analysis.
