## Relational Database Foundations & SQL Window Functions
**Course ID:** 273-[DB]-Lab

### 🎯 Project Goal
The goal of this lab was to get comfortable working with relational databases directly from the command line. I practiced securely logging into a hosted MariaDB server on a Linux EC2 instance and writing advanced SQL queries using **Window Functions** (`PARTITION BY`, `SUM() OVER`, and `RANK() OVER`) to analyze complex, real-world data sets without modifying the underlying tables.

### ⚙️ How it Works
* **Secure Database Access:** I connected to the database server using SSH, switched to root privileges, and used the MySQL CLI client to authenticate securely into the MariaDB monitor.
* **Running Totals & Analytical Querying:** Instead of using basic aggregate functions that collapse rows, I used window functions (`SUM() OVER`) to calculate running population totals across specific regions while keeping individual country details intact.
* **Data Ranking & Partitioning:** I leveraged the `RANK() OVER` function combined with `PARTITION BY` to group countries by their geographic region and automatically rank them from highest to lowest population.

### 📷 Lab Evidence
| Task | Delivery Check | Evidence |
| :---: | :--- | :--- |
| **1** | Secure MariaDB Authentication & Login | ![Secure MariaDB Login](images/01_mariadb_login_success.png) |
| **2** | SQL Window Functions (Running Totals & Country Rank) | ![SQL Window Functions](images/02_sql_window_functions_running_total.png) |
| **3** | Regional Partitioning & Custom Ranking Query | ![Regional Partitioning](images/03_sql_regional_rank_partition.png) |

### 🛠️ Lessons Learned & Optimization
* **Grouping vs. Partitioning:** This lab really helped me understand the difference between `GROUP BY` and `PARTITION BY`. With `GROUP BY`, the database collapses my rows into single summary rows. By using `PARTITION BY` inside a window function, I can calculate values like running totals or ranks and still display every single country's row side-by-side.
* **Handling Ties in Ranking:** I noticed how `RANK()` behaves when values are identical. For example, in the Antarctica region where populations are all 0, they all shared a rank of 1. In a production application, if I wanted to avoid skipping rank numbers after a tie (like jumping from 1 to 6), I learned I could use `DENSE_RANK()` instead to keep the ranking numbers sequential.
* **The CLI DB Advantage:** While graphical tools (like phpMyAdmin or DBeaver) are nice, knowing how to log directly into a terminal-based database monitor is a lifesaver. If an application server is struggling and you can't load a web GUI, being able to SSH in and run diagnostics directly via raw SQL is an essential skill for any sysadmin or cloud engineer.

### 📊 Technical Competence
Relational Database Administration, SQL Query Design, Advanced Window Functions (`SUM() OVER`, `RANK() OVER`), Data Partitioning & Ordering, MariaDB CLI Navigation.
