# Day 7 - Testing and Salesforce DX

## 1. Why Testing Matters

Testing is an important part of Salesforce development because enterprise applications handle large amounts of business data, customer records, workflows, approvals, and integrations. Errors in production systems can cause data loss, process failures, and business interruptions.

Testing helps developers to:

- Verify that code works correctly
- Detect errors before deployment
- Improve application quality
- Ensure business logic works properly
- Increase system reliability
- Maintain secure deployments

### Example 1:
If an Apex trigger updates student attendance incorrectly, testing helps identify the issue before users access the system.

### Example 2:
If an automation updates account details with wrong values, test classes prevent invalid deployment.

Salesforce requires minimum code coverage before deployment:

- Minimum deployment coverage = 75%
- Critical logic should be tested completely

---

## 2. What is Asynchronous Apex?

Asynchronous Apex is used when operations need to run separately from the main execution flow. It improves performance and handles large or delayed processes.

Types of Asynchronous Apex:

### 1. Future Methods

Used for background execution.

Example:

```apex
@future
public static void updateRecords() {
}
```

Uses:

- Callouts
- Background updates
- Heavy operations

---

### 2. Queueable Apex

Used for advanced asynchronous processing.

Features:

- Supports job chaining
- Supports complex objects
- Better monitoring

Example:

```apex
System.enqueueJob(new MyQueueableClass());
```

---

### 3. Batch Apex

Used for processing large datasets.

Example:

- Updating thousands of Leads
- Data cleanup operations
- Bulk processing

Methods:

- start()
- execute()
- finish()

---

### 4. Scheduled Apex

Runs jobs automatically at specified times.

Example:

- Daily report generation
- Weekly maintenance tasks
- Automatic record updates

Example code:

```apex
System.schedule(
'DailyJob',
cronExpression,
new DailyProcessor()
);
```

---

## 3. What is Salesforce DX?

Salesforce DX (Developer Experience) is a development model and collection of tools used for modern Salesforce application development.

Main components:

### Salesforce CLI

Command line tool used for:

- Creating projects
- Managing scratch orgs
- Running tests
- Deployments

Example:

```bash
sf org login web
```

---

### Scratch Org

Temporary development environment.

Features:

- Short lifespan
- Configurable
- Used for testing

Example workflow:

Developer → Scratch Org → Testing → Deployment

---

### Dev Hub

Main organization used for managing scratch orgs.

Responsibilities:

- Create scratch orgs
- Track environments
- Manage development process

---

### Source Control

Git and GitHub store project code.

Benefits:

- Version history
- Team collaboration
- Rollback support

---

## 4. Complete System Workflow (End-to-End Explanation)

### Step 1:
Requirement Collection

Business team provides requirements.

Example:

Student Management System

Requirements:

- Student registration
- Attendance tracking
- Notifications
- Reports

↓

### Step 2:
System Design

Create:

- Objects
- Fields
- Relationships
- Validation rules

↓

### Step 3:
Development

Build:

- Flows
- Apex classes
- Triggers
- Queueable jobs
- Batch processing

↓

### Step 4:
Testing

Perform:

- Unit testing
- Integration testing
- Automation testing

↓

### Step 5:
Source Control

Push code to GitHub.

```bash
git add .
git commit -m "Day7 submission"
git push
```

↓

### Step 6:
Deployment

Move code:

Developer Org

↓

Testing Org

↓

Production Org

↓

### Step 7:
Monitoring and Maintenance

- Fix bugs
- Improve performance
- Add features
- Monitor logs

---

## 5. Important Test Cases

### Test Case 1: Lead Update Validation

Scenario:

Update LeadSource using Batch Apex.

Input:

200 Leads

Expected Result:

All LeadSource values become:

```text
Dreamforce
```

Status:

PASS

---

### Test Case 2: Queueable Contact Creation

Scenario:

Insert contacts for CA Accounts.

Input:

50 Accounts

Expected:

50 Contacts inserted

Status:

PASS

---

### Test Case 3: Future Method Contact Counter

Scenario:

Count account contacts.

Input:

Account with 2 Contacts

Expected:

```text
Number_Of_Contacts__c = 2
```

Status:

PASS

---

### Test Case 4: Scheduled Apex Processing

Scenario:

Update blank LeadSource records.

Input:

200 Leads

Expected:

LeadSource updated to:

```text
Dreamforce
```

Status:

PASS

---

## 6. Reflection: Why Enterprise Software Development Needs Structured Workflows

Enterprise systems manage important business operations such as customer management, finance, education, healthcare, inventory, and reporting.

Structured workflows are necessary because they:

1. Reduce development errors
2. Improve collaboration
3. Support version control
4. Enable automated testing
5. Increase deployment safety
6. Improve maintainability
7. Support scalability
8. Protect production systems

Without structured workflows:

- Code becomes difficult to manage
- Testing becomes unreliable
- Deployments fail
- Maintenance cost increases

Salesforce DX, testing frameworks, Git, and automation create a controlled development process suitable for enterprise applications.

---

## Technologies Used

- Salesforce Platform
- Apex
- Future Methods
- Queueable Apex
- Batch Apex
- Scheduled Apex
- Salesforce DX
- Git
- GitHub
- Scratch Orgs
- Dev Hub
