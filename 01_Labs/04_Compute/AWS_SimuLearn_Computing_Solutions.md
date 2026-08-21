# ☁️ AWS SimuLearn: Computing Solutions

## 🎯 Simulearn Objective
Evaluate Amazon EC2 instance families, analyze compute performance requirements, and perform a live instance type resize to scale an application's compute and memory capacity.

---

## 🏗️ Architecture & Configuration
* **Region:** `us-east-1` (N. Virginia)
* **Initial Instance State:** `Running` | Type: `t3.micro` / `t3.large` family
* **Target Instance State:** `Stopped` | Type: `m4.large` (General Purpose)
* **Access Method:** EC2 Instance Connect (Public IP)

---

## 🛠️ Key Implementation Steps
1. **Instance & Metric Inspection:** Inspected the running compute instance, verified instance details, and accessed the node using EC2 Instance Connect to examine system application logs (`tail -f aws_compute_solutions.log`).
2. **Instance Family Comparison:** Compared specification trade-offs (vCPUs, RAM, Bandwidth, and Pricing) across General Purpose (`t3`), Compute Optimized (`c5`), and Memory Optimized (`r5`) instance types.
3. **Graceful Lifecycle Management:** Executed a controlled instance stop operation to transition the server into a modifiable `Stopped` state.
4. **Compute Resizing (DIY Task):** Modified the instance configuration via **Actions > Instance settings > Change instance type**, upgrading the node to an `m4.large` instance type.
5. **Validation:** Extracted and submitted the Instance ID (`i-xxxxxxxxxxxxxxxxx`) to verify successful instance type reconfiguration.

---

## 💡 Key Architectural Takeaway
Scaling compute resources vertically requires managing instance lifecycle states. EC2 instance types cannot be modified while running; stopping the instance allows seamless rightsizing across instance families to meet changing application workloads without re-provisioning storage or networking.

---

## 📜 Certification & Verification

<p align="center">
  <a href="https://github.com/arabbika/my-aws-journey/blob/main/Certifications/Computing%20Solutions.png" target="_blank">
    <img src="https://raw.githubusercontent.com/arabbika/my-aws-journey/main/Certifications/Computing%20Solutions.png" alt="AWS SimuLearn - Computing Solutions Badge" width="350" />
  </a>
</p>
