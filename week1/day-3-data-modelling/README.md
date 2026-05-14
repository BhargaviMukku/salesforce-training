# Salesforce Training – Day 3 Assignment

# 1. Difference Between App, Object, Record, and Field

| Term | Meaning | Example |
| --- | --- | --- |
| App | A collection of related tabs, objects, and tools used for a specific purpose | College Management App |
| Object | A database table that stores related information | Student Object |
| Record | A single row of data inside an object | One student’s details |
| Field | A single piece of information in a record | Student Name, Roll Number |

## App

An app is like a complete workspace in Salesforce. It contains multiple objects and tools required for a particular task or department.

**Example:**  
A “College Management App” may contain Student, Faculty, Course, and Attendance objects.

---

## Object

An object is like a table in a database. It stores similar types of data.

**Example:**  
A Student object stores all student information.

| Student Name | Roll No | Branch |
| --- | --- | --- |
| Ravi | 101 | CSE |

---

## Record

A record is one complete entry inside an object.

**Example:**  
Ravi’s details form one record in the Student object.

---

## Field

A field stores a specific piece of information.

**Example Fields:**
- Student Name
- Roll Number
- Phone Number
- Email

---

# 2. Standard vs Custom Objects

| Standard Objects | Custom Objects |
| --- | --- |
| Already provided by Salesforce | Created by users |
| Used for common business needs | Used for organization-specific needs |
| Cannot be deleted | Can be deleted |
| Examples: Account, Contact, Opportunity | Examples: Student, Course, Attendance |

## Standard Objects

Salesforce provides standard objects by default.

**Examples:**
- Account
- Contact
- Lead
- Opportunity

These objects are commonly used in CRM systems for managing customer and business data.

---

## Custom Objects

Custom objects are created by users according to business requirements.

**Examples in College System:**
- Student
- Faculty
- Course
- Attendance

Custom objects help organizations store their own unique data.

---

# 3. College Data Model

## Objects Used

1. Student  
2. Faculty  
3. Course  
4. Attendance  

---

## Relationships

| Parent Object | Child Object | Relationship |
| --- | --- | --- |
| Faculty | Course | One-to-Many |
| Course | Student | Many-to-Many |
| Student | Attendance | One-to-Many |

---

# College Data Model Diagram

```text
+----------------+
|    Faculty     |
+----------------+
| Faculty ID     |
| Faculty Name   |
| Department     |
+----------------+
        |
        | teaches
        v
+----------------+
|     Course     |
+----------------+
| Course ID      |
| Course Name    |
| Credits        |
+----------------+
        |
        | enrolled by
        v
+----------------+
|    Student     |
+----------------+
| Student ID     |
| Student Name   |
| Branch         |
+----------------+
        |
        | has
        v
+----------------+
|   Attendance   |
+----------------+
| Date           |
| Status         |
+----------------+
```
# 4. Formula Fields

## Definition

Formula fields automatically calculate values based on other fields.

They reduce manual work and improve accuracy.

---

## Example 1 – Total Marks Percentage

### Fields Used
- Subject1 Marks
- Subject2 Marks
- Subject3 Marks

### Formula

```text
((Subject1__c + Subject2__c + Subject3__c) / 300) * 100
```

### Explanation

This formula calculates the percentage of marks obtained by a student.

---

## Example 2 – Full Name

### Formula

```text
First_Name__c & " " & Last_Name__c
```

### Explanation

This formula combines first name and last name into a full name automatically.

---

# 5. Validation Rules

## Definition

Validation rules ensure users enter correct data before saving records.

They improve data quality and reduce mistakes.

---

## Example 1 – Phone Number Validation

### Rule

```text
LEN(Phone__c) <> 10
```

### Error Message

```text
Phone number must contain exactly 10 digits.
```

### Explanation

This rule prevents users from entering invalid phone numbers.

---

## Example 2 – Age Validation

### Rule

```text
Age__c < 17
```

### Error Message

```text
Student age must be greater than or equal to 17.
```

### Explanation

This rule ensures only eligible students are admitted.

---

# 6. Reflection – Why Structured Enterprise Data Matters

Structured enterprise data is very important because it helps organizations store information in an organized and systematic way. In Salesforce, data is stored using objects, records, and fields, which makes it easy to manage and access.

Properly structured data improves:
- Accuracy
- Data security
- Reporting
- Decision-making
- Automation

For example, in a college management system, structured data helps track students, courses, attendance, and faculty details efficiently. It reduces duplicate information and saves time.

Enterprise data also helps organizations generate reports and insights quickly, which supports better business decisions. Without structured data, managing large amounts of information becomes difficult and confusing.

Therefore, structured enterprise data is essential for smooth operations and better productivity in any organization.


```text
((Subject1__c + Subject2__c + Subject3__c) / 300) * 100
