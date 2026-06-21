# ◈ Relational Database Table Operations
**Course ID**: `268-[DF]-Lab`

## 🎯 Data Objective
This lab focused on the fundamentals of relational database design and management. The objective was to construct normalized table schemas, define data types and constraints to ensure relational integrity, and perform administrative operations using Data Definition Language (DDL).



## ⚙️ Schema & Execution Logic
* **Schema Design:** Designed normalized database tables (e.g., `world.country`, `world.city`), selecting appropriate data types (e.g., `CHAR`, `INT`, `ENUM`) to balance storage efficiency and query performance.
* **Table Implementation:** Executed comprehensive SQL DDL statements:
    * `CREATE`: Initialized database and table structures with defined Primary Keys.
    * `ALTER`: Corrected schema drift and naming inconsistencies (e.g., renaming `Conitinent` to `Continent`).
    * `SHOW`: Validated metadata and object existence within the database environment.
    * `DROP`: Implemented controlled deletion of schema objects to maintain database cleanliness.

## 📷 Lab Evidence
| Task | Data Operation | Evidence |
| :--- | :--- | :--- |
| **1** | Database/Schema Initialization | ![Schema_Setup](./images/268_Schema_Design.png) |
| **2** | Table Creation & DDL Execution | ![Table_DDL](./images/268_Table_Creation.png) |
| **3** | Integrity Audit & Cleanup | ![Integrity_Audit](./images/268_FK_Validation.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Identified a critical naming error in the `country` table schema (`Conitinent`) immediately after creation, which would have caused integration failures in downstream applications.
* **Engineering Resolution:** Utilized the `ALTER TABLE RENAME COLUMN` statement to correct the schema attribute without needing to drop and re-create the entire table, demonstrating efficient, non-destructive administrative practices.
* **"What If" Scenario:** In a production environment, I would leverage **Migration Scripts** (using tools like Flyway or Liquibase) to version-control all schema changes. This ensures that any `ALTER` or `CREATE` operations are repeatable, auditable, and easily reversible if an update impacts application performance.

## 📊 Technical Competence
* **Demonstrated Skills:** Database Normalization, DDL/DML Syntax Proficiency, Relational Integrity (PK Constraints), Metadata Auditing, Schema Refactoring.
