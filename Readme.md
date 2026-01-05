
# Process Social Media Leads with GPT-4.1 Summaries, Google Sheets, Jira & Slack

This workflow automatically collects new lead messages from social media platforms, LinkedIn, or web forms, filters relevant marketing inquiries using keywords, classifies and summarizes the lead using AI (GPT-4.1), logs it to Google Sheets, creates a Jira task, and sends Slack notifications.

It also generates **weekly lead reports** for team insights. This end-to-end automation eliminates manual triage, ensures no valid inquiry is missed, and keeps teams aligned with real-time alerts and weekly summaries.

---

## ⚡ Quick Start – Implementation Steps

1. Connect a **Webhook** to your social media inbox, LinkedIn, Twitter, or web form.
2. Add credentials in n8n:

   * OpenAI
   * Google Sheets
   * Jira
   * Slack
3. Enable the workflow.
4. Send a test message to confirm:

   * Google Sheets logging
   * Slack notification
   * Jira ticket creation
5. Activate the **weekly scheduler** for lead performance reports.

---

## 📌 What It Does

This workflow performs the following actions:

* Filters incoming messages using marketing-related keywords (ads, collaboration, partnership, inquiries).
* Uses **GPT-4.1** to:

  * Classify the lead (Sales, Support, Partnership, Influencer, General).
  * Generate a concise AI summary.
* Logs structured lead data into **Google Sheets**.
* Automatically creates a **Jira issue** with lead details.
* Sends **instant Slack notifications** for new leads.
* Runs a scheduled workflow to generate **weekly lead reports** in Slack.

This creates a structured, automated pipeline for capturing, summarizing, and assigning leads efficiently.

---

## 👥 Who’s It For

* Marketing and sales teams handling social media and web leads.
* Agencies managing multiple client inquiries.
* Businesses needing automated notifications and ticket creation.
* Teams using Slack and Jira as core collaboration tools.

---

## 🛠 Requirements

To use this workflow, you’ll need:

* n8n (cloud or self-hosted).
* Webhook-enabled social media inbox or form endpoint.
* **OpenAI API key** with access to GPT-4.1.
* **Google Sheets** credentials.
* **Jira Software Cloud** API credentials.
* **Slack Bot Token** with permission to post messages.
* A predefined keyword list for filtering inbound messages.

---

## 🧠 How It Works

### 1. Webhook Trigger

Receives new messages from social media platforms or web forms.

### 2. Lead Keyword Filter (Code Node)

Filters messages using a predefined keyword list to detect marketing-relevant inquiries.

### 3. AI Lead Classifier (OpenAI Node)

Sends message text to GPT-4.1, which returns:

* Lead category
* Short summary

### 4. AI Output Parser (Code Node)

Parses structured AI output and merges it with metadata (source, timestamp, username).

### 5. Store Lead (Google Sheets)

Logs lead details:

* Username
* Source
* Category
* AI summary
* Timestamp

### 6. Create Jira Task

Automatically creates a Jira issue with the summarized lead information.

### 7. Slack Notification

Sends a formatted Slack alert to notify the team instantly.

### 8. Weekly Reporting Workflow

* Runs on a schedule.
* Fetches lead data from Google Sheets.
* Filters records from the previous week.
* Aggregates totals and categories.
* Posts a weekly summary report to Slack.

---

## 🛠 Customization Options

### Keyword Filtering

Modify the JavaScript code to adjust keywords for your campaigns.

### AI Classification

Customize the OpenAI prompt to refine:

* Categories
* Summary length
* Tone or formatting

### Google Sheets

Add additional columns such as:

* Email
* Phone number
* Campaign name
* Platform source

### Jira Configuration

Customize:

* Project
* Issue type
* Labels
* Priority
* Assignee

### Slack Formatting

Adjust emojis, layout, and message structure to match your team’s style.

---

## ➕ Optional Add-Ons

* Email alerts for high-priority or VIP leads.
* WhatsApp auto-responses via messaging APIs.
* CRM integrations (HubSpot, Zoho, Salesforce).
* Sentiment analysis for lead urgency detection.
* Daily or monthly analytics dashboards.

---

## 📈 Use Case Examples

* Capture Instagram, LinkedIn, and Twitter DMs automatically.
* Create Jira tickets for every qualified marketing inquiry.
* Notify teams instantly via Slack.
* Filter out spam or irrelevant messages.
* Share weekly lead summaries with stakeholders.

---

## 🧪 Troubleshooting Guide

| Issue                  | Possible Cause              | Solution                             |
| ---------------------- | --------------------------- | ------------------------------------ |
| No leads captured      | Webhook not receiving data  | Verify webhook URL and payload       |
| AI summary empty       | Invalid OpenAI key or quota | Regenerate key or check usage        |
| Jira task not created  | Required fields missing     | Update Jira node configuration       |
| Slack message not sent | Channel or permission issue | Verify Slack credentials and channel |
| No leads pass filter   | Keywords too restrictive    | Expand or adjust keyword list        |

---

## 💬 Need Help?

If you need help with:

* Workflow setup
* Prompt tuning
* Keyword optimization
* Jira or Slack customization
* Scaling or extending this automation

The **WeblineIndia** n8n automation team can help design, customize, and deploy workflows tailored to your business needs.