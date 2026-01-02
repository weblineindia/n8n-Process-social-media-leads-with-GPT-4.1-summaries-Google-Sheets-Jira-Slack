# Process Social Media Leads with GPT‑4.1 Summaries, Google Sheets, Jira & Slack

This workflow automatically collects new lead messages from social media platforms, LinkedIn, or web forms, filters relevant marketing inquiries using keywords, classifies and summarizes the lead using AI (GPT‑4.1), logs it to Google Sheets, creates a Jira task, and sends Slack notifications. Additionally, it generates weekly lead reports for team insights. This end‑to‑end pipeline reduces manual triage, ensures no valid inquiry is missed, and keeps your team updated with both immediate notifications and weekly summary reports. :contentReference[oaicite:1]{index=1}

---

## ⚡ Quick Start – Implementation Steps

1. Connect your webhook to your social media inbox, LinkedIn, Twitter, or web form. :contentReference[oaicite:2]{index=2}
2. Add your **OpenAI**, **Google Sheets**, **Jira**, and **Slack** credentials in n8n. :contentReference[oaicite:3]{index=3}
3. Enable the workflow. :contentReference[oaicite:4]{index=4}
4. Send a test message to confirm Google Sheets logging, Slack notification, and Jira task creation. :contentReference[oaicite:5]{index=5}
5. Activate the scheduler for weekly reports to track lead performance. :contentReference[oaicite:6]{index=6}

---

## 📌 What It Does

This workflow performs the following key tasks: :contentReference[oaicite:7]{index=7}

- Filters incoming messages for marketing‑related keywords like ad request, promo request, collaboration, partnership or social media inquiry. :contentReference[oaicite:8]{index=8}
- Uses **GPT‑4.1** to classify the lead into categories such as Sales, Support, Partnership, Influencer Inquiry, or General Lead. :contentReference[oaicite:9]{index=9}
- Generates a short AI summary of the message content. :contentReference[oaicite:10]{index=10}
- Logs structured lead data to **Google Sheets** (username, source, category, summary, timestamp). :contentReference[oaicite:11]{index=11}
- Creates a **Jira** task automatically with summary, description, category, and received time. :contentReference[oaicite:12]{index=12}
- Sends a **Slack notification** to alert the team instantly. :contentReference[oaicite:13]{index=13}
- Runs a scheduled workflow that aggregates weekly leads and sends a weekly report to Slack. :contentReference[oaicite:14]{index=14}

This ensures a structured, automated pipeline for capturing, summarizing, and assigning leads efficiently. :contentReference[oaicite:15]{index=15}

---

## 👥 Who’s It For

- Marketing and sales teams handling leads from social media and web forms. :contentReference[oaicite:16]{index=16}
- Agencies managing client campaigns and inquiries. :contentReference[oaicite:17]{index=17}
- Businesses that want automated notifications and ticketing. :contentReference[oaicite:18]{index=18}
- Teams using Slack and Jira for daily operations. :contentReference[oaicite:19]{index=19}

---

## 🛠 Requirements to Use This Workflow

- n8n account or self‑hosted instance. :contentReference[oaicite:20]{index=20}
- Webhook‑enabled social media inbox or lead form endpoint. :contentReference[oaicite:21]{index=21}
- **OpenAI API Key** with access to GPT‑4.1. :contentReference[oaicite:22]{index=22}
- **Slack Bot Token** with permission to post in your channel. :contentReference[oaicite:23]{index=23}
- **Jira Software Cloud API credentials**. :contentReference[oaicite:24]{index=24}
- **Google Sheets credentials**. :contentReference[oaicite:25]{index=25}
- Predefined keyword list for filtering inbound messages. :contentReference[oaicite:26]{index=26}

---

## 🧠 How It Works & Setup Steps

### 1. Webhook Trigger

Receives new messages from social media or web forms and starts the workflow. :contentReference[oaicite:27]{index=27}

### 2. Lead Keyword Filter (Code Node)

Filters incoming messages using a predefined list of marketing or inquiry keywords. :contentReference[oaicite:28]{index=28}

### 3. AI Lead Classifier (OpenAI Node)

Sends the message text to the GPT‑4.1 model, which returns a category and a concise summary. :contentReference[oaicite:29]{index=29}

