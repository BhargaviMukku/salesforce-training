# Salesforce Training – Day 5 Assignment

# 1. What is Apex?

Apex is a programming language developed by Salesforce for building custom business logic and automation on the Salesforce platform. It is similar to Java and is used when declarative tools like Flow Builder are not enough to meet business requirements.

Apex allows developers to:
- Create custom automation
- Write complex business logic
- Integrate external systems
- Create custom APIs and services
- Process large amounts of data

Apex runs securely on Salesforce servers and works closely with Salesforce objects and records.

---

# 2. Difference Between Flow vs Apex and Configuration vs Coding

## Flow vs Apex

| Flow | Apex |
| --- | --- |
| Declarative tool | Programming language |
| Built using clicks | Built using code |
| Easy for admins | Requires coding skills |
| Best for simple automation | Best for complex logic |
| Faster development | More flexible and powerful |
| Easy to maintain | Requires developers |

---

## Configuration vs Coding

| Configuration | Coding |
| --- | --- |
| Uses clicks not code | Uses programming languages |
| Easy to implement | Requires technical skills |
| Faster deployment | More development time |
| Limited customization | Highly customizable |
| Used for standard business logic | Used for advanced requirements |

---

# 3. Real Examples Where Apex Is Needed

## 1. PDF Generation System

A college management system may need to generate student report cards in PDF format automatically. Since Flow Builder cannot generate PDFs directly, Apex is required.

---

## 2. External Payment Gateway Integration

If the college system connects with an external payment gateway for online fee payment, Apex APIs are needed to communicate with external systems.

---

## 3. Complex Attendance Processing

If attendance calculation involves advanced conditions such as percentage calculation across semesters and automatic detention logic, Apex is better suited for handling the complexity.

---

# 4. Integrated College Management System Design

## CRM

Salesforce CRM is used to manage all college-related activities such as:
- Student management
- Faculty management
- Attendance tracking
- Fee management
- Placement activities

The CRM centralizes all student and academic information in one system.

---

## Objects

| Object Name | Purpose |
| --- | --- |
| Student | Stores student details |
| Faculty | Stores faculty details |
| Course | Stores course information |
| Attendance | Stores attendance records |
| Fees | Stores fee payment details |
| Placement | Stores placement information |

---

## Relationships

| Parent Object | Child Object | Relationship |
| --- | --- | --- |
| Faculty | Course | One-to-Many |
| Course | Student | Many-to-Many |
| Student | Attendance | One-to-Many |
| Student | Fees | One-to-Many |
| Student | Placement | One-to-Many |

---

## Validation Rules

Validation rules ensure correct data entry.

### Examples
- Phone number must contain 10 digits
- Student age must be greater than 17
- Attendance percentage cannot exceed 100%
- Fee amount cannot be negative

---

## Flow Automation

### Attendance Alert Flow
If attendance falls below 75%, automatically send a warning notification to the student.

### Fee Reminder Flow
Automatically send fee reminder emails before the due date.

### Placement Notification Flow
Automatically notify eligible students about placement opportunities.

---

## Apex Usage

### PDF Report Card Generation
Apex generates downloadable student report cards.

### External API Integration
Apex connects the system with external payment services.

### Complex Result Calculation
Apex calculates semester grades and cumulative CGPA automatically.

---

# 5. Pseudocode Examples

## Example 1 – Attendance Warning Logic

```text
IF attendance_percentage < 75
THEN
    Send warning email to student
END IF
```
---
## Example 2 – Fee Reminder Logic

```text
IF fee_due_date is near
THEN
    Send reminder notification
END IF
```

---

## Example 3 – Placement Eligibility Logic

```text
IF CGPA >= 7.5
THEN
    Mark student as placement eligible
END IF
```

---

# 6. Reflection – Why Enterprise Systems Eventually Need Programming

Enterprise systems initially start with simple configurations and declarative tools like Flow Builder. However, as organizations grow, business processes become more complex and require advanced customization.

Programming becomes necessary because:
- Some business logic is too complex for declarative tools
- External system integrations require APIs
- Advanced automation requires custom logic
- Large-scale data processing needs better performance
- Custom user experiences require coding

In Salesforce, tools like Flow Builder can handle many common tasks, but Apex is needed for advanced enterprise requirements such as PDF generation, API integration, and complex calculations.

Therefore, enterprise systems eventually require programming to achieve scalability, flexibility, advanced automation, and better system integration.
