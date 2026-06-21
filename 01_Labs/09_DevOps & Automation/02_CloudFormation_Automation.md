# ◈ CloudFormation Automated Deployments
**Course ID**: `190-[JAWS]-Lab`

## 🎯 Architectural Objective
This project marks the shift from manual provisioning to automated infrastructure. The objective is to codify environment architecture into AWS CloudFormation templates, ensuring environment consistency, version control, and rapid, repeatable deployments.



## ⚙️ Execution & IaC Logic
* **Template Engineering:** [E.g., "Drafted modular YAML CloudFormation templates defining VPC, EC2, and Security Group resources, utilizing parameters for multi-environment flexibility."]
* **Deployment Automation:** [E.g., "Executed stack deployments via AWS CLI and CloudFormation console, implementing change sets to preview infrastructure modifications before applying."]

## 📷 Lab Evidence
| Task | Automation Milestone | Evidence |
| :--- | :--- | :--- |
| **1** | Template Validation (Linting) | ![Template_Valid](./images/190_CF_Lint.png) |
| **2** | Stack Provisioning & Resource Creation | ![Stack_Create](./images/190_CF_Stack.png) |
| **3** | Change Set Deployment/Updates | ![Change_Set](./images/190_CF_Update.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Stack creation failed during deployment due to a circular dependency between the Security Group and an EC2 instance."]
* **Engineering Resolution:** [How you fixed it: e.g., "Analyzed the stack event log, restructured the template resource dependencies using the `DependsOn` attribute, and successfully re-deployed."]
* **"What If" Scenario:** [In a production system, I would integrate these templates into a CI/CD pipeline (e.g., AWS CodePipeline) to automate testing, linting, and deployment, ensuring that infrastructure is treated exactly like application code.]

## 📊 Technical Competence
* **Demonstrated Skills:** Infrastructure as Code (CloudFormation), YAML/JSON Template Design, Dependency Management, Automated Provisioning, CI/CD Principles.
