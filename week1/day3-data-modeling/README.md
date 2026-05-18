# Day 3 – Data Modeling

# 1. Difference Between App, Object, Record and Field

## 1.1 App

App is a collection of related tabs, objects and tools.

Example:

Student Management App

It can contain:

- Student Object
- Course Object
- Faculty Object

---

## 1.2 Object

Object stores data.

Examples:

- Student
- Course
- Faculty
- Department

Think of object like a table.

Example:

Student Object stores student information.

---

## 1.3 Record

Record means one row of data inside an object.

Example:

Student Object

Student Name: Rahul

Roll Number: 101

Department: CSE

This complete information is one record.

---

## 1.4 Field

Field stores individual values.

Examples:

- Student Name
- Email
- Phone Number
- Roll Number
- Department

Field is like a column in a table.

---

# 2. Standard Objects vs Custom Objects

## 2.1 Standard Objects

Standard objects are already available in Salesforce.

Examples:

1. Account
2. Contact
3. Lead
4. Opportunity

No need to create them manually.

---

## 2.2 Custom Objects

Custom objects are created by users according to requirements.

Examples:

1. Student__c
2. Course__c
3. Department__c
4. Faculty__c

These are created manually.

---

# 3. College Data Model

## 3.1 Objects Used

1. Student

2. Course

3. Faculty

4. Department

---

## 3.2 Relationships

1. Department → Student

One department can contain many students.

Example:

CSE Department

- Student 1
- Student 2
- Student 3

---

2. Department → Faculty

One department can have many faculty members.

Example:

ECE Department

- Faculty A
- Faculty B

---

3. Course → Student

Students can enroll in courses.

Example:

Python Course

- Rahul
- Ram
- Priya

---

4. Faculty → Course

Faculty teaches courses.

Example:

Faculty: Mr. Kumar

Course: Database Management

---

## 3.3 College Data Model Diagram

(Add screenshot image here)

![College Data Model](images/college-data-model.png)

---

# 4. Formula Fields

Formula field automatically calculates values.

## Example 1

Field Name:

Total_Fees

Formula:

Tuition Fee + Hostel Fee

Example:

Tuition Fee = 50000

Hostel Fee = 20000

Result:

Total Fees = 70000

---

## Example 2

Field Name:

Full_Name

Formula:

First Name + Last Name

Example:

First Name = Rahul

Last Name = Kumar

Result:

Rahul Kumar

---

Formula fields update automatically.

Add screenshot:

![Formula Field](images/formula-field.png)

---

# 5. Validation Rules

Validation rules prevent wrong data entry.

## Example 1

Phone number must contain 10 digits.

Rule:

LEN(Phone)=10

Correct Example:

9876543210

Wrong Example:

98765

System shows error.

---

## Example 2

Age must be greater than 18.

Rule:

Age > 18

Correct Example:

20

Wrong Example:

15

System will not save.

---

Add screenshot:

![Validation Rule](images/validation-rule.png)

---

# 6. Reflection – Why Structured Enterprise Data Matters

Structured enterprise data is important because:

1. Keeps information organized

2. Improves data accuracy

3. Reduces duplicate records

4. Makes reports easier

5. Helps automation

6. Improves business decisions

7. Saves time

8. Improves data management

Example:

Without structure:

Student data may be repeated many times.

With structure:

Data becomes clean and easy to manage.
