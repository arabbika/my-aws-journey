# ◈ EBS Volume Management
**Course ID**: `182-[JAWS]-Lab`

## 🎯 Project Goal
The goal of this lab was to understand how block storage works in AWS by managing the complete lifecycle of an Amazon Elastic Block Store (EBS) volume. I practiced provisioning a new volume, attaching it to a running Linux server, formatting and mounting the file system, and executing backup and recovery procedures using EBS snapshots.



## ⚙️ How it Works
Volume Lifecycle Management: I created a new General Purpose (gp2) EBS volume from the AWS Management Console and attached it as a raw block device to an active EC2 instance.

Linux File System Integration: To make the raw storage usable, I formatted the block device with an ext3 file system using mkfs and mapped it to the directory tree at /mnt/data-store using the mount command.

Persistence Configuration: I edited the system's /etc/fstab configuration file so that the operating system would remember the mount point and automatically reconnect the storage whenever the server reboots.

## 📷 Lab Evidence
| Task | Storage Operation | Evidence |
| :--- | :--- | :--- |
| **1** | EBS Volume Creation & Attachment | ![Volume_Attach](./images/182_EBS_Attach.png) |
| **2** | File System Formatting & Mounting | ![FS_Mount](./images/182_EBS_Mount.png) |
| **3** | Snapshot Restoration & Data Integrity | ![Data_Check](./images/182_EBS_Data.png) |

## 🛠️ Lessons Learned & Optimization
The Ghost Volume Trap: During testing, I noticed that if I rebooted the EC2 instance, my newly mounted storage would completely vanish from the directory tree. I learned that manual mount commands only last for the current login session. To fix this permanently, I looked up the disk's unique attributes and added them to /etc/fstab, ensuring the storage survives server restarts.

Disaster Recovery with Snapshots: I practiced taking a point-in-time backup (snapshot) of my volume, deleting some sample files, and then creating a brand-new EBS volume from that snapshot. Attaching the new volume proved that the data was perfectly intact, showing how snapshots serve as a fast backup and recovery solution.

Cross-AZ Considerations: Working through this lab highlighted a crucial EBS behavior: an EBS volume can only be attached to an EC2 instance in the exact same Availability Zone (AZ). If I need to move data to a different AZ for high availability, taking a snapshot and restoring it as a new volume in the target zone is the correct cloud architecture pattern.

## 📊 Technical Competence
EBS Volume Management, Linux File System Utilities (mkfs, mount, lsblk), Persistent Storage Architecture (/etc/fstab), Point-in-Time Snapshotting, Backup & Disaster Recovery Design.
