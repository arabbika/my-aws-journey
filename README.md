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
