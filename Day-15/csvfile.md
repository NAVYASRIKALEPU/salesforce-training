# Salesforce Data Loader Notes

## Uploading CSV Data

A CSV (Comma-Separated Values) file is used to import records into Salesforce.

### Steps:

1. Open Data Loader.
2. Choose an operation (Insert, Update, Upsert).
3. Log in to Salesforce.
4. Select the object (Account, Contact, Lead, etc.).
5. Browse and select the CSV file.
6. Proceed to field mapping.
7. Execute the operation.

---

## Field Mapping

Field mapping connects CSV columns to Salesforce fields.

### Example

CSV File:

| Name     | Phone     |
| -------- | --------- |
| ABC Corp | 123456789 |

Salesforce Mapping:

| CSV Column | Salesforce Field |
| ---------- | ---------------- |
| Name       | Account Name     |
| Phone      | Phone            |

Data Loader can automatically match fields with the same names.

---

## Bulk Operations

Data Loader is designed to process large numbers of records efficiently.

### Common Bulk Operations

* **Insert** – Add new records.
* **Update** – Modify existing records.
* **Upsert** – Insert new records or update existing ones.
* **Delete** – Remove records.

### Benefits

* Saves time.
* Handles thousands of records at once.
* Reduces manual data entry.

---

## Real Examples

### Example 1: Import New Accounts

CSV:

| Name     | Phone     |
| -------- | --------- |
| ABC Corp | 123456789 |

Operation: **Insert**

Result: A new Account record is created.

---

### Example 2: Update Contacts

CSV:

| Id          | Email                                   |
| ----------- | --------------------------------------- |
| 003xx000123 | [user@email.com](mailto:user@email.com) |

Operation: **Update**

Result: Existing Contact email is updated.

---

### Example 3: Upsert Leads

CSV:

| Email                                 | Company |
| ------------------------------------- | ------- |
| [lead@test.com](mailto:lead@test.com) | ABC Ltd |

Operation: **Upsert** using Email as an External ID.

Result:

* Existing lead → Updated
* New lead → Created

### Quick Summary

**Upload CSV → Map Fields → Choose Bulk Operation → Run → Review Success/Error Files**.
