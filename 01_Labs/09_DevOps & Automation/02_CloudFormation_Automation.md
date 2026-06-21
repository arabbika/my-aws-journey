# ◈ CloudFormation Automated Deployments
**Course ID**: `190-[JAWS]-Lab`

## 🎯 Architectural Objective
This project represents the foundational shift from manual, imperative infrastructure management to declarative, automated deployments. The objective was to codify environment architecture—including VPCs, S3 buckets, and EC2 compute nodes—into modular CloudFormation templates, ensuring repeatable, consistent, and version-controlled infrastructure environments.



## ⚙️ Execution & IaC Logic
* **Template Engineering:** Developed and iterative improved YAML templates using structural hierarchies (`Parameters`, `Resources`, `Outputs`). Implemented dynamic AMI retrieval via `AWS::SSM::Parameter` to ensure regional template portability.
* **Orchestration & Dependency Management:** Leveraged intrinsic functions like `!Ref` to manage complex resource dependencies (e.g., binding an EC2 instance to a specific Subnet and Security Group), ensuring CloudFormation resolved the correct creation order automatically.
* **Change Management:** Utilized CloudFormation Change Sets to preview infrastructure modifications, ensuring that updates to existing stacks (like adding an S3 bucket or EC2 instance) were validated before execution.

## 📷 Lab Evidence
| Task | Automation Milestone | Evidence |
| :--- | :--- | :--- |
| **1** | Template Validation & Initial Stack Launch | ![Template_Valid](./images/190_CF_Lint.png) |
| **2** | Incremental Resource Addition (S3/EC2) | ![Stack_Create](./images/190_CF_Stack.png) |
| **3** | Change Set Preview & Deployment | ![Change_Set](./images/190_CF_Update.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Encountered stack update failures during the iterative addition of resources due to resource property syntax errors and indentation mismatches in the YAML schema.
* **Engineering Resolution:** Leveraged CloudFormation's "Events" tab to pinpoint the exact resource initialization failure. Corrected the YAML indentation (ensuring two-space standardization) and validated resource references, leading to a successful `UPDATE_COMPLETE` status.
* **"What If" Scenario:** In a production-grade system, I would integrate these templates into a CI/CD pipeline (e.g., AWS CodePipeline with `cfn-lint` for static analysis). This would allow me to automatically test infrastructure changes in a staging environment before deploying to production, effectively treating infrastructure as an immutable asset.

## 📊 Technical Competence
* **Demonstrated Skills:** Infrastructure as Code (CloudFormation), YAML Template Syntax, Intrinsic Function Usage (`!Ref`), Dynamic AMI Referencing (SSM Parameter Store), Resource Dependency Mapping, Change Set Orchestration.
