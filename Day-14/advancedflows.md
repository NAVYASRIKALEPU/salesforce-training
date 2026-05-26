# Advanced Flow Logic, Choices and Loops, Multi-Step Automation, and Invocable Apex

## Advanced Flow Logic

* Advanced flow logic helps create complex business automation in Salesforce.
* Logic controls how flows make decisions and perform actions.
* Decision elements are used to create conditions and branching paths.
* Helps automate real-world business scenarios efficiently.

### Features

* Conditional logic
* Dynamic record handling
* Automated decision making
* Multiple action paths

### Example

* If Amount > 50000 → Send Approval Request
* Else → Auto Approve Record

---

# Choices and Loops

## Choices

* Choices allow users to select options in Screen Flows.
* Used in dropdowns, radio buttons, and picklists.
* Helps collect user input dynamically.

### Example Choices

* Yes / No
* High / Medium / Low
* Department Selection

---

## Loops

* Loops process multiple records one by one inside a flow.
* Used for bulk data processing and repeated actions.
* Helps avoid repetitive manual operations.

### Uses of Loops

* Update multiple records
* Process collections
* Perform repeated calculations

### Example

* Loop through Accounts
* Update Account Status for each record

---

# Multi-Step Automation

* Multi-step automation performs several actions in sequence.
* Combines decisions, loops, updates, and notifications in one flow.
* Useful for complex business processes.

### Example Workflow

1. Record Created
2. Check Conditions
3. Update Related Records
4. Send Email Notification
5. Create Task
6. End Flow

### Benefits

* Reduces manual effort
* Improves process efficiency
* Automates enterprise workflows

---

# Invocable Apex

* Invocable Apex allows Apex methods to be called from Salesforce Flow.
* Used when Flow functionality alone is not enough.
* Helps integrate custom business logic with automation.

### Features

* Reusable Apex methods
* Flow integration
* Supports advanced processing

### Example

```apex id="7mk7gx"
public class AccountHelper {

    @InvocableMethod
    public static void updateAccounts(List<Id> accountIds) {

        List<Account> accounts = [
            SELECT Id, Name FROM Account
            WHERE Id IN :accountIds
        ];

        update accounts;
    }
}
```

### Advantages

* Extends Flow capabilities
* Supports complex logic
* Improves automation flexibility
* Combines low-code and pro-code development
