# ◈ EBS Volume Management
**Course ID**: `182-[JAWS]-Lab`

## 🎯 Storage Objective
This lab focuses on implementing durable, high-performance block storage. The objective is to demonstrate the end-to-end lifecycle of Amazon Elastic Block Store (EBS) volumes, including creation, attachment, file system mounting, and data persistence management within an EC2 environment.



## ⚙️ Execution & Scripting
* **Volume Lifecycle:** [E.g., "Provisioned gp3 EBS volumes and attached them to running instances to provide scalable, persistent storage."]
* **System Integration:** [E.g., "Executed Linux commands (`lsblk`, `mkfs`, `mount`) to format and mount volumes, ensuring data persistence across instance reboots."]

## 📷 Lab Evidence
| Task | Storage Operation | Evidence |
| :--- | :--- | :--- |
| **1** | EBS Volume Creation & Attachment | ![Volume_Attach](./images/182_EBS_Attach.png) |
| **2** | File System Formatting & Mounting | ![FS_Mount](./images/182_EBS_Mount.png) |
| **3** | Persistence/Data Integrity Check | ![Data_Check](./images/182_EBS_Data.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Volume failed to auto-mount after an instance reboot, causing application data errors."]
* **Engineering Resolution:** [How you fixed it: e.g., "Diagnosed the issue by checking `/etc/fstab` and corrected the mount configuration to ensure persistent, automated re-mounting on boot."]
* **Efficiency Gains:** [Why is this approach better? e.g., "Understanding volume lifecycle management is critical for data durability and ensuring that persistent storage remains decoupled from instance compute lifecycle."]

## 📊 Technical Competence
* **Demonstrated Skills:** EBS Lifecycle Management (Provisioning/Attachment), Linux File System Operations (Format/Mount), Persistent Storage Architecture, `/etc/fstab` Configuration.
