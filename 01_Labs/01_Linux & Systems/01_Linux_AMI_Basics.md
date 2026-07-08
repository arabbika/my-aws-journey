# ◈ Amazon Linux AMI Fundamentals
**Course ID**: `225-[LX]-Lab`

## 🎯 Project Goal
The goal of this lab was to establish a secure remote connection to a cloud-based Amazon Linux instance and learn how to use the built-in Linux documentation system (man pages) to figure out command syntax and flags without needing to google them.



## ⚙️ How it Works
Secure Remote Access: I connected to the hosted EC2 instance securely using an SSH client and public/private key-pair authentication to manage the server remotely.

Documentation Navigation: I utilized the man (manual) utility to open internal documentation directly in the terminal, learning how to quickly skim through structural sections like NAME, SYNOPSIS, and OPTIONS.

Command Discovery: Instead of guessing command flags, I used the built-in manual to look up specific arguments, structural requirements, and examples for essential Linux tools.

📷 Lab Evidence

## 📷 Lab Evidence
| Task | CLI Output | Evidence |
| :--- | :--- | :--- |
| **1** | SSH Authentication & Login | ![SSH_Login](./images/225_SSH_Access.png) |
| **2** | Man Page Interface Navigation | ![Man_Pages](./images/225_Man_Nav.png) |
| **3** | Identifying Command Headers | ![Command_Headers](./images/225_Man_Headers.png) |

## 🛠️ Lessons Learned & Optimization
The SSH Connection Hurdle: I initially ran into connection errors trying to authenticate. I learned that Windows SSH clients like PuTTY require private keys to be in .ppk format, whereas Linux/macOS terminals and modern OpenSSH tools use .pem files. Using PuTTYgen to convert the key format resolved the issue immediately.

Breaking the "Google Dependency": When working under pressure in a terminal, switching back and forth to a web browser to look up commands ruins your momentum. Learning to use man <command> keeps your hands on the keyboard and gives you the exact technical answers for the specific version of Linux you are running.

Keyboard Shortcuts Matter: Inside a manual page, you aren't just scrolling. I learned to use / to search for text, n to jump to the next match, and q to instantly exit back to the command prompt, making navigation incredibly fast.

## 📊 Technical Competence
Secure Shell (SSH) Connectivity, Key-Pair Configuration (.pem vs .ppk), Linux Manual System (man), Terminal Help Navigation, Cloud Instance Remote Administration.
