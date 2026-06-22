# ◈ Amazon Linux AMI Fundamentals
**Course ID**: `225-[LX]-Lab`

## 🎯 System Objective
This lab establishes the baseline for cloud-based system administration. The objective is to securely connect to an Amazon Linux environment and master the Linux `man` (manual) pages, ensuring proficiency in navigating system documentation and command syntax.



## ⚙️ Execution & Exploration Logic
* **Remote Access:** Established secure connectivity to the EC2 instance using SSH/PuTTY with key-pair authentication, ensuring encrypted management access.
* **Documentation Mastery:** Utilized the `man` command to navigate internal Linux help documentation, identifying command syntax, descriptions, and functional headers (SYNOPSIS, OPTIONS, etc.).

## 📷 Lab Evidence
| Task | CLI Output | Evidence |
| :--- | :--- | :--- |
| **1** | SSH Authentication & Login | ![SSH_Login](./images/225_SSH_Access.png) |
| **2** | Man Page Interface Navigation | ![Man_Pages](./images/225_Man_Nav.png) |
| **3** | Identifying Command Headers | ![Command_Headers](./images/225_Man_Headers.png) |

## 🛠️ Operational Intelligence
Challenge: Encountered connectivity issues during SSH authentication due to file permission requirements and key format compatibility.

Engineering Resolution: Verified that the Public Key was correctly associated with the instance during provisioning. For Windows-based environments, I ensured the private key was correctly managed using PuTTYgen to convert the .pem file to .ppk format, ensuring compatibility with SSH clients and secure key-based authentication.

Efficiency Gains: Mastering the man pages reduces dependency on external documentation, allowing for rapid, context-aware troubleshooting directly from the CLI terminal during high-pressure incidents.
## 📊 Technical Competence
* **Demonstrated Skills:** SSH Key Management, CLI Navigation, Manual Page (Help) System Proficiency, Linux Instance Access Control.
