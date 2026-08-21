# 🌐 AWS SimuLearn: Connecting VPCs

## 🎯 Objective
Establish secure, private inter-VPC network connectivity between isolated department networks using AWS VPC Peering, explicit route table target configuration, and security group ICMP ingress authorization.

---

## 🏗️ Architecture & Configuration
* **Virtual Private Clouds (VPCs):**
  * **Developer VPC:** `192.168.0.0/20`
  * **Finance VPC:** `172.31.0.0/16`
* **Network Infrastructure:**
  * **VPC Peering Connection:** `Developer <> Finance`
  * **Routing Tables:** Bi-directional route entries directing cross-VPC CIDR traffic through the peering connection target (`pcx-*`)
  * **Security Group:** `FinanceServerSecurityGroup` enforcing ICMP IPv4 ingress rules scoped to `192.168.0.0/20`

---

## 🛠️ Key Implementation Steps
1. **Peering Connection Provisioning:** Initialized a non-overlapping requester-accepter peering connection (`Developer <> Finance`) across isolated department virtual private clouds.
2. **Route Table Configuration:**
   * Configured the **Developer Route Table** with destination `172.31.0.0/16` targeting the VPC Peering ID.
   * Configured the **Finance Route Table** with destination `192.168.0.0/20` targeting the VPC Peering ID.
3. **Firewall Ingress Hardening:** Modified `FinanceServerSecurityGroup` to permit Custom ICMP - IPv4 traffic originating strictly from the Developer VPC CIDR block.
4. **End-to-End Connectivity Validation:** Connected to `DeveloperServer` via AWS Systems Manager Session Manager and executed `ping` requests against `FinanceServer`'s private IP address to confirm successful packet traversal.

---

## 💡 Key Architectural Takeaway
VPC Peering allows instances across separate virtual private clouds to communicate using private IP addresses as if they were on the same network. Establishing connectivity requires three core layers: active peering acceptance, explicit bi-directional route table definitions, and security group ingress authorization.

---

## 📜 Certification & Verification

<p align="center">
  <a href="https://github.com/arabbika/my-aws-journey/blob/main/Certifications/Connecting%20VPCs.png" target="_blank">
    <img src="https://raw.githubusercontent.com/arabbika/my-aws-journey/main/Certifications/Connecting%20VPCs.png" alt="AWS SimuLearn - Connecting VPCs Badge" width="350" />
  </a>
</p>
