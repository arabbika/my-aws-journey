# ◈ Storage Gateway and EFS Configuration
**Course ID**: `183-[JAWS]-Lab`

## 🎯 Storage Objective
This lab focuses on implementing scalable, multi-client storage solutions. The objective is to configure Amazon Elastic File System (EFS) for elastic, shared file access and explore Storage Gateway to bridge on-premises environments with AWS cloud storage.



## 🛡️ Governance & Access Logic
* **Elastic Scaling:** [E.g., "Deployed Amazon EFS with multiple mount targets to provide high-availability shared storage accessible by multiple EC2 instances simultaneously."]
* **Hybrid Connectivity:** [E.g., "Configured AWS Storage Gateway to extend on-premises storage capacity into the cloud, ensuring data consistency and optimized latency."]

## 📷 Lab Evidence
| Task | Storage Configuration | Evidence |
| :--- | :--- | :--- |
| **1** | EFS File System & Mount Target Setup | ![EFS_Config](./images/183_EFS_Setup.png) |
| **2** | Storage Gateway Gateway Setup | ![Gateway_Config](./images/183_Gateway_Setup.png) |
| **3** | Cross-Instance File Access Verification | ![Access_Test](./images/183_Multi_Instance.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Instances in the private subnet were unable to mount the EFS target due to network connectivity restrictions."]
* **Engineering Resolution:** [How you fixed it: e.g., "Identified that Security Group rules on the EFS mount target were blocking NFS traffic (TCP port 2049) from the application security group; updated rules to permit necessary communication."]
* **"What If" Scenario:** [In a production environment, I would leverage EFS Lifecycle Management policies to automatically move infrequently accessed files to EFS Infrequent Access (IA) storage classes, significantly reducing overall storage costs.]

## 📊 Technical Competence
* **Demonstrated Skills:** Shared Storage (EFS) Lifecycle, NFS Protocol Management, Hybrid Cloud Architecture, Mount Target Security, Storage Tiering Strategies.
