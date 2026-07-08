# ◈ Linux CLI and File System Operations
**Course ID**: `227/233-[LX]-Lab`

🎯 Project Goal
The goal of this lab was to get comfortable working entirely inside the Linux terminal. I practiced navigating complex directory structures, managing files, and using administrative shortcuts to move around the file system quickly and efficiently without relying on a desktop interface.



## ⚙️ How it works
Directory Navigation & Control: I used absolute and relative paths with cd and pwd to move around the system, keeping track of exactly where I was in the directory tree.

File Manipulation: I built, copied, renamed, and cleaned up file structures using core Linux utilities like mkdir, touch, cp, mv, and rm.

Terminal Efficiency: To speed up my workflow, I leveraged Bash history features (history, !!, and CTRL+R) to recall and reuse complex commands instantly instead of retyping them.

## 📷 Lab Evidence
| Task | Delivery Check | Evidence |
| :--- | :--- | :--- |
| **1** | Hierarchical Folder Creation | ![Folder_Tree](./images/227_233_Folder_Creation.png) |
| **2** | Recursive Move & Reorganization | ![Move_Ops](./images/227_233_Reorg.png) |
| **3** | File System Audit (`ls -laR`) | ![Audit_Output](./images/227_233_Audit.png) |

## 🛠️ Lessons Learned & Optimization
The Non-Empty Directory Roadblock: While trying to clean up my folder structure, I kept hitting rmdir: failed to remove errors. I learned that rmdir only works on completely empty folders. To fix this, I switched to the recursive remove command (rm -r), which successfully cleared out the directory's contents and the folder itself in one shot.

The Power of Flags: I realized how crucial command flags are. For example, using ls -laR instead of just ls completely changes your visibility, allowing you to see hidden files (-a), detailed permissions (-l), and nested subdirectories (-R) all at once.

CLI vs. GUI: Doing this lab made it clear why system administrators stick to the CLI. Once you know the shortcuts, restructuring a massive file system using recursive commands is incredibly fast and easily automated, whereas doing it manually in a graphical interface would take forever.

## 📊 Technical Competence
Linux CLI Navigation, File & Directory Architecture, Bash History Shortcuts, Permission Auditing (ls), Recursive File Operations (cp -r, rm -r).
