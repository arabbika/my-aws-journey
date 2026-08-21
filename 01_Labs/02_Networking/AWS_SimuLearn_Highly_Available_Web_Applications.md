# ⚡ AWS SimuLearn: Highly Available Web Applications

## 🎯 Objective
Architect and deploy a fault-tolerant, highly available web application architecture across three Availability Zones using an Application Load Balancer (ALB), Target Group health checks, dynamic Auto Scaling Groups (ASG), and multi-tiered Security Group authorization.

---

## 🏗️ Architecture & Configuration
* **VPC:** `lab/TravelAgencyVpc`
* **Compute & Scaling:**
  * **Auto Scaling Group:** `TravelAgencyWebServers` (Desired: 3 | Min: 3 | Max: 3) distributed across `PublicSubnet1` (us-east-1a), `PublicSubnet2` (us-east-1b), and `PublicSubnet3` (us-east-1c)
* **Traffic Routing & Load Balancing:**
  * **Application Load Balancer:** `TravelAgencyServers-ALB` (Internet-facing)
  * **Target Group:** `TravelAgencyWebServer-TG`
  * **Custom Health Check Path:** `/health` (Threshold: 2 | Timeout: 2s | Interval: 5s)
* **Network Security & Firewalls:**
  * **ALB Security Group:** `TravelAgencyLoadBalancer` (Inbound HTTP 80 from `0.0.0.0/0`)
  * **EC2 Security Group:** `TravelAgencyWebServer` (Inbound HTTP 80 restricted strictly to `TravelAgencyLoadBalancer` Security Group ID)

---

## 🛠️ Key Implementation Steps
1. **Target Group & Custom Health Monitoring:** Created `TravelAgencyWebServer-TG` under `lab/TravelAgencyVpc` and configured custom health monitoring against the `/health` HTTP endpoint for rapid failure detection.
2. **Application Load Balancer Provisioning:** Deployed `TravelAgencyServers-ALB` across three distinct Availability Zones and mapped listeners to forward inbound public web traffic directly to the target group.
3. **Least-Privilege Security Hardening:**
   * Provisioned `TravelAgencyLoadBalancer` security group to accept internet HTTP requests.
   * Hardened `TravelAgencyWebServer` security group by restricting inbound HTTP traffic exclusively to the ALB's security group reference.
4. **Multi-AZ Auto Scaling Configuration:** Updated `TravelAgencyWebServers` ASG network settings to span subnets in all three Availability Zones and scaled desired capacity to 3 instances to ensure high availability and automatic auto-healing.

---

## 💡 Key Architectural Takeaway
High availability requires removing single points of failure at both the routing and compute layers. Decoupling incoming user traffic using an Application Load Balancer combined with an Auto Scaling Group spanning three Availability Zones guarantees seamless failure recovery and load distribution. Restricting backend EC2 ingress directly to the ALB security group establishes a secure, least-privilege edge-to-backend network tier.

---

## 📜 Certification & Verification

<p align="center">
  <a href="https://github.com/arabbika/my-aws-journey/blob/main/Certifications/Highly%20Available%20Web%20Applications.png" target="_blank">
    <img src="https://raw.githubusercontent.com/arabbika/my-aws-journey/main/Certifications/Highly%20Available%20Web%20Applications.png" alt="AWS SimuLearn - Highly Available Web Applications Badge" width="350" />
  </a>
</p>
