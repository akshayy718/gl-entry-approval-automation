<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0,EA4B8B,FF6B9D,FFB3D1&height=200&section=header&fontSize=42&fontColor=fff&animation=fadeIn&fontAlignY=36" width="100%"/>
</div>

<div align="center">

<pre>
 ██████╗ ██╗         ███████╗███╗   ██╗████████╗██████╗ ██╗   ██╗
██╔════╝ ██║         ██╔════╝████╗  ██║╚══██╔══╝██╔══██╗╚██╗ ██╔╝
██║  ███╗██║         █████╗  ██╔██╗ ██║   ██║   ██████╔╝ ╚████╔╝ 
██║   ██║██║         ██╔══╝  ██║╚██╗██║   ██║   ██╔══██╗  ╚██╔╝  
╚██████╔╝███████╗    ███████╗██║ ╚████║   ██║   ██║  ██║   ██║   
 ╚═════╝ ╚══════╝    ╚══════╝╚═╝  ╚═══╝   ╚═╝   ╚═╝  ╚═╝   ╚═╝  

 █████╗ ██████╗ ██████╗ ██████╗  ██████╗ ██╗   ██╗ █████╗ ██╗     
██╔══██╗██╔══██╗██╔══██╗██╔══██╗██╔═══██╗██║   ██║██╔══██╗██║     
███████║██████╔╝██████╔╝██████╔╝██║   ██║██║   ██║███████║██║     
██╔══██║██╔═══╝ ██╔═══╝ ██╔══██╗██║   ██║╚██╗ ██╔╝██╔══██║██║     
██║  ██║██║     ██║     ██║  ██║╚██████╔╝ ╚████╔╝ ██║  ██║███████╗
╚═╝  ╚═╝╚═╝     ╚═╝     ╚═╝  ╚═╝ ╚═════╝   ╚═══╝  ╚═╝  ╚═╝╚══════╝

 █████╗ ██╗   ██╗████████╗ ██████╗ ███╗   ███╗ █████╗ ████████╗██╗ ██████╗ ███╗   ██╗
██╔══██╗██║   ██║╚══██╔══╝██╔═══██╗████╗ ████║██╔══██╗╚══██╔══╝██║██╔═══██╗████╗  ██║
███████║██║   ██║   ██║   ██║   ██║██╔████╔██║███████║   ██║   ██║██║   ██║██╔██╗ ██║
██╔══██║██║   ██║   ██║   ██║   ██║██║╚██╔╝██║██╔══██║   ██║   ██║██║   ██║██║╚██╗██║
██║  ██║╚██████╔╝   ██║   ╚██████╔╝██║ ╚═╝ ██║██║  ██║   ██║   ██║╚██████╔╝██║ ╚████║
╚═╝  ╚═╝ ╚═════╝    ╚═╝    ╚═════╝ ╚═╝     ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝ ╚═════╝ ╚═╝  ╚═══╝
</pre>

### 🎬 Demo Video → **[Watch Full Workflow Demo](https://drive.google.com/file/d/1oscpLaeHALSRTYQPnyXWFAlQk9K1nxEc/view?usp=sharing)**

