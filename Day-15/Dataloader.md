# Salesforce Data Loader – Beginner Notes

## 1. What is Data Loader?

**Data Loader** is a Salesforce client application used to **insert, update, upsert, delete, export, and export all Salesforce records** in bulk.

### Features

* Handles large volumes of data (up to millions of records).
* Supports CSV files.
* Can schedule data operations.
* Available for Windows and macOS.

---

# 2. Installing Data Loader

### Step 1: Login to Salesforce

* Open Salesforce.
* Click **Setup**.

### Step 2: Download Data Loader

* Search for **Data Loader** in Setup Quick Find.
* Open **Data Loader**.
* Click **Download Data Loader**.

### Step 3: Install

* Run the installer.
* Follow the installation wizard.
* Launch Data Loader after installation.

### Step 4: Login

* Open Data Loader.
* Select your environment:

  * Production
  * Sandbox
* Enter Salesforce credentials.
* Complete authentication.

---

# 3. Importing Data

Importing means adding or updating records in Salesforce from a CSV file.

## Supported Operations

### Insert

Creates new records.

Example:

| Name     | Phone  |
| -------- | ------ |
| ABC Corp | 123456 |

Result: New Account record is created.

---

### Update

Modifies existing records.

Requires:

* Salesforce Record ID
* External ID

Example:

| Id          | Phone  |
| ----------- | ------ |
| 001xx000123 | 987654 |

Result: Existing record is updated.

---

### Upsert

Combination of:

* Insert
* Update

If record exists → Update

If record doesn't exist → Insert

Uses:

* Salesforce ID
* External ID

---

## Steps to Import Data

1. Open Data Loader.
2. Select **Insert**, **Update**, or **Upsert**.
3. Login to Salesforce.
4. Select Object (Account, Contact, Lead, etc.).
5. Browse and select CSV file.
6. Click **Next**.
7. Map CSV fields to Salesforce fields.
8. Save mapping (optional).
9. Click **Finish**.
10. Review success and error files.

---

# 4. Export Data

Export retrieves Salesforce records into a CSV file.

## Why Export?

* Backup data.
* Reporting.
* Data analysis.
* Migration.

---

## Steps for Export

1. Open Data Loader.
2. Click **Export**.
3. Login.
4. Select object.
5. Choose output CSV location.
6. Create SOQL query or select fields.
7. Click **Finish**.
8. CSV file is generated.

---

# 5. Export All

### Difference Between Export and Export All

| Export              | Export All                           |
| ------------------- | ------------------------------------ |
| Active records only | Includes deleted records             |
| Regular backup      | Recovery purposes                    |
| Most common         | Used when deleted records are needed |

---

## Steps for Export All

1. Open Data Loader.
2. Click **Export All**.
3. Select object.
4. Choose output file.
5. Run export.

Result:

* Active records
* Records in Recycle Bin

---

# 6. Field Mapping

Field mapping connects CSV columns with Salesforce fields.

Example:

| CSV Column   | Salesforce Field |
| ------------ | ---------------- |
| AccountName  | Name             |
| AccountPhone | Phone            |
| WebsiteURL   | Website          |

### Auto-Match

Data Loader automatically maps fields with matching names.

---

# 7. Success and Error Files

After every operation Data Loader creates:

### Success File

Contains:

* Successfully processed records
* Salesforce IDs

### Error File

Contains:

* Failed records
* Error messages

Example Errors:

* Required field missing
* Invalid picklist value
* Duplicate records
* Validation rule failure

---

# 8. Beginner Workflow

### Scenario: Import New Accounts

#### Step 1

Prepare CSV:

| Name     | Phone | Website |
| -------- | ----- | ------- |
| ABC Corp | 12345 | abc.com |

#### Step 2

Open Data Loader.

#### Step 3

Select **Insert**.

#### Step 4

Choose **Account** object.

#### Step 5

Select CSV file.

#### Step 6

Map fields.

#### Step 7

Click **Finish**.

#### Step 8

Review success/error files.

#### Step 9

Verify records in Salesforce.

---

# 9. Best Practices

✅ Always backup data before updates or deletes.

✅ Test with a small number of records first.

✅ Validate CSV data before importing.

✅ Use External IDs for Upsert operations.

✅ Check success and error logs after every run.

✅ Use Sandbox for testing.

---

# Quick Revision

| Operation  | Purpose                           |
| ---------- | --------------------------------- |
| Insert     | Create new records                |
| Update     | Modify existing records           |
| Upsert     | Insert or Update                  |
| Delete     | Remove records                    |
| Export     | Download active records           |
| Export All | Download active + deleted records |

### Data Loader Workflow

**Prepare CSV → Open Data Loader → Login → Choose Operation → Select Object → Map Fields → Execute → Review Success/Error Files → Verify Data**

These notes cover the essentials of **Installing Data Loader, Importing Data, Export/Export All, and the Beginner Workflow** for Salesforce beginners.
