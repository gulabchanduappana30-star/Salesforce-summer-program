# Day 4 – Flow Builder

## 1. What is Flow Builder?

Flow Builder is an automation tool in Salesforce used to automate business processes without writing code. It helps users create workflows visually using elements and connectors.

Flow Builder can:

- Create records
- Update records
- Delete records
- Send emails
- Post to Chatter
- Trigger approvals
- Automate tasks

Example:

When a new Lead is created:

Lead Created  
↓  
Flow Runs  
↓  
Check matching Account  
↓  
Update Lead automatically

Flow Builder reduces manual work and improves efficiency.

---

## 2. Types of Flows

Salesforce provides different flow types.

Examples:

1. Screen Flow
2. Record Triggered Flow
3. Scheduled Flow
4. Autolaunched Flow
5. Platform Event Flow

### Screen Flow

Screen Flow interacts with users using forms and screens.

Features:

- Takes user input
- Shows messages
- Works like an application form
- Used in customer portals

Example 1:

Employee enters leave request

Screen appears  
↓  
Employee fills form  
↓  
Request saved

Example 2:

Customer fills support ticket

Screen Flow  
↓  
Capture details  
↓  
Create case

---

### Record Triggered Flow

Record Triggered Flow runs automatically when records are created, updated, or deleted.

Features:

- No manual action required
- Runs automatically
- Used for automation

Example 1:

New Account created

Account Created  
↓  
Flow runs  
↓  
Create follow-up task

Example 2:

Lead company matches account

Lead Created  
↓  
Flow checks account  
↓  
Updates matching account field

---

## 3. Your Automation Ideas

### Idea 1: Student Attendance Alert

Attendance below 75%

↓

Flow sends warning email

---

### Idea 2: Leave Approval Automation

Employee applies leave

↓

Manager approval notification sent

---

### Idea 3: Customer Follow-Up

New customer account created

↓

Task created automatically

---

### Idea 4: Lead Matching System

Lead entered

↓

Flow checks existing accounts

↓

Marks matching account

---

### Idea 5: Ticket Escalation

Support ticket open more than 3 days

↓

Flow escalates ticket

---

## 4. Your Flow Diagram

Example diagram:

Lead Created

↓

Look for Matching Account

↓

Update Matching Account

↓

Post to Chatter

↓

Send Email

Add image:

flow-diagram.png

You can draw using:

- draw.io
- PowerPoint
- Paint
- Screenshot from Flow Builder

---

## 5. Manual vs Automated Process

| Manual Process | Automated Process |
|---------------|-------------------|
| User enters data manually | Flow updates automatically |
| More time required | Faster process |
| Higher error chance | Lower error chance |
| Repeated work | Reusable automation |
| Human dependency | System driven |

Example:

Manual:

Lead created  
↓  
User searches account  
↓  
User updates field

Automated:

Lead created  
↓  
Flow checks account  
↓  
Field updated automatically

---

## 6. Reflection – Why Automation Matters in Enterprise Systems

Automation is important because enterprise systems handle large amounts of data and repeated processes.

Benefits:

- Saves time
- Reduces errors
- Improves productivity
- Handles large scale operations
- Gives faster responses
- Reduces manual work

Examples:

1. Banking

Loan approval notifications sent automatically.

2. E-commerce

Order created

↓

Invoice generated automatically

3. CRM Systems

Lead entered

↓

Customer data processed automatically

Automation helps companies increase efficiency and improve business performance.

---
