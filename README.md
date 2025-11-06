📩 AI-Powered Gmail Automation Workflow using N8N

An Automation Technique which Automatically Detect Important Emails → Create GitHub Issues → Send Telegram Alerts → Auto-Reply via Gmail

🧠 Overview

This project automates the handling of important emails using an AI-driven workflow built in n8n. Whenever a new email arrives, the system checks its content, determines whether it is important, and then triggers a series of automated actions—including GitHub issue creation, Telegram alerts, and Gmail auto-response.

This removes the need for manually scanning busy inboxes and ensures that urgent messages are never missed.

⚙️ Features

 -Automatic Email Detection
 -A Gmail Trigger node constantly monitors the inbox for new messages.

 -AI-Based Email Classification
 -An AI Agent analyzes each email and classifies it as:

   -Important

   -Not Important

  -GitHub Issue Creation
     -If an email is important, a GitHub Issue is automatically created with:

  -Email subject as the title

  -Email body as the description

  -Instant Telegram Notification
      -A Telegram message is sent immediately to notify the user about the important email.

  -Gmail Auto-Reply
      -A confirmation email is automatically sent to the sender.

  -Smooth End-to-End Workflow
     -The workflow ends after sending both Telegram and Gmail notifications.

🏗️Architecture

                ┌──────────────────────────┐
                │        Gmail Inbox       │
                │ (New Email Arrives)      │
                └─────────────┬────────────┘
                              │
                              ▼
                ┌──────────────────────────┐
                │      Gmail Trigger       │
                │ (Detects new email)      │
                └─────────────┬────────────┘
                              │
                              ▼
                ┌──────────────────────────┐
                │        AI Agent          │
                │ Classifies:              │
                │   • Important            │
                │   • Not Important        │
                └───────┬────────┬─────────┘
                        │        │
         Important Email│        │ Not Important
                        │        │
                        ▼        ▼
    ┌───────────────────────┐    ┌────────────────────────┐
    │     GitHub Issue      │    │  No action / End       │
    │ Created Automatically │    └────────────────────────┘
    └──────────┬────────────┘
               │
               ▼
    ┌───────────────────────┐
    │ Telegram Notification │
    │ (Instant Alert)       │
    └──────────┬────────────┘
               │
               ▼
    ┌───────────────────────┐
    │   Gmail Auto-Reply    │
    │ (Confirmation sent)   │
    └──────────┬────────────┘
               │
               ▼
          Workflow Ends

✅ Existing System (Problems)

    -Emails can be missed in a flooded inbox.

    -No automatic way to detect urgent messages.

    -Users must manually check emails.

    -No alerting mechanism.

    -No integration between Gmail, GitHub, and Telegram.

✅ Proposed System (Solution)

    -Uses AI to classify the importance of emails.

    -Automatically creates GitHub issues for urgent tasks.

    -Sends instant notifications via Telegram.

    -Sends auto-reply confirmation through Gmail.

    -Fully automated and reduces manual work.

🧩 Tools & Technologies

| **Tool / Platform**            | **Purpose**                                         |
| ------------------------------ | --------------------------------------------------- |
| ✨ **n8n**                     | Automation & workflow orchestration                |
| 📧 **Gmail API**               | Detects new emails & sends automatic replies        |
| 🤖 **AI Agent (OpenAI)**       | Classifies emails as *Important* or *Not Important* |
| 🐙 **GitHub API**              | Creates issues automatically for important emails   |
| 📲 **Telegram Bot API**        | Sends instant notifications & alerts                |
| 🔐 **OAuth Tokens / API Keys** | Secure authentication for Gmail, GitHub & Telegram  |


-Gmail Trigger: Detects new incoming email.

-AI Agent: Reads email content and categorizes it.

-If Important:

-Creates GitHub Issue

-Sends Telegram Notification

-Sends Gmail Auto-Reply

 -If Not Important: No action is taken.

Workflow ends.

🧨Setup Instructions

1. Sign up on [n8n.io](https://app.n8n.io/workflows) and open your workflow editor.
 

Create and connect credentials:

🔑 Gmail OAuth Credential → connect your Gmail account

🔑 OpenAI API Key → for the AI Agent

🔑 GitHub Personal Access Token → for creating GitHub issues

🔑 Telegram Bot Token → from BotFather + Chat ID

In n8n, add the following nodes:

✅ Gmail Trigger → Detects new incoming emails

✅ AI Agent → Classifies email as Important or Not Important

✅ GitHub Node → Creates an issue automatically for important emails

✅ Telegram Node → Sends instant alert notification

✅ Gmail Send Node → Sends auto-reply confirmation

Connect the workflow like this:
Gmail Trigger → AI Agent → GitHub Issue → Telegram Notification → Gmail Auto-Reply

Configure each node:

Gmail Trigger → New Email

AI Agent → Add prompt for classification

GitHub → Choose repo & map title/body from email

Telegram → Add your Chat ID

Gmail Auto-Reply → Write your confirmation message

Execute Workflow → Send a test email and watch it:
✅ Detect the mail
✅ Classify importance
✅ Create GitHub issue
✅ Send Telegram alert
✅ Send Gmail confirmation


Use Cases
1. Automated Priority Email Detection

2. Real-Time Alerts for Critical Messages

3. Automatic Task Creation in GitHub

4. Auto-Reply for Important Senders

5. Centralized Tracking of Important Emails

🚧 Future Scope

Add priority levels (High / Medium / Low).

Train AI model for more accurate classification.

Add Slack or WhatsApp notifications.

Multi-user support and role-based alerts.

Dashboard for monitoring email logs and issues.

🧑‍💻Author

👩‍🎓 Anaparthi Lavanya B.Tech Student | Automation & AI Enthusiast

🌐 “In a world full of noise, smart automation ensures that what matters never gets missed.”

✅ Conclusion

This project provides an intelligent automation workflow to manage important emails efficiently. By combining AI classification with automation tools (Gmail, GitHub, Telegram), users can stay updated instantly and avoid missing critical information. The system is scalable, flexible, and perfect for personal or team-based productivity.
