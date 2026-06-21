# ◈ RDS and DynamoDB Implementation Challenge
**Course ID**: `162-[DF]-Lab`

## 🎯 Data Objective
This lab is a comparative architectural exercise. The objective is to evaluate and deploy both relational (RDS) and NoSQL (DynamoDB) solutions, determining the optimal data storage strategy based on schema requirements, scale, and access patterns.



## 🛡️ Integration & Design Logic
* **Relational Implementation (RDS):** [E.g., "Deployed a MySQL RDS instance for highly structured transactional data, focusing on ACID compliance and complex join operations."]
* **NoSQL Implementation (DynamoDB):** [E.g., "Provisioned a DynamoDB table for high-velocity, schema-less data, utilizing Partition and Sort keys to optimize for single-digit millisecond latency."]

## 📷 Lab Evidence
| Task | Implementation | Evidence |
| :--- | :--- | :--- |
| **1** | RDS Schema & Instance Deployment | ![RDS_Config](./images/162_RDS_Challenge.png) |
| **2** | DynamoDB Table & Index Creation | ![Dynamo_Config](./images/162_Dynamo_Challenge.png) |
| **3** | Comparative Load/Latency Test | ![Compare_Test](./images/162_Benchmarking.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "DynamoDB queries were returning incomplete data results due to inefficient partition key selection."]
* **Engineering Resolution:** [How you fixed it: e.g., "Analyzed the query patterns, redesigned the schema to include a Global Secondary Index (GSI), and successfully optimized data retrieval."]
* **"What If" Scenario:** [In a production environment, I would leverage AWS Database Migration Service (DMS) to transition data between these engines if access patterns evolved from structured transactional queries to high-scale, unstructured web requests.]

## 📊 Technical Competence
* **Demonstrated Skills:** RDBMS vs. NoSQL Architectural Comparison, DynamoDB Data Modeling (GSI/LSI), Transactional Integrity (ACID), Throughput Optimization (RCU/WCU).
