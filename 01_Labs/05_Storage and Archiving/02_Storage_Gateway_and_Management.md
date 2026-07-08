# ◈ Storage Gateway and EFS Configuration
**Course ID**: `183-[JAWS]-Lab`

## 🎯 Project Goal
The goal of this lab was to implement scalable, multi-client storage solutions and automate data backups. I practiced using shared file systems, writing scripts to handle automated snapshots, and building synchronization workflows to replicate critical server data directly over to Amazon S3 for durable, off-site storage.


## 🛡️ How it Works
Scalable File Sharing: I configured high-availability, shared file systems designed to let multiple EC2 instances connect, read, and write to the same central storage pool simultaneously.

Backup Automation: I used a combination of Linux cron scheduling and a custom Python script to automatically take snapshots of block storage devices on a regular basis, enforcing a cost-saving retention policy.

S3 Synchronization: I integrated local storage volumes with object storage by building an automated synchronization pipeline using the AWS CLI, ensuring all critical data has a secure, version-controlled backup.

## 📷 Lab Evidence
| Task | Storage Configuration | Evidence |
| :--- | :--- | :--- |
| **1** | Automated Snapshot Lifecycle (cron) | ![Snapshot_Config](./images/183_Snapshot_Cron.png) |
| **2** | S3 Bucket Versioning & Sync Setup | ![S3_Sync](./images/183_S3_Versioning.png) |
| **3** | Version Restoration & Data Recovery | ![Recovery_Test](./images/183_Data_Recovery.png) |

## 🛠️ Lessons Learned & Optimization
Stopping Snapshot Sprawl: Leaving automated backup scripts to run indefinitely can quickly bloat AWS storage costs as old snapshots pile up. To solve this, I deployed a Python retention script (snapshotter_v2.py) that enforces a strict "Keep Last 2" rule—automatically sweeping the environment and deleting older, unneeded snapshots every time a new one is successfully created.

The S3 Sync Advantage: Rather than blindly copying massive data directories up to the cloud every night, I utilized aws s3 sync. This command evaluates file checksums and only transfers modified files. It cuts down on network bandwidth and speeds up backup jobs significantly.

Thinking Like a Cloud Architect: If I were deploying this setup in a production enterprise environment, I wouldn't rely entirely on custom cron scripts. I would centralize our compliance strategy using AWS Backup to coordinate snapshots across EBS and EFS automatically, and hook our S3 bucket up to S3 Lifecycle Policies to transition aging backups into ultra-low-cost S3 Glacier storage.

## 📊 Technical Competence
Automated Storage Lifecycle Management, Python Scripting (boto3 / Automation), Cron Job Scheduling, S3 Data Synchronization, Object Versioning & Disaster Recovery, Multi-Instance Shared Storage.
