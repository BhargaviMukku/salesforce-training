# 1. What is SOQL?

SOQL (Salesforce Object Query Language) is a query language used in Salesforce to retrieve data from objects such as Account, Contact, Lead, and custom objects. It is similar to SQL but designed specifically for Salesforce. Developers use SOQL in Apex classes, triggers, and Developer Console to search and access records stored in Salesforce.

Example:
SELECT Name, Phone FROM Account

This query retrieves the Name and Phone fields from the Account object.

---

# 2. What is an Apex Trigger?

An Apex Trigger is a piece of Apex code that executes automatically when specific actions happen on Salesforce records, such as insert, update, delete, or undelete operations.

Triggers help automate business logic in Salesforce.

Example:
- Automatically create a task when an order is shipped.
- Send notifications when records are updated.
- Validate data before saving records.

Triggers run either before or after database events.

---

# 3. Difference

## Flow vs Trigger

| Flow | Trigger |
|------|------|
| Mostly created using clicks, not code | Written using Apex code |
| Easier for admins | Used mainly by developers |
| Good for simple automation | Good for complex logic |
| Can use screens and UI | Runs completely in backend |
| Slower for very large operations | Better performance for bulk operations |

## Before Trigger vs After Trigger

| Before Trigger | After Trigger |
|------|------|
| Runs before data is saved | Runs after data is saved |
| Used for validation or updating fields | Used for related records and notifications |
| Faster because record is not committed yet | Used when record ID is needed |
| Example: Set default values | Example: Create related task |

---

# 4. Your Trigger Use Cases

## Example 1 – Welcome Email Trigger
When a new customer record is created, automatically send a welcome email.

## Example 2 – Task Creation Trigger
When an order status changes to “Shipped”, automatically create a follow-up task.

## Example 3 – Attendance Alert Trigger
If student attendance falls below 75%, automatically notify the student.

## Example 4 – Salary Approval Trigger
When employee salary exceeds a limit, automatically send approval request to manager.

## Example 5 – Inventory Update Trigger
When a product is sold, automatically reduce stock quantity in inventory.

---

# 5. Query Examples (English Query Ideas)

## Example 1
Find all accounts located in Hyderabad.

SOQL:
SELECT Name FROM Account WHERE BillingCity='Hyderabad'

## Example 2
Find contacts whose last name is Smith.

SOQL:
SELECT Id, Name FROM Contact WHERE LastName='Smith'

## Example 3
Find all employees with salary greater than 50000.

SOQL:
SELECT Name, Salary__c FROM Employee__c WHERE Salary__c > 50000

## Example 4
Find all orders that are shipped.

SOQL:
SELECT Name, Status__c FROM Order__c WHERE Status__c='Shipped'

## Example 5
Find students with attendance below 75%.

SOQL:
SELECT Name, Attendance__c FROM Student__c WHERE Attendance__c < 75

---

# 6. Reflection – Why Enterprise Systems React Automatically to Data Changes

Enterprise systems handle huge amounts of data every day. Manual monitoring and updates are slow and error-prone. Automatic reactions through flows, triggers, and automation tools help businesses respond instantly to important data changes.

For example:
- Notifications can be sent immediately.
- Tasks can be created automatically.
- Data can stay accurate and updated.
- Customer service becomes faster.
- Business processes become more efficient.

Automation improves productivity, reduces human errors, saves time, and helps organizations manage operations smoothly in real time.
