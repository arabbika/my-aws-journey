# ◈ Static S3 Web Hosting
**Course ID**: `170-[JAWS]-Activity`

## 🎯 Architectural Objective
This project demonstrates the efficiency of serverless, static web hosting. The objective was to leverage Amazon S3’s built-in hosting capabilities to deliver high-availability, low-cost static web content, while implementing automated deployment scripts to streamline content updates.



## ⚙️ Content & Delivery Logic
* **Bucket Configuration:** Configured S3 for static website hosting, mapping the index document and enabling public access via modified Block Public Access (BPA) settings and ACLs.
* **Access Control:** Managed identity through IAM, attaching `AmazonS3FullAccess` policies to specific users to enable programmatic bucket administration.
* **Automated Deployment:** Developed a custom bash script (`update-website.sh`) using the AWS CLI to automate synchronization between local source files and the S3 bucket.

## 📷 Lab Evidence
| Task | Delivery Check | Evidence |
| :--- | :--- | :--- |
| **1** | Bucket Creation & Website Enablement | ![S3_Config](./images/170_S3_Hosting_Setup.png) |
| **2** | CLI-based Object Upload & IAM Audit | ![Object_Upload](./images/170_S3_Object_Upload.png) |
| **3** | Browser-Based Connectivity Test | ![Web_Access](./images/170_S3_Web_Result.png) |

## 🛠️ Operational Intelligence
* **Challenge:** Accessing the bucket website endpoint initially returned a 403 "Forbidden" error, despite the bucket being configured for public access.
* **Engineering Resolution:** Identified that account-level "Block Public Access" (BPA) settings were overriding bucket-level configurations. Disabled the specific BPA block and enabled ACLs to permit public read access, successfully validating the endpoint.
* **Efficiency Gains:** Transitioned from `aws s3 cp` to `aws s3 sync`. The `sync` command is significantly more efficient as it performs an incremental update, only uploading files that have changed (checksum-based) rather than re-uploading the entire directory, saving bandwidth and execution time.
* **"What If" Scenario:** In a production environment, I would place a **CloudFront** distribution in front of this S3 bucket. This would provide HTTPS encryption, support Origin Access Control (OAC) to ensure the bucket remains private (accessible only via CloudFront), and leverage global edge caching for faster content delivery.

## 📊 Technical Competence
* **Demonstrated Skills:** S3 Static Website Hosting, AWS CLI Automation (Shell Scripting), IAM Policy/User Management, ACLs & Bucket Policy configuration, Incremental Deployment Patterns (`s3 sync`).
