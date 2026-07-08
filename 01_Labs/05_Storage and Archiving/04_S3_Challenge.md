# ◈ S3 Advanced Storage Challenge
**Course ID**: `184-[JAWS]-Lab`

## 🎯 Project Goal
The goal of this lab was to dive deeper into the practical administration of Amazon S3. I practiced managing object permissions, interacting with storage buckets directly through the command line interface, and auditing access controls to balance security with data availability.


## ⚙️ How it Works
Access Control Management: I worked with both bucket-level configurations and object-level permissions to understand the difference between keeping a storage bucket private while hosting specific public files.

CLI Storage Operations: I bypassed the AWS Management Console entirely to interact with the S3 API directly via the terminal, practicing efficient object uploads, listing directory contents, and auditing my storage resources from the command line.

Permission Isolation: I explored how AWS handles access hierarchies, validating how bucket-level restrictions interact with individual object permissions.

s3 cp or bucket control panel to successfully upload web assets to the bucket.awsweb1.PNG $\rightarrow$ Rename to 03_Web_Access.png: The final verification window showing the publicly readable item loaded over standard HTTP web addresses.

## 📷 Lab Evidence

| Task | Optimization Metric | Evidence |
| :---: | :--- | :--- |
| **1** | Bucket Provisioning & Object Upload | ![S3 Resource Configuration](images/01_S3_Config.png) |
| **2** | Object-Level Public Access Configuration | ![CLI Object Upload Success](images/02_Object_Upload.png) |
| **3** | CLI-based Resource Auditing | ![Web URL Access Validation](images/03_Web_Access.png) |

## 🛠️ Lessons Learned
The Object-Level 403 Forbidden Hurdle: After setting up my bucket, I tried to view an uploaded image in my browser using its object URL and immediately ran into a 403 "Forbidden" error. I realized that making a bucket accessible doesn't automatically mean its contents are public. I had to explicitly apply object-level Access Control Lists (ACLs) to grant public read permissions, which fixed the browser error instantly.

The CLI Speed Advantage: Uploading files one by one through a browser dashboard is incredibly tedious. Learning to use aws s3 cp and aws s3 ls showed me how easy it is to manage large amounts of cloud storage programmatically right from my local terminal workflow.

Designing with Production Security in Mind: In a real-world enterprise environment, relying on object-level public ACLs is highly discouraged because it makes it too easy to accidentally leak data. For a production site, I would activate S3 Block Public Access (BPA) at the account level to lock down the bucket completely, and instead use an S3 Bucket Policy to securely serve files globally through a CloudFront distribution using Origin Access Control (OAC).

## 📊 Technical Competence
Amazon S3 Bucket Architecture, AWS CLI Interaction (aws s3), Access Control Lists (ACLs), Public vs. Private Data Isolation, AWS Cloud Security Principles.
