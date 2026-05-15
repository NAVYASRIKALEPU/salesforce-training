# Record Triggered Flow – Short Notes
## What is Record-Triggered Flow?
Salesforce Flow Builder Record-Triggered Flow is a type of Salesforce Flow that runs automatically when a record is created, updated, or deleted.

It is mainly used for automating tasks without manual action.

---
# When Flows Execute
### 1. Before Save Flow
* Runs before the record is saved
* Used for quick field updates
* Faster performance

### 2. After Save Flow
* Runs after the record is saved
* Used for creating tasks, sending emails, or updating related records

### 3. Delete Trigger Flow
* Runs when a record is deleted
---

# Real-World Examples
* Send welcome email when a new Contact is created
* Create follow-up task after Opportunity creation
* Update Account status automatically
* Notify manager when Case priority is high
* Auto-assign leads to sales representatives