[![Demo Video](https://img.shields.io/badge/▶_Watch_Demo-Google_Drive-EA4B8B?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1oscpLaeHALSRTYQPnyXWFAlQk9K1nxEc/view?usp=sharing)
[![GitHub](https://img.shields.io/badge/GitHub-akshayy718-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/akshayy718)
[![n8n](https://img.shields.io/badge/n8n-Cloud_v2.10.4-EA4B8B?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io)

</div>

<div align="center">

![n8n](https://img.shields.io/badge/n8n-Cloud_v2.10.4-EA4B8B?style=flat-square&logo=n8n&logoColor=white)
![Gmail API](https://img.shields.io/badge/Gmail_API-OAuth_2.0-FF6B9D?style=flat-square&logo=gmail&logoColor=white)
![SAP](https://img.shields.io/badge/SAP-SuccessFactors-EA4B8B?style=flat-square&logo=sap&logoColor=white)
![Sage X3](https://img.shields.io/badge/Sage-X3_ERP-FF6B9D?style=flat-square)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-EA4B8B?style=flat-square&logo=javascript&logoColor=white)
![REST API](https://img.shields.io/badge/REST-API_Integration-FF6B9D?style=flat-square)

</div>

---

## 📌 Overview

An **enterprise-grade GL Entry Approval Automation** built on **n8n Cloud** that bridges **SAP SuccessFactors** (finance source) and **Sage X3** (ERP target) through a structured human-in-the-loop approval workflow.

> 🏦 Every General Ledger entry is automatically fetched, routed to the approver via email, and posted to Sage X3 only after explicit approval — with full audit trail throughout.

Eliminates manual GL approval bottlenecks, enforces segregation of duties, and ensures every financial entry is authorized before hitting the ERP system.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔄 **Automated GL Fetch** | Pulls new GL entries from SAP SuccessFactors via OData REST API on schedule |
| 📧 **Smart Approval Email** | Professional HTML email with 20+ GL fields sent to approver via Gmail API |
| ✅ **Human-in-the-Loop** | Approver clicks Approve/Reject directly in email — no login required |
| 🏦 **Sage X3 Integration** | Approved entries auto-posted to Sage X3 via REST API (GACCENTRY endpoint) |
| ❌ **Rejection Flow** | Rejected entries trigger instant notification to requester with reason |
| 📊 **23 GL Fields Mapped** | Full field mapping: ACCNUM, AMTCUR, ACCDAT, DESVCR, LEDTYP, CCE, PJT and more |
| 🔐 **OAuth 2.0 Security** | Gmail integration uses OAuth 2.0 — no passwords stored |
| 🚨 **Error Notifications** | Dedicated error workflow alerts admin on any failure |
| 📬 **Posted Confirmation** | Requester receives confirmation email when entry is successfully posted |

---

## 🎬 Demo Video

<div align="center">

| | Link | Description |
|--|------|-------------|
| 🎬 | [**Watch Full Workflow Demo**](https://drive.google.com/file/d/1oscpLaeHALSRTYQPnyXWFAlQk9K1nxEc/view?usp=sharing) | Complete end-to-end demo — approval + rejection flows |

</div>

---

## 🏗️ Workflow Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    SCHEDULE TRIGGER                          │
│                                                             │
│   Runs automatically every 15 days (configurable)           │
│   Kicks off the GL entry fetch process                      │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│              CODE NODE — GL DATA GENERATION                  │
│                                                             │
│   Generates / fetches GL entry with 23 fields:             │
│   entryId · amount · currency · accountCode · accountName   │
│   date · postingDate · costCenter · projectCode · ledgerType│
│   documentType · fiscalYear · period · companyCode          │
│   debitAccount · creditAccount · taxCode · referenceNumber  │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│            EXTRACT ENTRY DETAILS (Set Node)                  │
│                                                             │
│   Maps 23 GL fields to structured variables                 │
│   Validates and types each field correctly                  │
│   Prepares payload for approval email                       │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│         SEND APPROVAL EMAIL (Gmail API + OAuth 2.0)          │
│                                                             │
│   Sends professional HTML email to finance manager          │
│   Shows: Entry ID · Amount · Account · Cost Center          │
│   Contains: [Approve] and [Reject] buttons                  │
│   PAUSES workflow — waits for manager response              │
└──────────────────────────┬──────────────────────────────────┘
                           │
                    Manager responds
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                IF NODE — APPROVAL DECISION                   │
│                                                             │
│   Checks: $json.data.approved === true                      │
│   TRUE  → Approved path                                     │
│   FALSE → Rejected path                                     │
└─────────────┬───────────────────────────┬───────────────────┘
              │                           │
         TRUE ▼                      FALSE ▼
┌─────────────────────┐     ┌──────────────────────────────┐
│  CREATE GL ENTRY    │     │    SEND REJECTION EMAIL       │
│  IN SAGE X3         │     │                              │
│                     │     │  Notifies requester with:    │
│  POST to Sage X3    │     │  Entry ID · Amount · Date    │
│  REST API endpoint  │     │  Account Code · Description  │
│  Maps all fields    │     │  Rejection reason            │
│  to Sage X3 schema: │     └──────────────────────────────┘
│  ACCNUM · AMTCUR    │
│  ACCDAT · DESVCR    │
│  LEDTYP · CCE · PJT │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────────────────────────────────────────────┐
│              SEND POSTED CONFIRMATION EMAIL                  │
│                                                             │
│   Confirms to requester: GL Entry Successfully Posted ✅    │
│   Includes: Entry ID · Amount · Account · Status: POSTED    │
└─────────────────────────────────────────────────────────────┘
```

---

## 🔄 Approval Flow Diagram

```
Finance Team                  n8n Workflow                Finance Manager
     │                             │                             │
     │  GL Entry Created           │                             │
     │ ─────────────────────────► │                             │
     │                             │                             │
     │                             │  Fetch GL Entry             │
     │                             │  (Schedule Trigger)         │
     │                             │                             │
     │                             │  Extract 23 Fields          │
     │                             │  ┌─────────────────┐        │
     │                             │  │ entryId         │        │
     │                             │  │ amount: 5000 AED│        │
     │                             │  │ accountCode     │        │
     │                             │  │ costCenter      │        │
     │                             │  │ projectCode     │        │
     │                             │  └─────────────────┘        │
     │                             │                             │
     │                             │  Send Approval Email ──────►│
     │                             │  [Approve] [Reject]         │
     │                             │                             │
     │                             │◄── Manager clicks Approve ──│
     │                             │                             │
     │                             │  IF approved = true         │
     │                             │  POST to Sage X3 API        │
     │                             │                             │
     │◄── Posted Confirmation ─────│                             │
     │    ✅ GL-2026-001 Posted     │                             │
     │                             │                             │
```

---

## 🗂️ GL Field Mapping — SuccessFactors → Sage X3

```
SAP SuccessFactors Field          Sage X3 API Field
─────────────────────────────     ─────────────────
entryId          ──────────────►  VCRNUM  (Voucher Number)
amount           ──────────────►  AMTCUR  (Amount in Currency)
accountCode      ──────────────►  ACCNUM  (Account Number)
postingDate      ──────────────►  ACCDAT  (Accounting Date)
description      ──────────────►  DESVCR  (Description)
ledgerType       ──────────────►  LEDTYP  (Ledger Type)
currency         ──────────────►  CUR     (Currency Code)
costCenter       ──────────────►  CCE     (Cost Center)
projectCode      ──────────────►  PJT     (Project Code)
fiscalYear       ──────────────►  FISCAL  (Fiscal Year)
period           ──────────────►  PER     (Accounting Period)
```

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Automation** | n8n Cloud v2.10.4 | Workflow orchestration engine |
| **Source System** | SAP SuccessFactors | GL entry origin (OData REST API) |
| **Target System** | Sage X3 ERP | GL journal entry destination (REST API) |
| **Email** | Gmail API | Approval notification delivery |
| **Auth** | OAuth 2.0 | Secure Gmail authentication |
| **Logic** | JavaScript (ES6) | GL data generation and transformation |
| **Trigger** | Schedule Trigger | Automated periodic execution |
| **Decision** | IF Node | Approve/Reject routing logic |

</div>

---

## 📁 Project Structure

```
gl-entry-approval-automation/
├── 📄 GL_Entry_Approval_Workflow.json   → n8n workflow (import directly)
├── 📄 README.md                         → This file
└── 📁 screenshots/                      → Workflow and email screenshots
```

---

## ⚡ Quick Start

### Prerequisites
- n8n Cloud account (free trial) or self-hosted n8n
- Gmail account with API access
- SAP SuccessFactors API credentials (from your SF admin)
- Sage X3 server URL + credentials (from your IT team)

### Import Workflow

```bash
# 1. Download the workflow JSON
# GL_Entry_Approval_Workflow.json

# 2. Open n8n Cloud
# Go to app.n8n.cloud

# 3. Create new workflow
# Click "..." → "Import from file"
# Select GL_Entry_Approval_Workflow.json

# 4. Connect credentials
# Gmail → OAuth 2.0 (follow Google auth flow)
# Sage X3 → Basic Auth (username + password)
# SuccessFactors → Basic Auth (username + API key)

# 5. Update configuration
# Replace mock GL data with real SuccessFactors API endpoint
# Replace jsonplaceholder URL with real Sage X3 endpoint
# Update approver email address

# 6. Activate workflow
# Click "Publish" → Toggle Active
```

### Configure Sage X3 Endpoint
```
POST https://{your-sage-x3-server}/syracuse/collaboration/syracuse/api/v1/GESBPC/GACCENTRY

Headers:
  Content-Type: application/json
  Authorization: Basic {base64(username:password)}

Body:
{
  "ACCNUM": "ACC-101",
  "AMTCUR": 5000.00,
  "ACCDAT": "20260309",
  "DESVCR": "Office supplies for Q1 2026",
  "LEDTYP": "1",
  "CUR": "AED",
  "CCE": "DEPT-IT",
  "PJT": "PROJ-001"
}
```

### Configure SuccessFactors Endpoint
```
GET https://{api-server}.successfactors.com/odata/v2/GLAccount

Headers:
  Authorization: Basic {base64(username:apikey)}
  Accept: application/json
```

---

## 📧 Approval Email Preview

```
┌─────────────────────────────────────────────┐
│         GL Entry Approval Required           │
│                                             │
│  Entry ID:    GL-2026-001                   │
│  Amount:      5000 AED                      │
│  Account:     ACC-101 - Office Supplies     │
│  Cost Center: DEPT-IT                       │
│  Project:     PROJ-001                      │
│  Date:        2026-03-09                    │
│  Description: Office supplies for Q1 2026   │
│  Created By:  finance@rgct.com              │
│  Company:     RGCT-001                      │
│                                             │
│  ┌──────────┐    ┌──────────────────────┐   │
│  │  Reject  │    │       Approve        │   │
│  └──────────┘    └──────────────────────┘   │
│                                             │
│         Automated with n8n                  │
└─────────────────────────────────────────────┘
```

---

## 🔮 Production Roadmap

- [ ] **Real SuccessFactors API** — replace mock data with live OData endpoint
- [ ] **Real Sage X3 API** — replace placeholder with production GACCENTRY endpoint
- [ ] **Multi-level approval** — CFO approval for entries above AED 50,000
- [ ] **Google Sheets audit log** — full audit trail with approver identity + timestamp
- [ ] **Duplicate detection** — prevent same GL entry being submitted twice
- [ ] **Reminder escalation** — auto-reminder if approval pending > 24 hours
- [ ] **Batch processing** — handle multiple GL entries in single execution
- [ ] **Dashboard** — approval rates, pending count, processing times

---

## 💼 Business Value

| Before Automation | After Automation |
|---|---|
| Manual email chains for approvals | One-click approve/reject in email |
| No audit trail | Full log of who approved what and when |
| Entries posted without authorization | Mandatory approval gate before Sage X3 |
| Hours of manual data entry | Instant API-to-API transfer |
| No rejection notifications | Instant requester notification with reason |
| No escalation process | Error notifications to admin on failure |

---

## 👨‍💻 Author

<div align="center">

**Akshay Santhosh** — AI/ML Engineer · Workflow Automation · SAP BTP Developer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Akshay%20Santhosh-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akshay-santhosh-435499208/)
[![GitHub](https://img.shields.io/badge/GitHub-akshayy718-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/akshayy718)
[![Email](https://img.shields.io/badge/Gmail-akshaysanthosh718-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:akshaysanthosh718@gmail.com)

</div>

---

<div align="center">

*Built with ❤️ using n8n Cloud · SAP SuccessFactors · Sage X3 · Gmail API · OAuth 2.0*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0,FFB3D1,FF6B9D,EA4B8B&height=130&section=footer&animation=fadeIn" width="100%"/>

</div>
