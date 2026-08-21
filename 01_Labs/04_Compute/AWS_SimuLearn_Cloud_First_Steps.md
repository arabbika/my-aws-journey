# ☁️ AWS SimuLearn: Cloud First Steps

## 🎯 Simulearn Objective
Demonstrate multi-Availability Zone (Multi-AZ) fault tolerance by deploying EC2 compute instances across distinct physical Availability Zones within the same AWS Region (`us-east-1`).

---

## 🏗️ Architecture & Configuration
* **Region:** `us-east-1` (N. Virginia)
* **Instance 1 (AZ1):** `us-east-1a` | Amazon Linux 2023 | Public IPv4 Enabled
* **Instance 2 (AZ2):** `us-east-1b` (or `us-east-1c`) | Amazon Linux 2023 | Public IPv4 Enabled

---

## 🛠️ Key Implementation Steps
1. **AZ Identification:** Inspected the existing EC2 web instance to identify its assigned Availability Zone (`us-east-1a`).
2. **Multi-AZ Provisioning:** Launched a secondary EC2 instance (`t2.micro`) within the same region, explicitly overriding automatic subnet selection to pin deployment to an alternate subnet in a separate AZ.
3. **Network & Security Alignment:** Configured matching network interfaces and security groups to maintain baseline connectivity standards.
4. **Validation:** Extracted and submitted both unique Instance IDs (`i-xxxxxxxxxxxxxxxxx`) to verify multi-AZ deployment compliance.

---

## 💡 Key Architectural Takeaway
Deploying workloads across multiple Availability Zones provides high availability and fault tolerance. It ensures application resilience against localized infrastructure failures without changing regional routing parameters.

---

## 📜 Certification & Verification

<p align="center">
  <a href="https://github.com/arabbika/my-aws-journey/blob/main/Certifications/Cloud%20First%20Steps.png" target="_blank">
    <img src="https://raw.githubusercontent.com/arabbika/my-aws-journey/main/Certifications/Cloud%20First%20Steps.png" alt="AWS SimuLearn - Cloud First Steps Badge" width="350" />
  </a>
</p>
