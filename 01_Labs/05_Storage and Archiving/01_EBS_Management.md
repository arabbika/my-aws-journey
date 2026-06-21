# ◈ EBS Volume Management
**Course ID**: `182-[JAWS]-Lab`

## 🎯 Storage Objective
This lab focused on implementing durable, high-performance block storage. The objective was to demonstrate the full lifecycle of Amazon Elastic Block Store (EBS) volumes—from initial provisioning and attachment to file system configuration, data snapshotting, and disaster recovery via restoration.



## ⚙️ Execution & Scripting
* **Volume Lifecycle:** Provisioned `gp2` EBS volumes and performed dynamic attachment to active EC2 instances. 
* **System Integration:** Executed low-level Linux storage operations to prepare volumes for use:
    * `mkfs -t ext3`: Initialized the block device with an ext3 file system.
    * `mount`: Integrated the storage into the Linux directory tree at `/mnt/data-store`.
    * `fstab` Configuration: Updated `/etc/fstab` to ensure persistent mounting across system reboots, preventing data accessibility issues.

## 📷 Lab Evidence
| Task | Storage Operation | Evidence |
| :--- | :--- | :--- |
| **1** | EBS Volume Creation & Attachment | ![Volume_Attach](./images/182_EBS_Attach.png) |
| **2** | File System Formatting & Mounting | ![FS_Mount](./images/182_EBS_Mount.png) |
| **3** | Snapshot Restoration & Data Integrity | ![Data_Check](./images/182_EBS_Data.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Discovered that manually mounted volumes lose their configuration after a system reboot, which is a critical risk for production application availability.
* **Engineering Resolution:** Diagnosed the issue by auditing the mount table; resolved by appending the correct UUID or device path to `/etc/fstab`, ensuring the OS automatically reconciles the volume at startup.
* **Efficiency Gains:** Utilizing EBS Snapshots allowed for rapid data recovery and cloning. This workflow is essential for disaster recovery (DR) planning, ensuring that storage state can be migrated or restored to new volumes in different Availability Zones if necessary.

## 📊 Technical Competence
* **Demonstrated Skills:** EBS Lifecycle Management (Provisioning/Attachment), Linux File System Operations (`mkfs`, `mount`, `lsblk`), Persistent Storage Architecture, `/etc/fstab` Configuration, Disaster Recovery (Snapshots).
