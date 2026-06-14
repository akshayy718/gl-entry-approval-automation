<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=0,EA4B8B,FF6B9D,FFB3D1&height=150&section=header&animation=fadeIn" width="100%"/>

# <span>🌸 GL Entry Approval Automation</span>

### `n8n Cloud` · `SAP SuccessFactors` · `Sage X3` · `Gmail API` · `OAuth 2.0`

</div>

<div align="center">

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

## 🏗️ Workflow Architecture

```
╔═══════════════════════════════════════════════════════════════╗
║  ⏰  SCHEDULE TRIGGER                                         ║
║      Runs automatically · Kicks off GL entry fetch            ║
╚══════════════════════════╦════════════════════════════════════╝
                           ║
                           ▼
╔═══════════════════════════════════════════════════════════════╗
║  { }  CODE NODE — GL DATA  (JavaScript)                       ║
║   entryId · amount · currency · accountCode · accountName     ║
║   date · postingDate · costCenter · projectCode · ledgerType  ║
║   documentType · fiscalYear · period · companyCode            ║
║   debitAccount · creditAccount · taxCode · referenceNumber    ║
╚══════════════════════════╦════════════════════════════════════╝
                           ║
                           ▼
╔═══════════════════════════════════════════════════════════════╗
║  ✏️   EXTRACT ENTRY DETAILS  (Set Node)                       ║
║       Maps 23 GL fields · Validates types · Prepares payload  ║
╚══════════════════════════╦════════════════════════════════════╝
                           ║
                           ▼
╔═══════════════════════════════════════════════════════════════╗
║  📧  SEND APPROVAL EMAIL  (Gmail API + OAuth 2.0)             ║
║   Professional HTML email with all GL fields → Manager        ║
║   [ Reject ]                    [ ✅ Approve ]                ║
║              ⏸️  WORKFLOW PAUSES — Waiting for response        ║
╚══════════════════════════╦════════════════════════════════════╝
                           ║
                    Manager responds
                           ║
                           ▼
╔═══════════════════════════════════════════════════════════════╗
║  🔀  IF NODE — APPROVAL DECISION                              ║
║      $json.data.approved === true ?                           ║
╚══════════╦════════════════════════════════════╦══════════════╝
           ║ TRUE ✅                             ║ FALSE ❌
           ▼                                    ▼
╔══════════════════════╗            ╔═══════════════════════════╗
║  🌐  CREATE GL ENTRY ║            ║  📧  SEND REJECTION EMAIL ║
║      IN SAGE X3      ║            ║  Notifies requester with  ║
║  POST to REST API    ║            ║  Entry details + reason   ║
║  ACCNUM · AMTCUR     ║            ╚═══════════════════════════╝
║  ACCDAT · DESVCR     ║
║  LEDTYP · CCE · PJT  ║
╚══════════╦═══════════╝
           ║
           ▼
╔═══════════════════════════════════════════════════════════════╗
║  ✅  SEND POSTED CONFIRMATION EMAIL                           ║
║      GL Entry Successfully Posted to Sage X3 · POSTED ✅     ║
╚═══════════════════════════════════════════════════════════════╝
```

---

## 🌸 Approval Flow

```
  👤 FINANCE TEAM            🤖 n8n WORKFLOW             👔 MANAGER
  ─────────────────        ───────────────────         ─────────────
       │                          │                          │
       │   GL Entry Created       │                          │
       │ ────────────────────────►│                          │
       │                     ⏰ Schedule triggers             │
       │                     { } Generate 23 GL fields       │
       │                     ✏️  Extract & validate           │
       │                          │                          │
       │                          │──── 📧 Approval ────────►│
       │                          │     [Reject][✅ Approve]  │
       │                          │◄─── ✅ Clicks Approve ───│
       │                     🔀 IF approved = true           │
       │                     🌐 POST to Sage X3 API          │
       │◄─── 📬 Posted Confirmation ──────────────────────── │
       │     ✅ GL-2026-001 POSTED                            │
  ─────────────────        ───────────────────         ─────────────
```

---

## 🗂️ GL Field Mapping — SuccessFactors → Sage X3

| SAP SuccessFactors Field | → | Sage X3 API Field | Description |
|---|---|---|---|
| `entryId` | → | `VCRNUM` | Voucher Number |
| `amount` | → | `AMTCUR` | Amount in Currency |
| `accountCode` | → | `ACCNUM` | Account Number |
| `postingDate` | → | `ACCDAT` | Accounting Date |
| `description` | → | `DESVCR` | Description / Narration |
| `ledgerType` | → | `LEDTYP` | Ledger Type |
| `currency` | → | `CUR` | Currency Code |
| `costCenter` | → | `CCE` | Cost Center |
| `projectCode` | → | `PJT` | Project Code |
| `fiscalYear` | → | `FISCAL` | Fiscal Year |
| `period` | → | `PER` | Accounting Period |

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

```bash
# 1. Open n8n Cloud → app.n8n.cloud
# 2. Create new workflow → Import from file
# 3. Select GL_Entry_Approval_Workflow.json
# 4. Connect Gmail credentials (OAuth 2.0)
# 5. Update approver email address
# 6. Replace mock URLs with real API endpoints
# 7. Click Publish → Activate
```

---

## 💼 Business Value

| Before Automation | After Automation |
|---|---|
| Manual email chains for approvals | One-click approve/reject in email |
| No audit trail | Full log of who approved what and when |
| Entries posted without authorization | Mandatory approval gate before Sage X3 |
| Hours of manual data entry | Instant API-to-API transfer |
| No rejection notifications | Instant requester notification with reason |

---

## 🔮 Production Roadmap

- [ ] Real SuccessFactors API — replace mock data with live OData endpoint
- [ ] Real Sage X3 API — replace placeholder with production GACCENTRY endpoint
- [ ] Multi-level approval — CFO approval for entries above AED 50,000
- [ ] Google Sheets audit log — full audit trail with approver identity + timestamp
- [ ] Reminder escalation — auto-reminder if approval pending > 24 hours

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
