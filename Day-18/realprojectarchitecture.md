# Salesforce Project Architecture Notes

## Real Project Architecture

A typical Salesforce enterprise application follows a layered architecture:

### Architecture Flow

**User → LWC → Apex Controller → Database/Business Logic → Response → LWC**

### Components

* **LWC (Lightning Web Components)** – User Interface
* **Apex Classes** – Business Logic
* **SOQL/SOSL** – Data Retrieval
* **Objects & Records** – Data Storage
* **Flows/Agentforce** – Process Automation

### Benefits

* Clear separation of responsibilities.
* Easier maintenance.
* Better scalability.

---

## LWC + Apex Integration

LWC communicates with Apex to retrieve or update Salesforce data.

### Process

1. User performs an action in LWC.
2. LWC calls an Apex method.
3. Apex processes data.
4. Salesforce returns the result.
5. LWC displays the response.

### Example

Customer clicks **"View Orders"**

* LWC sends request.
* Apex retrieves order records.
* Data is displayed on the screen.

### Advantages

* Fast data processing.
* Secure server-side logic.
* Reusable business logic.

---

## Validation Logic

Validation logic ensures data quality before records are saved.

### Common Validation Rules

* Required fields must be completed.
* Email format must be valid.
* Amount cannot be negative.
* Close Date cannot be in the past.

### Example

If an Opportunity Amount is less than 0:

* Validation rule prevents saving.
* User receives an error message.

### Benefits

* Accurate data.
* Reduced business errors.
* Consistent records.

---

## Component Communication

LWC components often need to exchange data.

### Parent → Child Communication

Uses **@api** properties.

Example:

* Parent sends Account ID to Child.

### Child → Parent Communication

Uses **Custom Events**.

Example:

* Child notifies Parent when a button is clicked.

### Unrelated Components

Use:

* Message Service (LMS)
* Pub/Sub (older approach)

### Benefits

* Better modular design.
* Reusable components.
* Cleaner code structure.

---

## Enterprise Workflow Thinking

Enterprise solutions focus on complete business processes rather than individual screens.

### Example: Case Management Workflow

1. Customer submits issue.
2. LWC captures details.
3. Apex validates information.
4. Case record is created.
5. Flow routes the case.
6. Agentforce assists support agents.
7. Notifications are sent.
8. Issue is resolved and closed.

### Key Principles

* Think end-to-end.
* Automate repetitive tasks.
* Maintain data integrity.
* Design for scalability.
* Build reusable components.

---

## Quick Summary

| Topic                        | Purpose                             |
| ---------------------------- | ----------------------------------- |
| Real Project Architecture    | Organizes application layers        |
| LWC + Apex Integration       | Connects UI with business logic     |
| Validation Logic             | Ensures correct data                |
| Component Communication      | Shares data between LWCs            |
| Enterprise Workflow Thinking | Designs complete business processes |

### Enterprise Flow

**User → LWC → Apex → Validation → Database → Flow/Automation → Response → User**.
