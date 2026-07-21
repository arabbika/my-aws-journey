# AWS Cloud Migration Proposal & Pre-Deployment Architectural Handover

> **Project:** AWS Serverless Migration for Shisanyama Operational Ecosystem  
> **Lead Presenter:** Solutions Architect & Delivery Lead  
> **Audience:** Executive Board of Directors (MD & CFO)  
> **Status:** Production-Ready / Handover Stage  

---

## 📋 Executive Briefing

Welcome, members of the Board of Directors. As your Lead Cloud Solutions Consultants, we are delivering the production-ready technical architecture designed to turn unstructured manual operational hurdles—such as lost double-bookings and kitchen friction—into scalable, high-performing digital business assets.

---

## 🔴 1. The Business Problem: Operational Bottlenecks

Evaluating standard on-premises manual limitations:

* **Manual Dependency:** Total reliance on fragile physical paper ledger records or a single standalone localized administrative computer terminal prone to physical damage.
* **Order Mix-Ups:** Frequent manual tracking mistakes resulting directly in kitchen order mix-ups, missing ticket items, and disruptive double-booked reservation slots.
* **Siloed Customer Data:** Complete lack of a centralized datastore, making it impossible to securely save repeat customer preferences or issue formal order confirmations.
* **Inability to Scale:** Expanding processing capacity requires high physical staffing expenditures or local compute hardware upgrades instead of fluid automation.

---

## 🎥 2. Media Pitch Briefing (Embedded Video Demo)

Below is the embedded presentation video pitch showcasing the conceptual transformation from manual limitations directly into a managed AWS serverless environment:

<video controls width="100%" poster="" style="border-radius: 8px; border: 1px solid #2a2a30;">
    <source src="00_Projects/00_Project_1_Building_a_Static_Website_and_Presenting_AWS_Migration_Benefits/2026-07-13 16-10-32 Compressed.mp4" type="video/mp4">
    Your browser does not support HTML5 video tags.
</video>

> **Note:** Replace `C:\Users\ashanar\Downloads\HG - Trim.mp4` with your relative local or remote video repository path (e.g., `./assets/HG-Trim.mp4`) when deploying to hosting platforms like GitHub or GitLab.

---

## ⚡ 3. Technical Solution & Cloud Ecosystem

Transitioning localized legacy bottlenecks into a highly available ecosystem of modern managed cloud service components to ensure platform auto-scaling and continuous availability:

| Service Component | Cloud Architecture Mapping & Implementation |
| :--- | :--- |
| **Amazon S3** | Eliminates localized frontend dependencies by hosting web code and high-availability digital menu graphics across globally distributed endpoints. |
| **AWS Cognito** | Removes authentication burdens by checking client logins automatically and generating secure data tokens for transaction validation. |
| **Amazon RDS / DynamoDB** | Provides a central database instance to record real-time seating availability logs and client historic choices, replacing vulnerable physical paper ledgers. |
| **AWS Lambda & SNS** | Introduces event-driven processing engines to handle messaging updates and order print notifications without maintaining permanent compute servers. |

---

## 💻 4. Interactive Portal Features & Execution Pipeline

The proposed frontend interface replaces manual ingestion pipelines with a high-contrast web portal layout built with accessible, clean components to handle secure consumer processing paths:

```text
[01 AWS Cognito Sign-In] ➔ [02 Menu Display] ➔ [03 Booking & Order Forms] ➔ [04 Confirmation Page]
