# Trigger Lifecycle – Notes

## What is Trigger Lifecycle?
Apex Trigger lifecycle refers to the sequence of events that occur when a Salesforce record is created, updated, or deleted.

Triggers execute automatically during different stages of record processing.
---

# Trigger Lifecycle Flow
### 1. Record Action Happens
A user or system creates, updates, or deletes a record.

### 2. Before Trigger Executes
Runs before the record is saved.

#### Uses
* Validate data
* Update field values
* Check conditions

### 3. Record Saved to Database
Salesforce stores the record.

### 4. After Trigger Executes
Runs after the record is saved.

#### Uses
* Send notifications
* Update related records
* Perform additional automation

---

# Automation Flow
Triggers work together with Salesforce automation tools like:

* Flows
* Validation Rules
* Process Automation
* Workflows

This helps automate complete business processes efficiently.
---

# Real-World Examples
## Example 1 – Lead Assignment
When a new Lead is created:

1. Before Insert trigger checks lead source
2. Record gets saved
3. After Insert trigger assigns lead to sales representative
---

## Example 2 – Order Processing
When an Order status changes:

* Trigger updates inventory
* Sends confirmation email
* Creates delivery task automatically
---

## Example 3 – Employee Management
When a new employee record is added:

* Trigger generates employee ID
* Sends welcome notification
* Creates onboarding tasks automatically
