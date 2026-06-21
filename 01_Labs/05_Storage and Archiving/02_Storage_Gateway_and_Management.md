# ◈ Storage Gateway and EFS Configuration
**Course ID**: `183-[JAWS]-Lab`

## 🎯 Storage Objective
This lab focused on implementing scalable, multi-client storage solutions and automating data durability. The objective was to manage block storage lifecycle via CLI automation and implement object-storage synchronization patterns to ensure data availability and version control.



## 🛡️ Governance & Access Logic
* **Elastic Scaling:** Configured shared file systems to provide high-availability storage accessible across compute instances.
* **Storage Lifecycle Automation:** Implemented `cron`-based automated snapshotting for EBS volumes and Python-based retention policies to prune older snapshots, optimizing storage costs and compliance.
* **Hybrid/Cross-Service Sync:** Utilized `aws s3 sync` to bridge local EBS storage with Amazon S3, establishing an off-site, durable backup target for critical data.

## 📷 Lab Evidence
| Task | Storage Configuration | Evidence |
| :--- | :--- | :--- |
| **1** | Automated Snapshot Lifecycle (cron) | ![Snapshot_Config](./images/183_Snapshot_Cron.png) |
| **2** | S3 Bucket Versioning & Sync Setup | ![S3_Sync](./images/183_S3_Versioning.png) |
| **3** | Version Restoration & Data Recovery | ![Recovery_Test](./images/183_Data_Recovery.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Managing an ever-growing repository of EBS snapshots, which can lead to significant storage overhead if not pruned regularly.
* **Engineering Resolution:** Developed and deployed a Python retention script (`snapshotter_v2.py`) to enforce a "Keep Last 2" snapshot policy, effectively automating lifecycle management and reducing manual overhead.
* **"What If" Scenario:** In a production environment, I would leverage **AWS Backup** to centralize and automate backup policies across multiple AWS services (EBS, EFS, RDS) and use **S3 Lifecycle Policies** to transition aging data to S3 Glacier, further optimizing cost-to-durability ratios.

## 📊 Technical Competence
* **Demonstrated Skills:** Automated Storage Lifecycle Management (CLI/Python), Cron Scheduling, S3 Data Synchronization, Object Versioning & Disaster Recovery, Hybrid Storage Patterns.
