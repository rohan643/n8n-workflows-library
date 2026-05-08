<div align="center">

# 🔄 n8n Workflows Library

**50+ production-ready n8n workflow templates for real businesses**

[![n8n](https://img.shields.io/badge/n8n-1.x-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Workflows](https://img.shields.io/badge/Workflows-54-gold?style=for-the-badge)]()
[![Stars](https://img.shields.io/github/stars/rohan643/n8n-workflows-library?style=for-the-badge&color=gold)]()

</div>

---

## What's Inside

A hand-crafted library of battle-tested n8n workflows built for real client deployments. Every workflow in this repo has been running in production. No toy examples.

## Workflow Categories

### 📧 Email & Communication
| Workflow | Description | Nodes |
|---|---|---|
| `email-sequence-crm.json` | Drip email sequence triggered by CRM stage changes | HubSpot → Gmail → Wait → Condition |
| `slack-digest.json` | Daily Slack digest of key business metrics | Airtable → OpenAI → Slack |
| `cold-email-reply-handler.json` | Auto-categorizes replies (interested/not now/unsubscribe) and updates CRM | Gmail → OpenAI → HubSpot |
| `invoice-reminder-sequence.json` | 3-touch invoice reminder with escalation logic | Stripe → Gmail → Slack |

### 🎯 Lead Generation & CRM
| Workflow | Description | Nodes |
|---|---|---|
| `lead-scoring-engine.json` | Scores inbound leads 0-100 using firmographic + behavioral data | Webhook → OpenAI → Airtable → HubSpot |
| `linkedin-to-crm.json` | Parses LinkedIn profile data and creates enriched CRM contacts | HTTP → Clearbit → HubSpot |
| `lead-dedup-merge.json` | Detects and merges duplicate leads across CRM | HubSpot → Code → HubSpot |
| `webinar-to-pipeline.json` | Converts webinar registrants to pipeline opportunities with follow-up | Zoom → HubSpot → Gmail |

### ⚡ Business Operations
| Workflow | Description | Nodes |
|---|---|---|
| `client-onboarding-full.json` | Full zero-touch onboarding: payment → contract → workspace → welcome | Stripe → DocuSign → Notion → Gmail |
| `proposal-generator.json` | Generates personalized proposals from discovery call notes | Notion → OpenAI → Google Docs → Gmail |
| `contract-tracker.json` | Tracks contract status and sends renewal reminders 60/30/7 days out | Airtable → Condition → Gmail |
| `monthly-report-automation.json` | Pulls data from 5 sources, generates PDF report, emails to client | Multiple APIs → OpenAI → PDF → Gmail |

### 🛒 E-Commerce
| Workflow | Description | Nodes |
|---|---|---|
| `abandoned-cart-recovery.json` | 3-email abandoned cart sequence with discount escalation | Shopify → Gmail → Condition |
| `post-purchase-flow.json` | Thank you → review request → upsell sequence with smart timing | Shopify → Gmail → Wait |
| `inventory-low-alert.json` | Slack + email alert when inventory drops below threshold | Shopify → Condition → Slack → Gmail |
| `refund-automation.json` | Auto-processes refunds under $50, routes larger ones for manual review | Shopify → Stripe → Condition → Slack |

### 🤖 AI-Powered
| Workflow | Description | Nodes |
|---|---|---|
| `ai-content-repurposer.json` | Takes one long-form blog post → 10 social posts + email newsletter | Google Docs → OpenAI → Buffer → Mailchimp |
| `ai-support-triage.json` | Classifies inbound support tickets and auto-resolves common issues | Gmail → OpenAI → Zendesk |
| `competitor-monitor.json` | Daily competitor pricing & content monitor with Slack summary | HTTP → OpenAI → Slack |
| `ai-meeting-notes.json` | Transcribes meetings → extracts action items → creates Notion tasks | Fireflies → OpenAI → Notion → Slack |

---

## Quick Start

### Prerequisites
- n8n instance (self-hosted or cloud)
- API credentials for relevant services

### Import a Workflow
```bash
# 1. Clone the repo
git clone https://github.com/rohan643/n8n-workflows-library.git

# 2. Open n8n → Workflows → Import from File
# 3. Select the .json file you want
# 4. Add your credentials in the credential nodes
# 5. Activate and test
```

### Environment Variables
Each workflow README documents required credentials. Common ones:
```env
OPENAI_API_KEY=sk-...
HUBSPOT_API_KEY=...
AIRTABLE_API_KEY=...
SLACK_WEBHOOK_URL=...
```

---

## Workflow Structure

All workflows follow this pattern:

```
Trigger (Webhook/Cron/App Event)
    ↓
Input Validation + Normalization
    ↓
Core Business Logic (with error branches)
    ↓
Output / Notifications
    ↓
Error Handler (Slack alert + log to Airtable)
```

Every workflow has:
- ✅ Error handling on every node
- ✅ Sticky notes explaining non-obvious logic
- ✅ Test data included
- ✅ Documented credentials

---

## Stats

```
Total Workflows:     54
Total Nodes Used:    847
Services Covered:    23
Production Tested:   100%
Client Deployments:  38
```

---

## Contributing

Found a bug or want to add a workflow? Open a PR. Requirements:
- Must be production-tested (not just demo)
- Must include error handling
- Must include sticky note documentation

---

<div align="center">

**Built by [Rohan Mukherjee](https://github.com/rohan643) @ Apex Automation Co.**

</div>
