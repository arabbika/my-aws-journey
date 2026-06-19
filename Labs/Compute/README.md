# ◈ EC2 Foundations and Provisioning
**Course ID**: `11-[CF]-Lab`

## 🎯 Architectural Objective
Establishing a foundational compute environment to understand resource provisioning, state management, and the impact of instance sizing on infrastructure performance.

## ⚙️ Technical Implementation
* **Compute:** Provisioned a `t3.micro` Linux-based instance using the Amazon Linux AMI, selected for its balance of performance and cost-efficiency.
* **Network:** Configured network integration by assigning the compute resource to a specific VPC subnet, ensuring proper connectivity within the isolated lab environment.
* **Lifecycle Management:** Executed instance state transitions (Stop/Start operations) to perform infrastructure modifications, transitioning the instance type from a `t3.micro` to an `m4.large` to demonstrate vertical scaling.

## 🛠️ Operational Intelligence (Troubleshooting)
* **Real-World Challenge:** Encountered a configuration dependency where the instance type modification was restricted while the resource was in a "Running" state.
* **Engineering Resolution:** Identified the requirement for a clean shutdown; performed a controlled stop of the instance to modify the configuration, then successfully verified the new instance type (`m4.large`) in the EC2 dashboard.
* **"What If" Scenario:** In a production environment, I would utilize **AWS Auto Scaling Groups (ASG)** to manage instance types and fleet capacity dynamically based on load, preventing the need for manual state transitions and associated service downtime.

## 📊 Technical Competence
* **Demonstrated Skills:** Infrastructure Provisioning, Lifecycle State Management, Vertical Scaling, and Resource Configuration.
