# Ashana Rabbikanth | Data, Business Analysis & AI

<div align="center">

**Business Systems Analyst | Data Analytics | AI Solutions**  
*Turning operational complexity into clear data, automated workflows, and practical AI tools.*

[![AWS Certified AI Practitioner](https://img.shields.io/badge/AWS-Certified%20AI%20Practitioner-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://www.credly.com/badges/04e4b5a6-37fc-450c-86fa-c010f89fd9b4)
[![Open to Work](https://img.shields.io/badge/💼-Open%20to%20Data%20%26%20BA%20Roles-2EA44F?style=for-the-badge)]()
[![Location](https://img.shields.io/badge/📍-Durban%2C%20South%20Africa%20%7C%20Remote-0078D4?style=for-the-badge)]()

<br />

[![About](https://img.shields.io/badge/About-0078D4?style=for-the-badge&logo=aboutdotme&logoColor=white)](#-about-me)
[![Skills](https://img.shields.io/badge/Skills-2EA44F?style=for-the-badge)](#-core-skills)
[![Projects](https://img.shields.io/badge/Projects-FF9900?style=for-the-badge&logo=github&logoColor=white)](#-featured-projects)
[![Certifications](https://img.shields.io/badge/Certifications-E50914?style=for-the-badge&logo=credly&logoColor=white)](#-certifications)
[![Labs](https://img.shields.io/badge/Labs-8A2BE2?style=for-the-badge&logo=jupyter&logoColor=white)](#-learning-lab-aws-restart)
[![Connect](https://img.shields.io/badge/Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](#-connect-with-me)

</div>

---

## 👤 About Me

I'm a **Business Systems Analyst and Data Specialist** with a proven record of turning messy operational data into dashboards, models, and automations that people actually use. My background spans banking systems, customer analytics, and enterprise operations — and I'm now extending that foundation with hands-on **AI and cloud data tooling** through AWS re/Start and AWS AI Practitioner certification.

### What I Bring

| Domain | Experience & Impact |
|--------|---------------------|
| **Business Analysis** | Requirements gathering, process improvement, stakeholder management, and KPI reporting across banking and enterprise operations. |
| **Data Analytics** | Built customer segmentation and cross-sell models at Liberty Group on a 50K-record base. Delivered 150+ freelance data, reporting, and automation projects across 4 countries. |
| **Operations & Reporting** | Designed a 4-week rolling **Performance Scorecard** adopted by 200+ agents across 10 Amazon VCS teams. Top 5% network performer for FCR, ACHT, and Quality across 60 months. |
| **Automation** | Built Python and Excel automation tools that cut clients' manual reporting time by an average of **60%**. |
| **AI Solutions** | Lead developer of live AI products including **HiRiseAboveBot** (WhatsApp AI tutor, 200+ users) |

### Currently Learning
- 🔄 **AWS re/Start** – Cloud Practitioner track (expected 2026) — building data-relevant cloud skills: S3, DynamoDB, Lambda, IAM, and serverless data pipelines
- 🔄 **Amazon Bedrock & Generative AI** – Prompt engineering, guardrails, and LLM-backed assistants
- 🔄 **SQL & Python for Analytics** – Continuing applied practice through hands-on labs

---

## 🧩 Core Skills

**Data & Analytics**  
`SQL` `Python` `Data Mining` `Custom Reporting` `Customer Segmentation` `Cross-Sell Modelling`

**Business Analysis**  
`Requirements Gathering` `Process Improvement` `Stakeholder Management` `KPI Reporting` `User Training & Onboarding`

**Excel & Data Modelling**  
`Power Query (ETL)` `Power Pivot` `DAX` `Dynamic Arrays` `XLOOKUP` `Slicer Dashboards`

**AI & Automation**  
`Generative AI` `LLM APIs (xAI Grok, Bedrock/Claude)` `Prompt Engineering` `Tesseract OCR` `Twilio API` `Flask`

**Cloud & Systems (supporting)**  
`AWS S3` `DynamoDB` `Lambda` `Cognito` `SNS` `SAP Bank Analyzer` `Core Banking Configuration`

**Compliance & Domain Knowledge**  
`Basel II` `NCA` `IAS` `Banking Systems` `Escalation Management` `FCR & ACHT Optimisation`

---

## 🚀 Featured Projects

> 📁 **[Browse Full Projects Directory →](./00_Projects)**

### 📊 Performance Scorecard — Amazon VCS
**Stack:** `Excel` `Power Query` `DAX` `Data Modelling`

Designed and built a 4-week rolling performance dashboard that consolidated key operational metrics into a single self-coaching view for agents. Rolled out to **200+ agents across 10 VCS teams**.

**Impact:**
- Enabled agent self-coaching and reduced manager reporting overhead
- Contributed to top 5% network ranking for FCR, ACHT, and Quality across 60 months
- Adopted as a standard reporting tool across multiple teams

---

### 🤖 HiRiseAboveBot — WhatsApp AI Tutor
**Stack:** `Python` `Flask` `xAI Grok-4` `Tesseract OCR` `Twilio API` `gTTS`

Live production AI tutoring platform serving CAPS/IEB students in low-bandwidth communities. No app needed — works entirely through WhatsApp.

**Features:**
- 📸 OCR processing for photographed questions
- 📐 Dynamic LaTeX math rendering
- 🔊 Generated audio lessons via gTTS
- 📱 200+ students on free trial

**Impact:** Digital inclusion for students with limited data access.

---

### 🌍 Global 3D E-Commerce Platform — Architecture & Business Case
**Stack:** `Route 53` `CloudFront` `WAF & Shield` `EC2 Auto Scaling` `Lambda` `EventBridge` `Aurora Global Database` `DynamoDB Global Tables` `S3` `ElastiCache` `KMS`

*Team mini-project — AWS re/Start Cloud Architecture Mini Team*

Multi-region, active-active architecture for a 3D e-commerce platform selling **EcoFlow portable power and solar systems**, driven by **2026 El Niño** weather scenarios that create sudden, global traffic surges.

**Business Analysis Deliverables:**
- Commercial case tying architecture decisions to real weather-driven demand
- Full **cost-benefit analysis** (CapEx → OpEx, auto-scaling, edge caching, serverless)
- Documented **architectural trade-offs** (multi-region active-active vs. consistency; serverless vs. EC2)
- Mapped against all six **AWS Well-Architected pillars**
- **El Niño stress-test scenario** with proactive peak-season recommendations

**Architecture Highlights:**
- **Edge:** Route 53 latency routing + health-check failover, CloudFront (90%+ static hit rate on 50MB+ manuals), WAF bot defense for scalper protection
- **Compute:** EventBridge + Lambda **pre-warming** from weather alert APIs; EC2 Auto Scaling across 2 AZs in 2 active regions
- **Data:** Aurora Global Database (primary writer / failover), DynamoDB Global Tables (active-active writes), ElastiCache in both regions

[📐 View Full Architecture & Business Case →](./00_Projects/Project_2_Global_3D_Ecommerce_Architecture/README.md)

---

### 🧠 Aura AI — Life & Task Co-Pilot
**Stack:** `AWS PartyRock` `Amazon Bedrock` `Claude Sonnet`

Multi-block generative AI application designed to neutralize cognitive gridlock through prompt-chained sequential blocks: role analysis, zero-stress game planning, and somatic grounding.

[🔗 View Live App](https://github.com/arabbika/my-aws-journey/tree/21bc4bd30e348944001e9e0927b3b76245527dfc/01_Labs/10_Machine%20Learning%20And%20Generative%20AI/aws-partyrock-aura-copilot)

---

### ☁️ AWS Cloud Migration Proposal
**Stack:** `S3` `Cognito` `DynamoDB` `Lambda` `SNS`

Serverless architecture proposal to transform manual operational workflows — delivered static hosting, authentication, and event-driven notifications. Demonstrated a **30% potential reduction** in operational costs through automation.

---

## 🏆 Certifications

### Official AWS Certifications
*Click badge to verify on Credly*

<table>
  <tr>
    <td align="center" width="200">
      <a href="https://www.credly.com/badges/04e4b5a6-37fc-450c-86fa-c010f89fd9b4" target="_blank">
        <img src="./Certifications/AWS%20Certified%20AI%20Practitioner%20Badge.png" width="140" alt="AWS Certified AI Practitioner" />
      </a>
      <br /><br />
      <b>AWS Certified AI Practitioner</b>
      <br />
      <sub>Issued: 2026</sub>
    </td>
  </tr>
</table>

### AWS Microcredentials
*Click badges to verify*

<table>
  <tr>
    <td align="center" width="200">
      <a href="https://www.credly.com/badges/e9eef2ce-df12-41ef-abce-202dec02ffab" target="_blank">
        <img src="./Certifications/Cloud%20Practitioner%20-%20Microcredential%20Training%20Badge.png" width="130" alt="AWS Cloud Quest Training" />
      </a>
      <br /><br />
      <b>Cloud Practitioner</b>
      <br />
      <sub>AWS Cloud Quest Training</sub>
    </td>
    <td align="center" width="200">
      <a href="https://www.credly.com/badges/bc7e00b8-6752-4c2a-aaf7-3bc0b1f48e71/public_url" target="_blank">
        <img src="./Certifications/AI%20Practitioner%20-%20Microcredential%20Training%20Badge.png" width="130" alt="AWS SimuLearn AI Practitioner" />
      </a>
      <br /><br />
      <b>AI Practitioner</b>
      <br />
      <sub>AWS SimuLearn Training</sub>
    </td>
  </tr>
</table>

### Additional Training
| Certificate | Provider |
|-------------|----------|
| Statistical Thinking for Data Science | ColumbiaX (edX) |
| Leadership: Foundational Principles | HarvardX (edX) |
| Diploma in Programming | Damelin Computer School |

---

## 🧪 Learning Lab (AWS re/Start)

> 📁 **[Explore All Lab Directories →](./01_Labs)**

Hands-on labs completed as part of my **AWS re/Start Cloud Practitioner track** (expected 2026). These labs build the cloud data and AI skills that support my analytics and business analysis work — covering storage, databases, security, and generative AI tooling.

### AWS Cloud Practitioner SimuLearn
| Module | Module |
|--------|--------|
| [Cloud Computing Essentials](./Certifications/Cloud%20Computing%20Essentials.png) | [Cloud Economics](./01_Labs/04_Compute/AWS_SimuLearn_Cloud_Economics.md) |
| [Cloud First Steps](./01_Labs/04_Compute/AWS_SimuLearn_Cloud_First_Steps.md) | [Computing Solutions](./01_Labs/04_Compute/AWS_SimuLearn_Computing_Solutions.md) |
| [Connecting VPCs](./01_Labs/02_Networking/AWS_SimuLearn_Connecting_VPCs.md) | [Core Security Concepts](./01_Labs/03_Security/AWS_SimuLearn_Core_Security_Concepts.md) |
| [Databases in Practice](./Certifications/Databases%20in%20Practice.png) | [File Systems in the Cloud](./01_Labs/05_Storage%20and%20Archiving/AWS_SimuLearn_File_Systems_in_the_Cloud.md) |
| [First NoSQL Database](./01_Labs/06_Databases/AWS_SimuLearn_First_NoSQL_Database.md) | [Highly Available Web Applications](./01_Labs/02_Networking/AWS_SimuLearn_Highly_Available_Web_Applications.md) |
| [Networking Concepts](./01_Labs/02_Networking/AWS_SimuLearn_Networking_Concepts.md) | |

### AWS AI Practitioner SimuLearn
| Badge | Badge |
|-------|-------|
| [Build Code with Amazon Q](./Certifications/Build%20and%20Understand%20Code%20with%20Amazon%20Q.png) | [Create an AI Smart Assistant](./Certifications/Create%20an%20AI%20Smart%20Assistant.png) |
| [Create Enterprise Knowledge Assistant](./Certifications/Create%20an%20Enterprise%20Knowledge%20Assistant.png) | [Explore Bedrock Playgrounds](./Certifications/Explore%20the%20Amazon%20Bedrock%20Playgrounds.png) |
| [Generate Code for a Webpage](./Certifications/Generate%20Code%20for%20a%20Webpage.png) | [Get Started with Generative AI](./Certifications/Get%20Started%20with%20Generative%20AI.png) |
| [Secure Conversational AI with Guardrails](./Certifications/Secure%20Conversational%20AI%20with%20Guardrails.png) | [Use AI services with SageMaker](./Certifications/Use%20AI%20services%20with%20Amazon%20SageMaker.png) |

### Lab Domains Covered
| Domain | Relevance |
|--------|-----------|
| **Databases** | RDS, Aurora, DynamoDB — query and model data in cloud environments |
| **Storage** | S3, EBS, EFS — structuring and managing data at scale |
| **Security** | IAM, least privilege, data protection — governance for sensitive data |
| **AI/ML** | Bedrock, SageMaker — building AI data applications |
| **Compute & Serverless** | Lambda — automating data workflows |
| **Networking & Monitoring** | VPC, CloudWatch — observability for data pipelines |

---

## 🗂️ Repository Structure

```text
📂 my-aws-journey/
│
├── 📁 Certifications/     # Verified badges and certificates
├── 📁 01_Labs/            # Hands-on labs (AWS re/Start track)
│   ├── 02_Networking/
│   ├── 03_Security/
│   ├── 04_Compute/
│   ├── 05_Storage and Archiving/
│   ├── 06_Databases/
│   ├── 10_Machine Learning And Generative AI/
│   └── ...
├── 📁 00_Projects/        # Portfolio projects
│   ├── Project_1_Building_a_Static_Website/
│   ├── Project_2_Global_3D_Ecommerce_Architecture/
│   └── HiRiseAboveBot/
└── 📄 README.md           # Portfolio overview
