# ◈ Linux CLI and File System Operations
**Course ID**: `227/233-[LX]-Lab`

## 🎯 System Objective
This lab focused on mastering the Linux terminal environment. The objective was to demonstrate absolute proficiency in navigating hierarchical file systems, executing administrative commands, and mastering file manipulation—creating, moving, copying, and deleting data structures efficiently.



## ⚙️ Execution & Scripting
* **Navigation & Manipulation:** Executed complex file operations using core utilities (`mkdir`, `touch`, `cp -r`, `mv`, `rm -r`) to replicate and reorganize a specific organizational folder structure.
* **Administrative Workflow:** Optimized shell productivity by utilizing history commands (`history`, `CTRL+R`, `!!`) and path-based navigation (`cd`, `pwd`) to interact with the file system securely and reliably.

## 📷 Lab Evidence
| Task | CLI Output | Evidence |
| :--- | :--- | :--- |
| **1** | Hierarchical Folder Creation | ![Folder_Tree](./images/227_233_Folder_Creation.png) |
| **2** | Recursive Move & Reorganization | ![Move_Ops](./images/227_233_Reorg.png) |
| **3** | File System Audit (`ls -laR`) | ![Audit_Output](./images/227_233_Audit.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Encountered `rmdir: failed to remove` errors when attempting to delete non-empty directories during the reorganization phase.
* **Engineering Resolution:** Applied the recursive remove command (`rm -r`) to safely purge directory contents before folder deletion, demonstrating the importance of understanding command-specific flags and directory states.
* **Efficiency Gains:** Utilizing relative paths and recursive commands allows for rapid file system restructuring that would be significantly slower and more error-prone in a graphical interface.

## 📊 Technical Competence
* **Demonstrated Skills:** Command Line Interface (CLI) Navigation, Recursive File/Directory Manipulation, Bash History Management, Path-based File Operations.
