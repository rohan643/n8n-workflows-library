<div align="center">

# 🔄 n8n Workflows Library

**54 production-tested n8n workflow templates. Drop in, add credentials, activate.**

[![n8n](https://img.shields.io/badge/n8n-Compatible-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io)
[![Workflows](https://img.shields.io/badge/Workflows-54-gold?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

</div>

---

## Categories

### 📧 Email & Communication (12 workflows)
| Workflow | Description |
|---|---|
| `email-sequence-crm.json` | CRM stage change → drip email sequence |
| `slack-digest.json` | Daily Slack digest of key metrics |
| `cold-email-reply-handler.json` | AI-classifies replies → updates CRM |
| `invoice-reminder-sequence.json` | 3-touch invoice reminder with escalation |

### 🎯 Lead Generation (11 workflows)
| Workflow | Description |
|---|---|
| `lead-scoring-engine.json` | GPT-4o ICP scoring on every new lead |
| `linkedin-to-crm.json` | LinkedIn profile → enriched CRM contact |
| `webinar-to-pipeline.json` | Webinar registrant → pipeline opportunity |

### ⚡ Operations (15 workflows)
| Workflow | Description |
|---|---|
| `client-onboarding-full.json` | Payment → contract → workspace → welcome |
| `proposal-generator.json` | Call transcript → Google Doc proposal |
| `monthly-report-automation.json` | 5 sources → PDF → email |

### 🤖 AI-Powered (16 workflows)
| Workflow | Description |
|---|---|
| `ai-content-repurposer.json` | Blog post → 10 social posts + newsletter |
| `ai-support-triage.json` | Classifies + auto-resolves support tickets |
| `ai-meeting-notes.json` | Transcript → action items → Notion tasks |
| `competitor-monitor.json` | Daily competitor intel → Slack briefing |

---

## Quick Import

1. Open n8n → **Workflows** → **Import from file**
2. Select any `.json` from the `workflows/` folder
3. Add credentials to each node (marked with ⚠️)
4. Test with **Execute Workflow**
5. Activate

---

## Error Handling

Every workflow includes:
- ✅ Error branch on critical nodes
- ✅ Slack alert on failure with full context
- ✅ Airtable error log for audit trail
- ✅ Sticky notes explaining non-obvious logic

---

<sub>Built by <a href="https://github.com/rohan643">@rohan643</a></sub>
