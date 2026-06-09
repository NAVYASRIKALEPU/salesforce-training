# Salesforce Data Loader Notes

## Insert Records

The **Insert** operation is used to add new records to Salesforce from a CSV file.

### Example

| Name     | Phone     |
| -------- | --------- |
| ABC Corp | 123456789 |

Result: A new Account record is created.

---

## Update Records

The **Update** operation modifies existing Salesforce records.

### Requirements

* Salesforce Record ID or External ID.
* Updated values in the CSV file.

### Example

| Id          | Phone     |
| ----------- | --------- |
| 001XX000123 | 987654321 |

Result: The existing Account phone number is updated.

---

## Delete Records

The **Delete** operation removes records from Salesforce.

### Requirements

* Salesforce Record IDs in the CSV file.

### Example

| Id          |
| ----------- |
| 001XX000123 |

Result: The record is deleted and moved to the Recycle Bin.

---

## Bulk Operations

Data Loader supports processing large numbers of records at once.

### Common Bulk Operations

* Insert
* Update
* Upsert
* Delete
* Export

### Benefits

* Faster processing of large datasets.
* Reduces manual effort.
* Improves data management efficiency.

---

## Enterprise Data Handling

Organizations use Data Loader to manage large volumes of Salesforce data.

### Common Uses

* Data migration between systems.
* Mass updates of customer information.
* Regular data backups using Export.
* Bulk deletion of obsolete records.

### Best Practices

* Always back up data before updates or deletes.
* Test operations in a Sandbox first.
* Verify field mappings carefully.
* Review success and error files after execution.

### Quick Summary

**Insert** = Add records
**Update** = Modify records
**Delete** = Remove records
**Bulk Operations** = Process thousands of records efficiently
**Enterprise Data Handling** = Manage large-scale Salesforce data securely and effectively.
