# ◈ Linux User, Group, and Process Management
**Course ID**: `229/239-[LX]-Lab`

## 🎯 System Objective
This lab focused on identity management and system monitoring. The objective was to implement secure user/group access controls, monitor system resource utilization, and automate routine auditing tasks to maintain operational health.



## ⚙️ Execution & Scripting
* **Identity Management:** Implemented the Principle of Least Privilege by creating custom users and groups, assigning members to roles (Sales, HR, Finance, etc.), and managing sudoer access.
* **Process Oversight:** Utilized monitoring utilities (`top`, `ps`, `grep`) to audit active system tasks and automated recurring file system reports using `cron` and `crontab`.
* **Automation:** Configured a daily automated audit script to parse system files and generate filtered logs, demonstrating proficiency in Linux task scheduling.

## 📷 Lab Evidence
| Task | CLI Output | Evidence |
| :--- | :--- | :--- |
| **1** | User/Group Membership Audit | ![Identity_Audit](./images/229_239_User_Group.png) |
| **2** | Process Monitoring Snapshot | ![Process_Monitor](./images/229_239_Process_Top.png) |
| **3** | Validated Cron Job Schedule | ![Cron_Audit](./images/229_239_Cron_Job.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Encountered "Permission Denied" errors when attempting to create files in restricted directories, and needed to troubleshoot why specific processes were not appearing in the audit logs.
* **Engineering Resolution:** Leveraged `sudo` for elevated administrative tasks and utilized piped commands (`ps -aux | grep -v root`) to refine process output by excluding unnecessary system-level root tasks.
* **Efficiency Gains:** Automated audit reporting via `crontab` replaces manual oversight, ensuring consistent reporting and alerting on system state changes without human intervention.

## 📊 Technical Competence
* **Demonstrated Skills:** User/Group Lifecycle Management, Linux Identity Security, Resource/Process Monitoring, Cron Job Scheduling & Automation, Log Analysis.
