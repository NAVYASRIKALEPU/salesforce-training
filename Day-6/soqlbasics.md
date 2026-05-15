# SOQL Basics – Notes

## What is SOQL?
SOQL (Salesforce Object Query Language) is used to retrieve data from Salesforce objects.
It is similar to SQL but works specifically with Salesforce data.

---
# Query Syntax
## Basic Syntax
```sql
SELECT FieldName FROM ObjectName
```

### Example
```sql
SELECT Name FROM Account
```

Retrieves the Name field from the Account object.
---

# Retrieving Records
## Retrieve Multiple Fields
```sql
SELECT Name, Email FROM Contact
```

## Retrieve Specific Records
```sql
SELECT Name FROM Contact WHERE City = 'Mumbai'
```

## Retrieve Limited Records
```sql
SELECT Name FROM Account LIMIT 5
```

## Sort Records
```sql
SELECT Name FROM Account ORDER BY Name
```

---
# Real Examples
## Get All Accounts
```sql
SELECT Name FROM Account
```

## Get Contacts with Email
```sql
SELECT Name, Email FROM Contact
```

## Get Opportunities Above Amount
```sql
SELECT Name, Amount FROM Opportunity WHERE Amount > 50000
```

## Get Recently Created Leads
```sql
SELECT Name FROM Lead ORDER BY CreatedDate DESC
```

# Uses of SOQL
* Retrieve Salesforce data
* Filter records
* Generate reports
* Use data in Apex and Flows
* Work with automation and integrations
