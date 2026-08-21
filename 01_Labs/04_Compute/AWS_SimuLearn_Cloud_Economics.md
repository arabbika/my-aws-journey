# ☁️ AWS SimuLearn: Cloud Economics

## 🎯 Objective
Model cloud workload operational costs using the AWS Pricing Calculator, compare purchasing models (On-Demand vs. Savings Plans/Reserved Instances), and perform cost optimization through workload rightsizing.

---

## 🏗️ Architecture & Configuration
* **Estimation Tool:** AWS Pricing Calculator (`calculator.aws`)
* **Region:** `us-east-1` (N. Virginia)
* **Initial Compute Profile:** `t3.medium` (Baseline: 2 instances | Peak: 4 instances over 8 hrs/day)
* **Optimized Compute Profile (DIY Task):** `t2.micro` (General Purpose, 1 vCPU, 1 GiB RAM)
* **EBS Storage:** 10 GB General Purpose SSD (`gp3`), 30 IOPS, Weekly Snapshots (1 GB delta)
* **Data Transfer:** 1 TB/month Inbound (Free), 100 GB/month Outbound to Internet

---

## 🛠️ Key Implementation Steps
1. **Workload Modeling:** Configured a custom estimation group (`Web Servers`) simulating variable daily web traffic spikes requiring baseline and peak capacity scaling.
2. **Pricing Structure Analysis:** Evaluated cost models including On-Demand rates, Compute Savings Plans, EC2 Instance Savings Plans, and Standard/Convertible Reserved Instances.
3. **Storage & Bandwidth Provisioning:** Estimated monthly costs for attached EBS `gp3` block storage, automated snapshots, and outbound internet egress traffic.
4. **Cost Optimization & Rightsizing (DIY Task):** Modified the compute specification, transitioning the instance family from `t3.medium` to a rightsized `t2.micro` footprint to minimize total cost of ownership (TCO).
5. **Estimate Generation:** Generated and submitted a public AWS estimate URL for automated solution validation.

---

## 💡 Key Architectural Takeaway
Cost optimization in the cloud requires continuous rightsizing and workload evaluation. By selecting instance families that strictly align with actual resource utilization (vCPU/RAM) and leveraging appropriate purchasing models, organizations can significantly reduce compute spend without compromising application functional requirements.

---

## 📜 Certification & Verification

<p align="center">
  <a href="https://github.com/arabbika/my-aws-journey/blob/main/Certifications/Cloud%20Economics.png" target="_blank">
    <img src="https://raw.githubusercontent.com/arabbika/my-aws-journey/main/Certifications/Cloud%20Economics.png" alt="AWS SimuLearn - Cloud Economics Badge" width="350" />
  </a>
</p>
