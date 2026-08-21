# ☁️ AWS SimuLearn: Networking Concepts

## 🎯 Objective
Configure Virtual Private Cloud (VPC) routing tables and Security Group inbound rules to enable end-to-end communication between a public-facing web tier and a isolated database tier running in a private subnet.

---

## 🏗️ Architecture & Configuration
* **Region:** `us-east-1` (N. Virginia)
* **VPC CIDR:** `10.10.0.0/16`
* **Public Subnet:** `10.10.0.0/24` (WebServerSubnet)
* **Private Subnet:** `10.10.2.0/24` (DbServerSubnet)
* **Security Groups:** 
  * `WebServerSecurityGroup` (Inbound: HTTP Port 80 from `0.0.0.0/0`)
  * `DbServerSecurityGroup` (Inbound: MySQL/Aurora Port 3306 from `WebServerSecurityGroup`)

---

## 🛠️ Key Implementation Steps
1. **Public Route Table Configuration:** Replaced the outbound NAT Gateway target in `RouteTable2` with an **Internet Gateway (`igw-xxxxxxx`)** destination (`0.0.0.0/0`) to make `WebServerSubnet` publicly accessible from the internet.
2. **Web Server Hardening:** Updated `WebServerSecurityGroup` inbound rules to allow incoming HTTP traffic on **Port 80** from `0.0.0.0/0` and set outbound rules to allow all traffic.
3. **Database Tier Isolation (DIY Task):** Configured `DbServerSecurityGroup` inbound rules to allow **MySQL/Aurora (Port 3306)** traffic restricted exclusively to requests originating from `WebServerSecurityGroup`.
4. **Validation & Verification:** Loaded the web application via public IP to confirm an active end-to-end database connection and submitted the database security group details for validation.

---

## 💡 Key Architectural Takeaway
Implementing multi-tier network security requires strict isolation principles. Public web servers should handle incoming internet traffic via Internet Gateways, while database servers in private subnets should only accept inbound connections on database ports (Port 3306) sourced directly from the web tier's security group.

---

## 📜 Certification & Verification

<p align="center">
  <a href="https://github.com/arabbika/my-aws-journey/blob/main/Certifications/Networking%20Concepts.png" target="_blank">
    <img src="https://raw.githubusercontent.com/arabbika/my-aws-journey/main/Certifications/Networking%20Concepts.png" alt="AWS SimuLearn - Networking Concepts Badge" width="350" />
  </a>
</p>
