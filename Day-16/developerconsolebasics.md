# Salesforce Developer Console Notes

## Developer Console Basics

The **Developer Console** is a Salesforce tool used to write, test, and debug Apex code and SOQL queries.

### Features

* Write and edit Apex classes and triggers.
* Execute Apex code.
* Run SOQL and SOSL queries.
* View debug logs.
* Analyze application performance.

### Opening Developer Console

1. Log in to Salesforce.
2. Click the **Gear Icon (⚙️)**.
3. Select **Developer Console**.

---

## Query Editor

The **Query Editor** is used to run SOQL and SOSL queries and view results.

### Steps

1. Open Developer Console.
2. Select the **Query Editor** tab.
3. Enter a SOQL query.
4. Click **Execute**.

### Example

```sql
SELECT Id, Name FROM Account
```

Result: Displays Account records with their IDs and names.

### Benefits

* Retrieve data quickly.
* Test SOQL queries.
* Verify records in Salesforce.

---

## Executing Apex

The **Execute Anonymous** window allows you to run Apex code without creating a class.

### Steps

1. Open Developer Console.
2. Click **Debug → Open Execute Anonymous Window**.
3. Enter Apex code.
4. Click **Execute**.

### Example

```apex
System.debug('Hello Salesforce!');
```

Result: Message appears in the debug log.

---

## Debugging Tools

Developer Console provides tools for troubleshooting and analyzing code.

### Common Tools

* **Logs** – View execution details.
* **Execution Log** – Track code execution step by step.
* **Stack Tree** – Shows execution hierarchy.
* **Execution Overview** – Summarizes processing time.
* **Checkpoints** – Inspect variable values during execution.

### Benefits

* Identify errors quickly.
* Trace code execution.
* Improve application performance.

### Quick Summary

**Developer Console** → Development and debugging tool
**Query Editor** → Run SOQL/SOSL queries
**Execute Anonymous** → Run Apex code instantly
**Debugging Tools** → Analyze logs, errors, and execution details.
