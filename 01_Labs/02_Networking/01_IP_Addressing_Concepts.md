# ◈ Networking Protocol Fundamentals
**Course ID**: `261/262-[NF]-Lab`

## 🎯 Network Objective
This lab focused on mastering IP addressing schemes in a cloud environment. The objective was to diagnose connectivity issues stemming from misconfigured IP types and to implement persistent addressing solutions to ensure high availability for production workloads.



## 🚦 Traffic & Flow Logic
* **Addressing Strategy:** Analyzed internal vs. external traffic requirements. Identified that instances requiring internet access need a Public IP/NAT, while internal-only resources remain secured within a private CIDR block.
* **Protocol Implementation:** * **Dynamic:** Configured standard instance provisioning where public IPs are assigned dynamically via DHCP at launch (and change upon reboot).
    * **Static:** Resolved "configuration drift" by implementing **Elastic IPs (EIP)**, providing a static, persistent public endpoint that survives instance stop/start cycles.

## 📷 Lab Evidence
| Task | Connectivity Check | Evidence |
| :--- | :--- | :--- |
| **1** | Public vs. Private IP Verification | ![IP_Audit](./images/261_262_IP_Verification.png) |
| **2** | Dynamic IP Fluctuation (Stop/Start) | ![DHCP_Change](./images/261_262_DHCP_Status.png) |
| **3** | Elastic IP (EIP) Association | ![EIP_Config](./images/261_262_EIP_Association.png) |

## 🛠️ Troubleshooting (The "Ping" Mindset)
* **Connectivity Roadblock:** Customer reported that their application "broke" every time an instance was restarted due to changing IP addresses.
* **Diagnostic Steps:** Replicated the issue by stopping and starting a test instance, observing the public IPv4 address change. Verified that the instance had no Elastic IP assigned.
* **Resolution:** Allocated an EIP from the AWS pool and associated it with the target instance, ensuring a static, reliable ingress point for the customer's resources.

## 📊 Technical Competence
* **Skills:** VPC Architecture, CIDR Calculation, Dynamic Host Configuration Protocol (DHCP) Analysis, Elastic IP Lifecycle Management, Route Table/Gateway Verification.
