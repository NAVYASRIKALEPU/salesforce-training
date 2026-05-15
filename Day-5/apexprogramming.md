# Apex & Salesforce CLI – Short Notes

## Collections
Apex Collections are used to store multiple values.

### Types
* List → Ordered collection
* Set → Unique values
* Map → Key-value pairs

### Example
```apex id="8dq8r6"
List<String> names = new List<String>();
```

# Logic Building
Logic building means creating step-by-step conditions and processes in code.

### Common Logic Tools
* Variables
* Loops
* Conditions
* Methods

### Purpose
* Automate decisions
* Process data efficiently
---

# Exception Handling
Exception handling is used to manage errors without stopping the program.

### Example
```apex id="g8ixht"
try{
   Integer a = 10/0;
}
catch(Exception e){
   System.debug(e);
}
```

### Benefit
* Prevents system crashes
* Handles errors safely

---

# Salesforce CLI Basics
Salesforce CLI is a command-line tool used for Salesforce development and deployment.

### Uses
* Create projects
* Authorize orgs
* Deploy code
* Run tests

### Example Command
```bash
sfdx force:org:list
```
Displays authorized Salesforce orgs.
