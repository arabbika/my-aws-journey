# ◈ S3 Advanced Storage Challenge
**Course ID**: `184-[JAWS]-Lab`

## 🎯 Architectural Objective
This project focused on the practical administration of Amazon S3, emphasizing object lifecycle management, granular access control, and CLI-based service interaction. The objective was to demonstrate the ability to securely provision, populate, and audit cloud object storage.



## ⚙️ Optimization & Lifecycle Logic
* **Access Control:** Implemented granular access patterns by configuring bucket-level and object-level permissions, demonstrating the distinction between private buckets and publicly accessible objects.
* **CLI Administration:** Leveraged the AWS CLI to interact directly with the S3 API, facilitating efficient object listing and administrative management of storage resources.

## 📷 Lab Evidence
| Task | Optimization Metric | Evidence |
| :--- | :--- | :--- |
| **1** | Bucket Provisioning & Object Upload | ![Bucket_Setup](./images/184_S3_Bucket_Setup.png) |
| **2** | Object-Level Public Access Configuration | ![Public_Access](./images/184_S3_Permissions.png) |
| **3** | CLI-based Resource Auditing | ![CLI_Audit](./images/184_S3_CLI_Audit.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Attempted to access an uploaded object via a web browser and received a 403 "Forbidden" error, despite the bucket being created successfully.
* **Engineering Resolution:** Identified that while the bucket permitted access, the individual object lacked the necessary public read permissions. Applied explicit object-level ACLs to grant the public read access, successfully resolving the connectivity error.
* **"What If" Scenario:** In a production system, I would strictly avoid public object-level ACLs. Instead, I would use **Bucket Policies** for controlled access and implement **S3 Block Public Access (BPA)** at the account level to prevent accidental exposure of sensitive data, utilizing **CloudFront with OAC** for secure, private object delivery.

## 📊 Technical Competence
* **Demonstrated Skills:** S3 Bucket Provisioning, AWS CLI Service Interaction (`aws s3`), Object-Level Access Control (ACLs), Public/Private Data Handling, AWS IAM Credential Management.
