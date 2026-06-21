# ◈ Data Interaction and Lifecycle Management
**Course ID**: `269/270/271-[DF]-Lab`

## 🎯 Data Objective
This lab focused on the application layer of database management. The objective was to demonstrate absolute proficiency in performing CRUD operations (Create, Read, Update, Delete) and executing complex conditional queries to extract actionable insights from structured, multi-table relational databases.



## ⚙️ Query & Execution Logic
* **Data Manipulation (DML):** Executed `INSERT`, `UPDATE`, and `DELETE` statements to manage record states. Implemented safety measures, such as `FOREIGN_KEY_CHECKS` and `WHERE` clause filtering, to maintain ACID compliance and prevent data corruption.
* **Query Optimization & Analysis:** Leveraged advanced SQL functions to derive insights:
    * **Filtering:** Used `WHERE` clauses with `BETWEEN` and `LIKE` (wildcards) for pattern matching and range-based data retrieval.
    * **Aggregation:** Applied `SUM()` and `COUNT()` functions to calculate metrics across large datasets.
    * **Normalization:** Used column aliasing (`AS`) to improve result set readability and `LOWER()` to ensure case-insensitive integrity during search operations.

## 📷 Lab Evidence
| Task | Data Operation | Evidence |
| :--- | :--- | :--- |
| **1** | CRUD Operation Execution | ![CRUD_Ops](./images/269_271_CRUD_Ops.png) |
| **2** | Complex Query/Search Results | ![Query_Results](./images/269_271_Complex_Query.png) |
| **3** | Data Integrity & Audit Verification | ![Data_Audit](./images/269_271_Data_Audit.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Encountered sub-optimal query performance when running aggregate functions across large tables. 
* **Engineering Resolution:** Analyzed the execution plan and identified that full table scans were occurring. Implemented B-Tree indexes on frequently filtered columns (`Population`, `Region`), which significantly reduced query latency by providing faster data pathing.
* **"What If" Scenario:** In a high-traffic production environment, I would offload heavy read operations to **Read Replicas** to protect the primary instance’s write performance. Additionally, I would implement an **Amazon ElastiCache** layer to cache the results of frequently executed complex aggregate queries, further minimizing database load.

## 📊 Technical Competence
* **Demonstrated Skills:** SQL/DML Proficiency, Advanced Query Filtering (`BETWEEN`, `LIKE`), Aggregate Functions (`SUM`, `COUNT`), Transaction/Constraint Management, Performance Troubleshooting (Indexing), Data Import/Export Workflows.
