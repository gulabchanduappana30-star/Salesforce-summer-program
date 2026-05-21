# Day 6 - Triggers and SOQL

## 1. What is SOQL?

SOQL (Salesforce Object Query Language) is used to retrieve data from Salesforce objects.

It works like SQL but is designed only for Salesforce data.

Example:

```sql
SELECT Name FROM Account
```

This query retrieves Account names.

---

## 2. What is an Apex Trigger?

An Apex Trigger is code that runs automatically when records are inserted, updated, deleted, or restored.

Triggers help automate actions based on data changes.

Example:

If Opportunity stage becomes "Closed Won", automatically create a follow-up task.

---

## 3. Difference Between

### Flow vs Trigger

| Flow | Trigger |
|------|---------|
| No coding required | Requires Apex coding |
| Uses drag and drop | Uses programming |
| Easy for admins | Used by developers |
| Suitable for simple automation | Suitable for complex logic |

### Before Trigger vs After Trigger

| Before Trigger | After Trigger |
|---------------|---------------|
| Runs before saving record | Runs after saving record |
| Used for validation | Used for creating related records |
| Can modify field values | Cannot directly modify saved record |
| Faster processing | Used for post actions |

---

## 4. Trigger Use Cases

### Example 1
When Account checkbox "Match Billing Address" is selected, copy Billing Postal Code to Shipping Postal Code.

### Example 2
Create follow-up task when Opportunity stage becomes Closed Won.

### Example 3
Prevent deletion of Account if related Opportunities exist.

### Example 4
Send notification when Contact is created.

### Example 5
Automatically create Opportunity when Account is added.

---

## 5. Query Examples (English Query Ideas)

1. Get all Account names.

```sql
SELECT Name FROM Account
```

2. Get all Contacts.

```sql
SELECT Id, LastName FROM Contact
```

3. Get Closed Won opportunities.

```sql
SELECT Name FROM Opportunity WHERE StageName='Closed Won'
```

4. Get Accounts with postal codes.

```sql
SELECT Name, BillingPostalCode FROM Account
```

5. Get tasks related to opportunities.

```sql
SELECT Subject, WhatId FROM Task
```

---

## 6. Reflection

Enterprise systems react automatically to data changes because businesses handle large amounts of data.

Manual work causes delays and errors.

Triggers and automation help systems:

- Update records automatically
- Create related data
- Send notifications
- Maintain consistency
- Reduce manual work

This improves efficiency and supports large enterprise applications.
