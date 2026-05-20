# Day 5 – Apex Introduction

## 1. What is Apex?

Apex is an object-oriented programming language developed by Salesforce. It is used to write custom business logic and automate processes inside the Salesforce platform.

Apex is similar to Java and C#.

Apex runs directly on the Salesforce Lightning Platform and works closely with database objects.

### Features of Apex

1. Object-oriented language
2. Supports classes and methods
3. Uses SOQL and SOSL queries
4. Supports triggers
5. Supports exception handling
6. Executes in cloud environment

### Example

```apex
public class HelloWorld {

    public static void printMessage(){

        String msg='Hello World';

        System.debug(msg);

    }

}
```

This code prints:

Hello World

---

## 2. Difference

### Flow vs Apex

| Flow | Apex |
|-------|-------|
| No-code automation | Code-based automation |
| Uses drag and drop | Uses programming |
| Easy for admins | Used by developers |
| Limited logic | Complex logic possible |
| Faster setup | More flexible |
| Less maintenance | Needs testing |

### Example

Flow Example:

Lead Created

↓

Check Matching Account

↓

Update Record

Apex Example:

```apex
trigger AccountTrigger on Account(before insert){

AccountTriggerHandler.CreateAccounts(
Trigger.New
);

}
```

---

### Configuration vs Coding

| Configuration | Coding |
|--------------|--------|
| Point and click | Write code |
| Uses Flow | Uses Apex |
| Quick setup | Complex setup |
| Less customization | High customization |
| Admin friendly | Developer focused |

Example:

Configuration:

Validation Rule

```text
Amount > 0
```

Coding:

```apex
if(amount<=0){

throw new Exception();

}
```

---

## 3. Real Examples Where Apex Is Needed

### Example 1 – Automatic Fee Calculation

Problem:

Student fee depends on:

- Course
- Hostel
- Scholarship
- Transport

Flow becomes complex.

Apex solution:

```apex
calculateFee();
```

System calculates total fee automatically.

---

### Example 2 – Attendance Alert System

Condition:

Attendance < 75%

Action:

Send warning email.

Logic:

```apex
if(attendance<75){

sendEmail();

}
```

---

### Example 3 – Placement Eligibility

Conditions:

CGPA > 7

Attendance > 80

No backlogs

Logic:

```apex
if(cgpa>7 &&
attendance>80 &&
backlogs==0){

eligible=true;

}
```

---

## 4. Integrated System Design – College Management System

### CRM Layer

CRM manages:

1. Student data
2. Faculty records
3. Courses
4. Attendance
5. Placements
6. Fees

---

### Objects

Student Object

Fields:

- Student ID
- Name
- Department
- Semester
- CGPA

Faculty Object

Fields:

- Faculty ID
- Subject
- Department

Course Object

Fields:

- Course ID
- Credits
- Duration

Attendance Object

Fields:

- Present Days
- Total Days

Placement Object

Fields:

- Company
- Package
- Status

---

### Relationships

Student

↓

Department

↓

Course

↓

Attendance

↓

Placement

Relationship Types:

1. Lookup Relationship
2. Master Detail Relationship

Example:

Student

↓

Attendance

Master Detail

Student

↓

Placement

Lookup

---

### Validation Rules

Rule 1:

Attendance cannot exceed total days.

```text
Attendance <= TotalDays
```

Rule 2:

CGPA range:

```text
CGPA >=0
CGPA <=10
```

Rule 3:

Fee cannot be negative.

```text
Fee > 0
```

---

### Flow Usage

Flow 1:

Student registered

↓

Create student record

↓

Assign department

↓

Send confirmation email

Flow 2:

Attendance updated

↓

Check percentage

↓

Send alert

Flow 3:

Placement selected

↓

Update status

↓

Notify student

---

### Apex Usage

Apex handles:

1. Fee calculation
2. Placement eligibility
3. Scholarship calculation
4. Bulk attendance processing
5. Email automation

Example:

```apex
public static Boolean checkEligibility(){

if(
cgpa>=7 &&
attendance>=80
){

return true;

}

return false;

}
```

---

## 5. Pseudocode Examples

### Example 1 – Attendance Check

START

Input attendance

IF attendance < 75

Send alert

ELSE

Continue

END

---

### Example 2 – Placement Check

START

Input CGPA

IF CGPA > 7

Eligible

ELSE

Not Eligible

END

---

### Example 3 – Fee Calculation

START

Base Fee

+ Hostel Fee

+ Transport Fee

- Scholarship

Return Total Fee

END

---

## 6. Reflection – Why Enterprise Systems Eventually Need Programming

Enterprise systems start with configuration tools such as Flow and Validation Rules.

As business complexity increases, coding becomes necessary.

Reasons:

1. Complex logic handling
2. Large data processing
3. Integration with external systems
4. Custom automation
5. Scalability
6. Performance optimization

Examples:

Banking:

Loan eligibility calculation

Hospital:

Patient priority handling

College:

Placement eligibility system

E-commerce:

Discount engine

Programming helps enterprise systems manage advanced requirements efficiently.

---
