# ◈ RDS Database and Application Integration
**Course ID**: `160-[DF]-Lab`

## 🎯 Architectural Objective
This lab focuses on the seamless integration between compute and data tiers. The objective is to deploy a scalable Amazon RDS instance and configure secure connectivity from an application server, ensuring that sensitive credentials are managed and data flows are restricted to authorized resources.



## 🛡️ Integration & Security Logic
* **Network Connectivity:** [E.g., "Configured Security Groups to permit traffic on the database port (e.g., 3306) exclusively from the application server's private IP, ensuring the DB is never exposed to the public internet."]
* **Secure Access:** [E.g., "Implemented Secrets Manager to handle database credentials, removing hard-coded passwords from the application configuration."]

## 📷 Lab Evidence
| Task | Integration Milestone | Evidence |
| :--- | :--- | :--- |
| **1** | RDS Instance Provisioning | ![RDS_Setup](./images/160_RDS_Instance.png) |
| **2** | App-to-DB Security Group Mapping | ![SG_Config](./images/160_SG_Mapping.png) |
| **3** | Successful Connection/Query Test | ![Conn_Test](./images/160_DB_Connect.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Application server timed out when attempting to reach the RDS instance, despite correct credentials."]
* **Engineering Resolution:** [How you fixed it: e.g., "Investigated the Security Group attached to the RDS instance and identified that it was not allowing inbound traffic from the application's subnet; updated the ingress rules and verified connectivity via `telnet`."]
* **"What If" Scenario:** [In a production environment, I would deploy the RDS instance in a Multi-AZ configuration for high availability and use AWS Database Proxy to manage connection pooling, reducing overhead on the database engine during traffic spikes.]

## 📊 Technical Competence
* **Demonstrated Skills:** RDS Management (Multi-AZ/Read Replicas), Security Group Orchestration, Database Connection Pooling, Secrets Management, Network Troubleshooting.
