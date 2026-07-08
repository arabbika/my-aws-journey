# ◈ Linux User, Group, and Process Management
**Course ID**: `229/239-[LX]-Lab`

## 🎯 Project Goal
The goal of this lab was to learn how to manage system identities securely and keep tabs on system health. I practiced setting up user accounts and group permissions to enforce the Principle of Least Privilege, monitored running processes, and set up a cron job to automate system auditing.


## ⚙️ How it Works
Identity & Access Management: I created dedicated user accounts and administrative groups (like Sales, HR, and Finance), assigned users to their respective roles, and managed elevated access using the sudoers file.

Process Tracking: I used monitoring utilities like top and ps combined with text filters to audit active system tasks, see what resources were being consumed, and identify specific running applications.

Task Automation: I configured automated scheduling using cron and edited the user crontab to run a daily background script that parses system files and generates filtered log reports automatically.

## 📷 Lab Evidence
| Task | Delivery Check | Evidence |
| :--- | :--- | :--- |
| **1** | User/Group Membership Audit | ![Identity_Audit](./images/229_239_User_Group.png) |
| **2** | Process Monitoring Snapshot | ![Process_Monitor](./images/229_239_Process_Top.png) |
| **3** | Validated Cron Job Schedule | ![Cron_Audit](./images/229_239_Cron_Job.png) |

## 🛠️ Lessons Learned & Optimization
Overcoming "Permission Denied" Walls: While trying to set up directories for different departments, I kept hitting permission errors. This forced me to really understand when to safely escalate privileges using sudo versus when to fix underlying group ownership with chown and chmod so users could do their work without admin rights.

Filtering out the Noise: Running a generic ps command dumps hundreds of active system processes to the screen, making it impossible to read. I optimized my auditing workflow by piping commands together—using ps aux | grep -v root to filter out background system tasks and zero in specifically on user actions.

Set It and Forget It: Manually checking server logs every day is inefficient and prone to human error. Automating my custom audit script through crontab showed me how easy it is to ensure regular, consistent monitoring happens entirely in the background while I focus on other tasks.

## 📊 Technical Competence
User & Group Lifecycle Management, Linux Access Controls (chmod/chown), Process Monitoring (top/ps), Bash Command Piping & Filtering (grep), Cron Automation & Scheduling.
