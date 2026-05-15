# Apex Triggers – Notes

## Trigger Events
Apex Triggers are pieces of Apex code that run automatically when changes happen to Salesforce records.
They are used to automate actions and apply business rules.

### Common Trigger Events
* Before Insert
* Before Update
* Before Delete
* After Insert
* After Update
* After Delete

Triggers can run before or after records are saved in the database.
---

# Before Insert Trigger
A Before Insert trigger executes before a new record is stored in Salesforce.

### Purpose
* Validate data
* Set default field values
* Modify records before saving

### Example
```apex id="n2q1fr"
trigger ContactTrigger on Contact(before insert) {
    for(Contact c : Trigger.new){
        c.Description = 'New Contact';
    }
}
```

### Explanation
This trigger automatically adds “New Contact” in the Description field before the Contact record is saved.

---

# After Update Trigger
An After Update trigger runs after a record is updated and saved in the database.

### Purpose
* Send notifications
* Update related records
* Perform actions after data is committed

### Example
```apex id="m8t5zl"
trigger AccountTrigger on Account(after update) {
    System.debug('Account Updated');
}
```

### Explanation
This trigger executes after an Account record is updated and prints a message in debug logs.

---

# Business Logic
Business logic refers to rules and operations that automate business processes in Salesforce.

### Examples
* Automatically assign leads
* Send email alerts
* Update status fields
* Create follow-up tasks
* Validate important data

Triggers help businesses reduce manual work and maintain accurate data automatically.
