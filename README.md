# 🧠 Support Triage Agent (Multi-Domain)

This project is a simple terminal-based support triage agent built for the HackerRank Orchestrate hackathon.

The goal of this agent is to read support tickets and decide:
- what kind of issue it is
- which product it belongs to
- whether it can be answered safely
- or if it should be escalated to a human

It works across three domains:
- HackerRank
- Claude
- Visa

---

## 🚀 What this agent does

For every support ticket, the agent:

- Reads the issue and subject
- Understands the type of request (bug, feature request, etc.)
- Identifies the product area
- Checks if the issue is risky (like fraud or hacking)
- Decides whether to reply or escalate
- Generates a short and safe response
- Saves everything into a clean CSV file


## 🛠️ Tech Used

- Python
- Pandas


## ▶️ How to run

### Step 1: Install pandas

```bash
pip install pandas
