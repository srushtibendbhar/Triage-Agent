🧠 Multi-Domain Support Triage Agent

This project is a terminal-based support triage agent built as part of the HackerRank Orchestrate hackathon.

The main idea behind this project is simple — support teams receive a lot of tickets, and not all of them need the same level of attention. Some can be answered automatically, while others (like fraud or security issues) should be handled by a human.

This agent helps in making that decision.

🚀 What the agent does

For each support ticket, the system:

Reads the issue and subject
Identifies the type of request (bug, feature request, product issue, etc.)
Detects which product the ticket belongs to (HackerRank, Claude, or Visa)
Checks if the issue is sensitive or risky
Decides whether to reply or escalate
Generates a short and safe response
Saves the result in a structured CSV file
🛠️ Tech stack

Python
Pandas

▶️ How to run

Step 1: Install pandas
Run: pip install pandas

Step 2: Run the program
From the main project folder, run:
python code/main.py support_tickets/support_tickets.csv support_tickets/output.csv

Step 3: Check the output
The output file will be available at:
support_tickets/output.csv

📄 Output format

The output CSV contains the following columns:

status → replied / escalated
product_area → detected domain
request_type → bug / feature_request / product_issue / invalid
response → short user-facing reply
justification → reason behind the decision
🧠 Approach

I used a simple rule-based approach to build this agent.

Combined the subject and issue text
Used keyword matching to classify the request
Identified product area based on company and context
Checked for high-risk keywords like fraud, hacked, and unauthorized

If the issue is risky, the agent escalates it. Otherwise, it generates a safe and clear response.

The focus was on making the system reliable, easy to understand, and consistent.

🚨 Handling sensitive cases

Some tickets require extra care, especially:

fraud-related issues
unauthorized transactions
hacked accounts

These are always escalated instead of being answered automatically.

🔮 Future improvements

With more time, this system can be improved by:

Using support documents more effectively
Improving classification accuracy
Handling multiple requests in a single ticket
Generating more personalized responses
🏁 Final thoughts

This project helped me understand how real-world support systems work and how decisions are made behind the scenes. The goal was to build something simple, clean, and safe rather than overly complex.
