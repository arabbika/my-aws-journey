# Automating Infrastructure Deployments with AWS CloudFormation

**Course ID:** 190-[JAWS]-Lab

---

## 🎯 Project Goal
The goal of this lab was to transition from manual infrastructure provisioning to Infrastructure as Code (IaC) using AWS CloudFormation. I practiced defining foundational networking, security groups, cloud storage, and compute resources using declarative YAML templates. Through iterative updates, I learned how to modify running stacks, leverage dynamic SSM parameter lookups, and safely tear down entire environments cleanly.

---

## ⚙️ How it Works
* **Declarative Template Provisioning:** I created and customized a CloudFormation template in YAML format to define a complete Virtual Private Cloud (VPC) network architecture, including an Internet Gateway, Public Subnet, Route Tables, and Security Groups.
* **Dynamic AMI Resolution via SSM:** Rather than hardcoding region-specific Amazon Machine Image (AMI) IDs, I integrated an SSM Parameter Store lookup (`/aws/service/ami-amazon-linux-latest/amzn2-ami-hvm-x86_64-gp2`). This allows the CloudFormation stack to dynamically resolve the latest valid Amazon Linux 2 AMI across any AWS region.
* **Iterative Stack Updates & Change Sets:** I practiced updating existing live stacks by appending an Amazon S3 Bucket and an Amazon EC2 instance (`t3.micro`). CloudFormation automatically calculated change sets to provision only new resources without disrupting existing infrastructure.
* **Automated Cleanup:** To prevent persistent costs and orphaned cloud infrastructure, I executed a controlled stack deletion that automatically unwound and removed all created resources in reverse dependency order.

---

## 🧠 Lessons Learned & Optimization
* **Strict YAML Formatting Matters:** In CloudFormation, correct indentation and spacing are critical. A misplaced space can break the template parser. Ensuring precise 2-space alignment for resource keys and 4-space alignment for nested properties avoided template parsing errors.
* **Dynamic Parameter Utility:** Hardcoding AMI IDs in template files leads to brittle deployments because AMI IDs change by region and update over time. Querying the Systems Manager Parameter Store inside the template’s `Parameters` block ensures the stack remains portable and up-to-date across all regions.
* **Inter-Resource References (`!Ref`):** Using intrinsic functions like `!Ref` allowed me to logically link resources together (e.g., attaching the EC2 instance to `PublicSubnet` and `AppSecurityGroup`) without needing to know physical resource IDs prior to execution.

---

## 🛠️ Technical Competence
* Infrastructure as Code (IaC)
* AWS CloudFormation Stacks & Change Sets
* AWS Systems Manager (SSM) Parameter Store Integration
* Amazon Virtual Private Cloud (VPC) & Security Group Provisioning
* Amazon S3 Bucket Declarative Configuration
* Amazon EC2 Compute Deployment
