# ◈ Serverless Architecture Challenge
**Course ID**: `177-[JAWS]-Lab`

## 🎯 Architectural Objective
This project represents an advanced serverless architectural challenge. The objective was to design and deploy a fully event-driven processing pipeline, utilizing S3 as a data ingest layer, AWS Lambda as the compute engine for automated text analytics, and Amazon SNS as the asynchronous notification channel.



## 🛡️ Governance & Integration Logic
* **Event Ingestion:** Configured S3 "Object Created" event notifications to act as the trigger mechanism, ensuring the compute layer scales automatically with data arrival.
* **Compute & Data Integration:** Orchestrated a Lambda function to perform real-time text analysis on uploaded objects. Integrated the function with Amazon SNS to handle outbound communications, ensuring decoupled, reliable delivery of processed results.
* **Identity & Security:** Applied the provided `LambdaAccessRole` (pre-configured with `AmazonS3FullAccess`, `AmazonSNSFullAccess`, and `CloudWatchFullAccess`) to grant the function least-privilege administrative rights to perform file reading and notification publishing.

## 📷 Lab Evidence
| Task | Integration Milestone | Evidence |
| :--- | :--- | :--- |
| **1** | S3 Event-Trigger Configuration | ![S3_Trigger](./images/177_S3_Trigger.png) |
| **2** | Lambda Function Logic & SNS Integration | ![Lambda_Logic](./images/177_Lambda_Backend.png) |
| **3** | End-to-End Execution Validation | ![API_Test](./images/177_API_Test.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Function execution failed to trigger upon object upload, despite the S3 bucket being correctly configured.
* **Engineering Resolution:** Debugged the S3-to-Lambda event notification path. Identified a missing permission on the S3 bucket's resource policy, which prevented the bucket from having the necessary `lambda:InvokeFunction` authority. Updated the function resource policy to allow `s3.amazonaws.com` as a principal, successfully enabling the trigger.
* **"What If" Scenario:** In a production environment, I would implement an **Amazon SQS (Simple Queue Service)** buffer between the S3 trigger and the Lambda function. This would prevent data loss if the Lambda function hits concurrency limits during a massive file upload spike and allows for robust retries on failed word-count processing tasks.

## 📊 Technical Competence
* **Demonstrated Skills:** Serverless Event-Driven Orchestration, S3 Event Notification Configuration, Compute Logic Design (Python), SNS Topic Management, Permission/Resource Policy Management.
