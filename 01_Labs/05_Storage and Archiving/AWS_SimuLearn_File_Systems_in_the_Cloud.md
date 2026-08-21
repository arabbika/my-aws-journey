# ☁️ AWS SimuLearn: File Systems in the Cloud

## 🎯 Objective
Configure and deploy Amazon Elastic File System (EFS) to deliver shared, highly available network file storage across multi-AZ EC2 web server fleets. Demonstrate POSIX file compliance and real-time cross-instance file sync using Session Manager terminal instances.

---

## 🏗️ Architecture & Configuration
* **Storage Service:** Amazon EFS (Elastic File System)
* **Compute Services:** Amazon EC2 Instances (`WebServer1`, `WebServer2`, `WebServer3`)
* **VPC & Network Infrastructure:** `PetModels VPC` spanning Availability Zones `us-east-1a`, `us-east-1b`, and `us-east-1c`
* **Network Security:**
  * **Target SG:** `PetModels-EFS-1-SG`
  * **Inbound Rule:** NFS Protocol (Port 2049) restricted specifically to the source `Web_Server_SG` security group

---

## 🛠️ Key Implementation Steps
1. **Security Isolation:** Provisioned custom network security group `PetModels-EFS-1-SG` with restrictive inbound NFS rules bound to the web server tier.
2. **EFS File System Creation:** Deployed `PetModels-EFS-1` with Bursting throughput, disabling automatic backups and lifecycle storage class transitions for optimized lab deployment.
3. **Multi-AZ Mount Targets:** Established dedicated EFS Mount Targets across all subnets (`us-east-1a`, `us-east-1b`, and `us-east-1c`) within the `PetModels VPC`.
4. **Client-Side Mounting:** Used AWS Systems Manager Session Manager to install `amazon-efs-utils` on EC2 nodes and mount the EFS endpoint onto `/data` mount points using TLS encryption.
5. **Cross-Instance File Consistency (DIY Task):** Configured `WebServer3` in `us-east-1c` with mount access, writing real-time concurrent log entries to verify shared storage access across all three availability zones.

---

## 💡 Key Architectural Takeaway
Unlike Amazon EBS block storage (which is locked to a single Availability Zone), Amazon EFS is a regional NFS service that spans multiple AZs by default. By attaching EFS Mount Targets to each subnet and controlling access via security groups, distributed web server fleets achieve seamless, concurrent read/write file access without managing underlying storage infrastructure.

---

## 📜 Certification & Verification

<p align="center">
  <a href="https://github.com/arabbika/my-aws-journey/blob/main/Certifications/File%20Systems%20in%20the%20Cloud.png" target="_blank">
    <img src="https://raw.githubusercontent.com/arabbika/my-aws-journey/main/Certifications/File%20Systems%20in%20the%20Cloud.png" alt="AWS SimuLearn - File Systems in the Cloud Badge" width="350" />
  </a>
</p>
