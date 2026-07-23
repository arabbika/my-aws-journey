# ◈ AWS Networking - Core IP Addressing & Routing Protocols
**Course IDs**: `261-[NF]-Lab` & `262-[NF]-Lab`

## 🎯 Project Goal
The goal of these combined labs was to gain hands-on experience diagnosing, troubleshooting, and configuring IPv4 address schemes within Amazon VPC environments. Acting as an AWS Cloud Support Engineer, I resolved two distinct customer tickets: investigating asymmetrical public/private instance reachability across subnets and remediating broken services caused by dynamic IP changes across EC2 restart cycles.

## ⚙️ How it Works
* **Public vs. Private IP Routing (`261-[NF]-Lab`)**:
  * **Instance Auditing**: I evaluated two EC2 instances in a VPC. I discovered `Instance A` was trapped inside the private network space because it was only assigned an RFC 1918 Private IP, whereas `Instance B` possessed a routable Public IP.
  * **Command Line Access**: Using native Windows CLI (OpenSSH), I confirmed direct SSH reachability to `Instance B` via port 22, while verifying that instances lacking public IPs cannot establish direct inbound/outbound internet routes.
  * **VPC CIDR Architectural Review**: I analyzed why public IP blocks (such as `12.0.0.0/16`) should never be used as internal VPC CIDR ranges due to severe routing overlap and packet drop issues.

* **Static vs. Dynamic IP Addressing (`262-[NF]-Lab`)**:
  * **Issue Replication**: I launched an EC2 instance configured with Auto-assign Public IP enabled. Stopping and starting the virtual server proved that default public IPs are dynamic—AWS releases them back to the global IP pool upon shutdown, causing connected applications to break.
  * **Elastic IP (EIP) Allocation**: I allocated an AWS Elastic IP (a static IPv4 address reserved for the AWS account) and associated it directly with the instance's network interface (ENI).
  * **Persistence Validation**: I performed full stop/start power cycles on the EC2 instance to verify that the Elastic IP remained permanently bound to the server across reboots.

## 📷 Lab Evidence

### Part 1: Public and Private IP Addresses (`261-[NF]-Lab`)
| Task | Description | Evidence |
| :--- | :--- | :--- |
| **1** | Instance A Details (Private IPv4 Only) | ![Instance A Details](/my-aws-journey/01_Labs/02_Networking/images/01-instance-a-networking-details.png) |
| **1** | Instance B Details (Public & Private IPv4) | ![Instance B Details](/my-aws-journey/01_Labs/02_Networking/images/02-instance-b-networking-details.png) |
| **2** | Instance A Reachability/Key Failure | ![Instance A Failure](/my-aws-journey/01_Labs/02_Networking/images/03-instance-a-ssh-failure.png) |
| **2** | Instance B Windows CLI SSH Connection Success | ![Instance B Success](/my-aws-journey/01_Labs/02_Networking/images/04-instance-b-ssh-success.png) |

### Part 2: Static and Dynamic IP Addresses (`262-[NF]-Lab`)
| Task | Description | Evidence |
| :--- | :--- | :--- |
| **1** | Initial Dynamic Public IP (Running State) | ![Dynamic Initial](/my-aws-journey/01_Labs/02_Networking/images/01-dynamic-ip-initial-running.png) |
| **1** | Dynamic Public IP Changed After Restart | ![Dynamic Changed](/my-aws-journey/01_Labs/02_Networking/images/02-dynamic-ip-changed-after-restart.png) |
| **1** | Elastic IP Allocation & Association | ![EIP Association](/my-aws-journey/01_Labs/02_Networking/images/03-elastic-ip-associated.png) |
| **1** | Static Elastic IP Persisted After Restart | ![Static Persisted](/my-aws-journey/01_Labs/02_Networking/images/04-static-ip-persisted-after-restart.png) |

## 🛠️ Lessons Learned & Optimization
* **The Auto-Assign Public IP Trap**: Auto-assigned public IPv4 addresses are ephemeral. They are tied directly to the lifecycle of the underlying EC2 hypervisor session. Stopping an instance returns its public IP to the AWS pool, meaning hardcoded IP configurations in external applications or DNS records will break instantly upon instance restart.
* **Persistent Addressing via Elastic IPs**: To achieve static public addressing without risking IP changes during maintenance windows, an Elastic IP (EIP) must be allocated. EIPs stay locked to your AWS account and remain bound to the assigned Elastic Network Interface (ENI) regardless of how many times the EC2 instance stops or starts.
* **Key Propagation Across Subnets**: Attempting an SSH hop from a public instance (`Instance B`) to a private instance (`Instance A`) failed because private key files (`.pem`) stay on the local client machine by default. Secure administrative access to private subnets requires Bastion Hosts with SSH agent forwarding or utilizing AWS Systems Manager (SSM) Session Manager to avoid exposing SSH keys altogether.
* **VPC CIDR Design Integrity**: Never use public IPv4 spaces (e.g., `12.0.0.0/16`) for VPC CIDR ranges. Because routers prioritize local subnets first, any external public website or service hosted on the true `12.x.x.x` internet space will become completely unreachable from within the VPC. Always stick strictly to RFC 1918 private ranges (`10.0.0.0/8`, `172.16.0.0/12`, `192.168.0.0/16`).

## 📊 Technical Competence
Amazon VPC Networking, Public vs. Private IPv4 Routing, Ephemeral vs. Static IP Lifecycles, Elastic IP (EIP) Allocation & Association, OpenSSH Command Line Troubleshooting, RFC 1918 Addressing Standards, Cloud Infrastructure Security.