### 4. AI Output Parser (Code Node)

Parses the structured JSON from the AI model and merges it with original message fields including timestamp. :contentReference[oaicite:30]{index=30}

### 5. Store Lead (Google Sheets Node)

Logs the structured lead (username, source, category, summary, timestamp) into Google Sheets. :contentReference[oaicite:31]{index=31}

### 6. Create Task (Jira Node)

Automatically creates a Jira ticket with the AI summary, category, and timestamp. :contentReference[oaicite:32]{index=32}

### 7. Send a Summary (Slack Node)

Sends a formatted Slack message to the channel you’ve selected to notify your team instantly. :contentReference[oaicite:33]{index=33}

### 8. Weekly Reporting

- **Schedule Trigger** — Runs weekly.
- **Extract Lead Data** — Fetches all logged leads from Google Sheets.
- **Weekly Lead Filter** — Filters to last week’s records.
- **Report Data Formatter** — Calculates totals, category counts, and example leads.
- **Weekly Report Slack** — Posts a formatted weekly summary to Slack. :contentReference[oaicite:34]{index=34}

---

## 🛠 How to Customize Nodes

### Keyword Filter

Modify the JavaScript code to add, remove, or adjust keywords for your specific campaigns or lead types. :contentReference[oaicite:35]{index=35}

### AI Classification

Update the **OpenAI prompt** to refine summary style, categories, or tone. :contentReference[oaicite:36]{index=36}

### Google Sheets Logging

Map additional columns such as email, phone number, or campaign source as needed. :contentReference[oaicite:37]{index=37}

### Jira Fields

Customize summary, description, labels, priority, assignees, or project destination. :contentReference[oaicite:38]{index=38}

### Slack Message Format

Adjust emojis, line breaks, and formatting to suit your preferred Slack style or team standards. :contentReference[oaicite:39]{index=39}

---

## ➕ Add‑Ons (Workflow Extensions)

- Send email alerts for **high‑priority** or VIP leads. :contentReference[oaicite:40]{index=40}
- Trigger **WhatsApp replies** using a message API provider. :contentReference[oaicite:41]{index=41}
- Integrate with CRMs like **HubSpot, Zoho, or Salesforce**. :contentReference[oaicite:42]{index=42}
- Add **sentiment analysis** to detect frustrated or high‑value users. :contentReference[oaicite:43]{index=43}
- Automate **daily analytics reports** or dashboards to Slack. :contentReference[oaicite:44]{index=44}

---

## 📈 Use Case Examples

1. **Instagram, LinkedIn, Twitter DMs** logged into Google Sheets. :contentReference[oaicite:45]{index=45}
2. Creating automated **Jira tickets** for marketing inquiries. :contentReference[oaicite:46]{index=46}
3. Sending **instant Slack alerts** for new leads. :contentReference[oaicite:47]{index=47}
4. Filtering irrelevant messages and only processing **qualified marketing leads**. :contentReference[oaicite:48]{index=48}
5. Generating **weekly summary reports** for team review. :contentReference[oaicite:49]{index=49}

---

## 🧪 Troubleshooting Guide

| **Issue**              | **Possible Cause**                          | **Solution**                                             |
| ---------------------- | ------------------------------------------- | -------------------------------------------------------- | --------------------------------------- |
| No leads appear        | Webhook not receiving messages              | Check webhook URL and ensure messages are sent correctly |
| AI summary empty       | Invalid OpenAI API key or model quota issue | Regenerate API key or check usage limits                 |
| Jira task not created  | Missing required Jira fields                | Add needed fields and update Jira node settings          |
| Slack message not sent | Incorrect channel or missing permissions    | Reconnect Slack credentials and verify channel           |
| Filter passes 0 items  | Keywords not matching                       | Update or expand the keyword list in the filter node     | :contentReference[oaicite:50]{index=50} |

---

## 💬 Need Help?

If you need assistance setting up this workflow, troubleshooting any issue, customizing nodes, building add‑ons, or automating more processes, our n8n workflow development team at **WeblineIndia** can help you. We can assist with integrations, scaling this pipeline, or building tailored automation solutions for your business. :contentReference[oaicite:51]{index=51}

---

If you want, I can **generate this as a downloadable `README.md` file** — just tell me!
::contentReference[oaicite:52]{index=52}
