# ◈ Build Your VPC and Launch a Web Server
**Course ID**: `267-[NF]-Lab`

## 🎯 Project Goal
Designing and deploying a multi-tier, high-availability network architecture using Amazon Virtual Private Cloud (VPC), complete with public and private subnets, security group firewalls, and an automated web server deployment on Amazon EC2.

---

## ⚙️ Technical Implementation

### 1. VPC & Subnet Architecture
* **Virtual Private Cloud:** Provisioned `Lab VPC` (`10.0.0.0/16`) to create an isolated logical network space.
* **Subnet Layout:** Built a dual-Availability Zone network topology with strict traffic segmentation across four subnets:
  * `Public Subnet 1` (`10.0.0.0/24`) & `Public Subnet 2` (`10.0.2.0/24`)
  * `Private Subnet 1` (`10.0.1.0/24`) & `Private Subnet 2` (`10.0.3.0/24`)
* **Routing & NAT:** Configured `Public Route Table` attached to an Internet Gateway for public-facing resources, and explicit associations for `Private Route Table` utilizing a NAT Gateway for secure outbound connectivity.

![VPC Creation](267%2001_vpc_creation%20.png)
*Figure 1: Successful provisioning of Lab VPC.*

![Subnet Creation](267%2002_subnet_creation.png)
*Figure 2: Subnet configuration across multiple Availability Zones.*

### 2. Security & Firewall Configuration
* **Security Group:** Built `Web Security Group` acting as a stateful virtual firewall assigned directly to the web instance.
* **Inbound Rules:** Configured rule `sgr-0e55b78c536883434` allowing inbound HTTP (Port 80) traffic from anywhere (`0.0.0.0/0`) to accept web requests.

![Security Group Rules](267%2003_security_group_rules.png)
*Figure 3: Inbound HTTP rule configuration for Web Security Group.*

### 3. Automated Web Server Provisioning
* **Compute:** Provisioned a `t3.micro` instance running Amazon Linux 2 (`Web Server 1`) into `Public Subnet 2` with an auto-assigned public IP.
* **Bootstrapping (User Data):** Automated package installation and service management at initial boot using the shell script:

```bash
#!/bin/bash
# Install Apache Web Server and PHP
yum install -y httpd mysql php
# Download Lab files
wget [https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-100-RESTRT-1/267-lab-NF-build-vpc-web-server/s3/lab-app.zip](https://aws-tc-largeobjects.s3.us-west-2.amazonaws.com/CUR-TF-100-RESTRT-1/267-lab-NF-build-vpc-web-server/s3/lab-app.zip)
unzip lab-app.zip -d /var/www/html/
# Turn on web server
chkconfig httpd on
service httpd start

```

![Web Server Test Success](267%20web_server_test_success.png)
*Figure 4: Successful HTTP connection to the web server via public IP (`52.11.158.35`).*

🛠️ Operational Intelligence (Troubleshooting)
Real-World Challenge: Ensuring proper network pathing so that instances in public subnets are reachable externally while internal subnets remain completely private.

Engineering Resolution: Verified explicit subnet route table associations, confirmed that auto-assigning public IP addresses was enabled on Public Subnet 2, and checked that the Web Security Group explicitly permitted port 80 traffic.

"What If" Scenario: In a production setting, placing web servers directly in public subnets exposes them to potential targeted attacks. I would deploy an Application Load Balancer (ALB) in the public subnets to accept incoming web traffic and place the backend EC2 web servers inside private subnets, routing traffic internally for enhanced network defense.

📊 Technical Competence
Demonstrated Skills: Virtual Private Cloud (VPC) Design, Multi-AZ Subnet Partitioning, Route Table Customization, Stateful Firewall Management (Security Groups), Automated EC2 Bootstrapping (User Data), and Web Infrastructure Verification.
