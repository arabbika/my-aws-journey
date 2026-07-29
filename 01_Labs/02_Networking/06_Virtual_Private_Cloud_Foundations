# ◈ Virtual Private Cloud Foundations
**Course ID**: `180-[JAWS]-Lab`

## 🎯 Project Goal
Designing and provisioning a custom logically isolated Virtual Private Cloud (VPC) network architecture to support multi-tier applications, enforce least-privilege network boundary controls, and enable secure outbound internet access for private resources.

## ⚙️ Technical Implementation
* **Network Topology:** Provisioned a custom VPC (`Lab VPC`) with a `10.0.0.0/16` IPv4 CIDR block and enabled DNS hostnames for automatic instance public DNS resolution.
* **Subnet Segmentation:** Partitioned network space into a `Public Subnet` (`10.0.0.0/24`) for internet-facing resources and a larger `Private Subnet` (`10.0.2.0/23`) to house isolated compute assets.
* **Routing & Gateways:** Attached an Internet Gateway (`Lab IGW`) to handle inbound/outbound internet traffic for the public subnet and deployed a managed NAT Gateway (`Lab NAT gateway`) with an Elastic IP to grant private subnet resources secure outbound-only internet connectivity.
* **Bastion Architecture:** Launched a jump box (`Bastion Server`) in the public subnet to establish a secure, controlled access point into the isolated `Private Instance` using SSH.

## 🖼️ Lab Evidence

### 1. Subnet Segmentation
Verified the allocation of public (`10.0.0.0/24`) and private (`10.0.2.0/23`) subnet ranges within `Lab VPC`.
![Subnets Overview](02-subnets-overview.png)

---

### 2. Public Network Routing
Configured `Public Route Table` with an explicit route targeting `Lab IGW` (`0.0.0.0/0`) associated with `Public Subnet`.
![Public Route Table](03-public-route-table.png)

---

### 3. Private Network Routing
Configured `Private Route Table` with a default route (`0.0.0.0/0`) targeting `Lab NAT gateway`.
![NAT Gateway Route](04-nat-gateway-route.png)

---

### 4. Bastion Host Connection
Established an SSH terminal session jumping from the public `Bastion Server` into the isolated `Private Instance`.
![Bastion Private SSH Session](05-bastion-private-ssh.png)

---

### 5. Outbound Connectivity Verification
Verified successful egress internet communication from the private instance through the NAT Gateway via HTTP header request (`curl -I https://aws.amazon.com`).
![Outbound NAT Connectivity Success](06-nat-ping-success.png)

## 🛠️ Operational Intelligence (Troubleshooting)
* **Real-World Challenge:** Initial connectivity verification from the private EC2 instance failed when testing outbound internet traffic via `ping amazon.com`, showing 100% packet loss despite the NAT Gateway being in an `Available` state.
* **Engineering Resolution:** Identified that while the Private Route Table had a `0.0.0.0/0` route pointing to the NAT Gateway, the `Private Subnet` itself had not been explicitly associated with the table, causing traffic to default to the main route table. Executed an explicit subnet association fix and verified outbound reachability via HTTP header inspect (`curl -I https://aws.amazon.com`), which returned an `HTTP/2 200` success response.
* **"What If" Scenario:** In a multi-AZ enterprise production deployment, I would deploy redundant NAT Gateways across multiple Availability Zones to prevent a single AZ failure from severing outbound internet connectivity for private workloads, combined with strict AWS Network Firewall rules to inspect outbound payload traffic.

## 📊 Technical Competence
* **Demonstrated Skills:** Custom VPC Design, Network Subnetting (CIDR), Route Table Engineering, NAT & Internet Gateway Deployment, Bastion Architecture, and Network Traffic Troubleshooting.
