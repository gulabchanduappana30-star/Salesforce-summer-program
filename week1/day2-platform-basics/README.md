# Day 2 - Salesforce Platform Basics

## 1. What is Salesforce Platform?

Salesforce Platform is a cloud-based application development and CRM platform that helps businesses manage customer data, automate workflows, and build business applications.

It allows companies to:

* Store customer information
* Automate business processes
* Build custom applications
* Generate reports and dashboards
* Improve communication between teams

Salesforce provides both:

* No-code development
* Programmatic development

This makes the platform useful for both administrators and developers.

---

# 2. Important Salesforce Concepts

## App

An App in Salesforce is a collection of tools, objects, tabs, and features designed for a specific business process.

Apps help users access related functionality in one place.

### Example:

Dreamhouse App

The Dreamhouse app helps real estate brokers manage:

* Customers
* Properties
* Brokers
* Property sales

---

## Object

Objects are database tables in Salesforce used to store information.

Each object contains:

* Fields
* Records

### Types of Objects

### Standard Objects

Objects already provided by Salesforce.

Examples:

* Contact
* Account
* Lead

### Custom Objects

Objects created by users based on business requirements.

Examples:

* Property
* Broker Property

### Example:

The Contact object stores:

* Customer Name
* Phone Number
* Email
* Loan Amount

---

## Tab

Tabs help users access objects and features from the Salesforce interface.

Tabs make navigation easier.

### Examples:

* Contacts Tab
* Accounts Tab
* Properties Tab

Users can click tabs to open records quickly.

---

# 3. Difference Between Configuration and Coding

| Configuration (No-Code)  | Coding (Programmatic)     |
| ------------------------ | ------------------------- |
| Uses clicks and settings | Uses programming          |
| Easy for admins          | Used by developers        |
| Faster implementation    | More customization        |
| No coding required       | Coding knowledge required |
| Uses Flow Builder        | Uses Apex and Lightning   |

## Example 1

Creating a custom field using Setup menu is Configuration.

## Example 2

Writing Apex code for automation is Coding.

---

# 4. My System Design

## Application Used

Dreamhouse Application

## Objects Used

* Contact Object
* Property Object

## Customization Performed

Created a custom currency field:

* Loan Amount

## User Interaction Flow

1. Broker opens Dreamhouse application.
2. Broker opens Contact records.
3. Broker enters customer loan amount.
4. Salesforce stores loan information.
5. Broker uses the information to recommend suitable properties.

---

