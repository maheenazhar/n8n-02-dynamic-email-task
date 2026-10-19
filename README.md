# ⚡ Dynamic Email Task Automation

[![n8n workflow](https://img.shields.io/badge/n8n-Workflow-orange.svg)](https://n8n.io)
[![Sequence](https://img.shields.io/badge/Sequence-%2302-blue.svg)](#)
[![Difficulty](https://img.shields.io/badge/Difficulty-Beginner-green.svg)](#)
[![Status](https://img.shields.io/badge/Status-Production--Ready-brightgreen.svg)](#)

> **Workflow Sequence #02** in the [Maheen Azhar n8n Workflow Collection](https://github.com/maheenazhar/n8n-workflows-collection).

---

## 📖 Overview

Listens for row updates or new submissions in Google Sheets and triggers automated, personalized email notifications via Gmail with dynamic placeholders.

### 🎯 Key Use Case
Automating client notifications, order confirmations, or internal task assignments as soon as a spreadsheet row is added or updated.

---

## 🏗️ Architecture & Flow

```mermaid
graph TD
  N0_Google_Sheets_Trigger["Google Sheets Trigger<br><i>(googleSheetsTrigger)</i>"]
  N1_Send_a_message["Send a message<br><i>(gmail)</i>"]
  N0_Google_Sheets_Trigger --> N1_Send_a_message
```

---

## 🧩 Nodes in this Workflow

| # | Node Name | Type | Version |
|---|-----------|------|---------|
| 1 | **Google Sheets Trigger** | `n8n-nodes-base.googleSheetsTrigger` | v1 |
| 2 | **Send a message** | `n8n-nodes-base.gmail` | v2.2 |

---

## 🔑 Prerequisites & Credentials

Before running this workflow, ensure you have the following configured in your n8n environment:

- [ ] **Google Sheets OAuth2 credential**
- [ ] **Gmail OAuth2 credential**
- [ ] **Google Sheet configured with recipient and task columns**

> [!NOTE]
> All credentials are decoupled from this export file for security. When importing into your n8n workspace, re-assign your local credentials in the respective node configuration panels.

---

## 🚀 Setup & Installation

1. **Clone or Download:**
   ```bash
   git clone https://github.com/maheenazhar/n8n-02-dynamic-email-task.git
   cd n8n-02-dynamic-email-task
   ```
2. **Import into n8n:**
   - Open your n8n canvas.
   - Click the top-right menu `...` -> **Import from File**.
   - Select `workflow.json` from this repository.
   - *(Alternative)*: Open `workflow.json`, copy the entire JSON contents, and paste directly (`Ctrl+V`) onto the n8n canvas.
3. **Configure Credentials:**
   - Open each integration node marked with a red credential prompt.
   - Select or configure your accounts (e.g., Google OAuth, Groq API, Supabase, SMTP).
4. **Activate / Test:**
   - Click **Test step** or **Execute Workflow** to verify end-to-end functionality.
   - Toggle the workflow to **Active** for live production use.

---

## 📄 File Structure

```
02-dynamic-email-task/
├── workflow.json   # Full exportable n8n workflow definition
├── README.md       # Comprehensive documentation and architecture
└── .gitignore      # Standard Git exclusions
```

---

## 👤 Author & Repository

- **Author:** [Maheen Azhar](https://github.com/maheenazhar)
- **Workflow ID:** `SYsZPKHkIaEiipLh`
- **Created Date:** `2026-10-07 19:14:39.070`
- **Last Modified:** `2026-10-07 19:39:50.661`
- **Repository:** [`https://github.com/maheenazhar/n8n-02-dynamic-email-task`](https://github.com/maheenazhar/n8n-02-dynamic-email-task)

---

*Part of the [n8n Workflows Collection](https://github.com/maheenazhar/n8n-workflows-collection) by Maheen Azhar.*
