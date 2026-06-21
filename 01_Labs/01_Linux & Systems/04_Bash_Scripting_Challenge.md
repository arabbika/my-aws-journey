# ◈ Advanced Bash Scripting and Automation
**Course ID**: `251/253-[LX]-Lab`

## 🎯 System Objective
This lab focuses on operational efficiency through automation. The objective was to design and deploy custom Bash scripts that replace repetitive manual workflows, ensuring repeatable, error-free system administration and backup management.



## ⚙️ Execution & Scripting
* **Script Design:** Developed modular Bash scripts utilizing variables, loops (`for`), and dynamic naming conventions to automate system backups and mass file generation.
* **Automation Workflow:** Implemented environment-aware variables (e.g., `$USER`, `$(date)`) to ensure scripts remain portable and functionally accurate across different execution sessions.
* **Logic Integration:** Designed conditional file management logic to dynamically detect existing file sequences, ensuring that batch automation processes pick up where previous runs concluded.

## 📷 Lab Evidence
| Task | CLI Output | Evidence |
| :--- | :--- | :--- |
| **1** | Backup Script Logic & Execution | ![Backup_Script](./images/251_253_Backup.png) |
| **2** | Dynamic File Generation (Challenge) | ![Batch_Files](./images/251_253_Challenge.png) |
| **3** | Log/File Integrity Verification | ![File_Check](./images/251_253_Verification.png) |

## 🛠️ Operational Intelligence
* **Challenge:** The challenge script required identifying the "highest" existing file number to prevent overwriting or resetting the sequence when generating new batches.
* **Engineering Resolution:** Implemented a pattern-matching filter using `ls` and `tail` to programmatically extract the maximum existing integer and increment from there, ensuring the automation remained state-aware.
* **Efficiency Gains:** Transitioning from manual `tar` commands to automated, timestamped backups reduces human error and guarantees a consistent, searchable audit trail of system states.

## 📊 Technical Competence
* **Demonstrated Skills:** Advanced Bash Scripting, Shell Variable Manipulation, Dynamic File/Directory Automation, Error Trapping & Logging, Automation Workflow Design.
