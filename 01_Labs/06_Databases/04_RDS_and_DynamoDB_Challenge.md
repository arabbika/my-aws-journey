# ◈ RDS Implementation & Data Relational Challenge
**Course ID**: `162-[DF]-Lab`

## 🎯 Data Objective
This lab focused on the architectural deployment of a relational database solution using Amazon RDS. The objective was to demonstrate end-to-end management, from provisioning a secure database instance to implementing normalized table schemas, performing bulk data insertion, and executing complex relational queries (JOINs) to extract integrated insights.



## 🛡️ Integration & Design Logic
* **Relational Deployment (RDS):** Provisioned a MySQL RDS instance within a controlled VPC environment, adhering to specific resource constraints (Burstable `db.t3` classes and General Purpose SSD storage).
* **Schema Orchestration:** Developed two distinct tables (`RESTART` and `CLOUD_PRACTITIONER`) with specific data types (Number, Date/Time). Implemented a relational link between these tables to demonstrate proficiency in normalizing structured data.
* **Complex Data Analysis:** Performed inner joins across the schema to synthesize disparate data points (Student ID, Name, and Certification Date), validating the relational integrity of the database.

## 📷 Lab Evidence
| Task | Implementation | Evidence |
| :--- | :--- | :--- |
| **1** | RDS Instance Deployment & Security | ![RDS_Config](./images/162_RDS_Challenge.png) |
| **2** | Table Construction & Bulk DML | ![Schema_Setup](./images/162_Schema_Design.png) |
| **3** | Relational JOIN Query Results | ![Join_Results](./images/162_Join_Analysis.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Encountered connectivity issues between the client LinuxServer and the RDS instance during the initial setup phase.
* **Engineering Resolution:** Identified that the security group attached to the RDS instance did not permit inbound traffic from the LinuxServer. Updated the ingress security rules to allow MySQL traffic (Port 3306) specifically from the instance's private IP, ensuring secure and authorized communication.
* **"What If" Scenario:** In a production-grade system, I would use **Infrastructure as Code (IaC)**, such as Terraform or AWS CloudFormation, to deploy the database instance and security rules. This would eliminate manual configuration errors and ensure that the database environment is always provisioned according to strict security and compliance standards.

## 📊 Technical Competence
* **Demonstrated Skills:** RDBMS Lifecycle Management, SQL Table Construction, Relational Data Modeling (Primary/Foreign Key logic), Complex Join Analysis, VPC Security Group Orchestration.
