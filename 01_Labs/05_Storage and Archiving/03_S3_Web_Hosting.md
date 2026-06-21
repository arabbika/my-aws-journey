# ◈ Static S3 Web Hosting
**Course ID**: `170-[JAWS]-Activity`

## 🎯 Architectural Objective
This project demonstrates the efficiency of serverless, static web hosting. The objective is to leverage Amazon S3’s built-in hosting capabilities to deliver high-availability, low-cost static web content directly from object storage.

## ⚙️ Content & Delivery Logic
* **Bucket Configuration:** [E.g., "Configured S3 bucket for static website hosting, specifying the index document and error handling paths."]
* **Access Control:** [E.g., "Applied Bucket Policies to enable 'Public Read' access for website content while maintaining strict object ownership and security."]

## 📷 Lab Evidence
| Task | Delivery Check | Evidence |
| :--- | :--- | :--- |
| **1** | Bucket Creation & Website Enablement | ![S3_Config](./images/170_S3_Hosting_Setup.png) |
| **2** | Object Upload & Permission Audit | ![Object_Upload](./images/170_S3_Object_Upload.png) |
| **3** | Browser-Based Connectivity Test | ![Web_Access](./images/170_S3_Web_Result.png) |

## 🛠️ Operational Intelligence
* **Challenge:** [E.g., "Accessing the bucket URL returned a 403 'Forbidden' error despite the bucket appearing to be public."]
* **Engineering Resolution:** [How you fixed it: e.g., "Identified that 'Block Public Access' settings at the account level were overriding the bucket policy; disabled the specific block and validated the policy JSON syntax."]
* **"What If" Scenario:** [In a production system, I would place a CloudFront distribution in front of this S3 bucket to implement HTTPS, use Origin Access Control (OAC), and cache content at edge locations to improve global performance.]

## 📊 Technical Competence
* **Demonstrated Skills:** S3 Bucket Configuration, Static Website Hosting, Bucket Policy Management, Public Access Control (BPA), Content Delivery Concepts.
