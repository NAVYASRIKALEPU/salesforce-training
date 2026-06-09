# Enterprise Architecture Notes

## Enterprise Architecture

Enterprise Architecture is the overall structure of an organization's technology systems, applications, data, and business processes.

### Goals

* Align technology with business objectives.
* Improve efficiency and maintainability.
* Support future growth.
* Enable integration between systems.

### Core Layers

### Presentation Layer

* LWC
* Mobile Apps
* Portals

### Business Logic Layer

* Apex Classes
* Flows
* Validation Rules

### Data Layer

* Salesforce Objects
* Databases
* External Data Sources

### Integration Layer

* REST APIs
* SOAP APIs
* Middleware

### Architecture Flow

```text
Users
  ↓
UI Layer (LWC)
  ↓
Business Logic (Apex/Flow)
  ↓
Data Layer
  ↓
External Systems
```

---

## System Design Thinking

System design focuses on creating applications that are reliable, maintainable, and efficient.

### Key Principles

### Modularity

Break applications into smaller reusable components.

Example:

* Account Component
* Contact Component
* Opportunity Component

### Separation of Concerns

Each layer has a specific responsibility.

* UI → Display information
* Apex → Business logic
* Database → Store data

### Reusability

Build components and services that can be used across multiple projects.

### Maintainability

Design systems that are easy to update and troubleshoot.

### Security

Protect data using permissions, roles, and sharing rules.

---

## Scalability Concepts

Scalability is the ability of a system to handle increasing workloads without performance issues.

### Types of Scalability

### Vertical Scaling

Increase resources of an existing system.

Examples:

* More CPU
* More Memory

### Horizontal Scaling

Add more servers or processing resources.

Examples:

* Multiple application servers
* Distributed services

### Salesforce Scalability Best Practices

* Use bulkified Apex code.
* Avoid SOQL and DML inside loops.
* Use asynchronous processing when appropriate.
* Optimize Flows and automation.
* Use efficient queries and indexes.

### Example

Poor Design:

```text
Loop
 └─ SOQL Query
```

Better Design:

```text
Single SOQL Query
      ↓
Process Records in Collection
```

### Benefits

* Faster performance.
* Better user experience.
* Reduced governor limit issues.
* Supports enterprise growth.

---

## Real-World Example

### Customer Support System

1. Customer submits a case.
2. LWC captures information.
3. Apex validates data.
4. Case record is created.
5. Flow assigns the case.
6. API notifies external systems.
7. Support team resolves the issue.

This architecture can support thousands of users because each layer has a clear responsibility and can scale independently.

---

## Quick Summary

| Topic                   | Purpose                                      |
| ----------------------- | -------------------------------------------- |
| Enterprise Architecture | Overall structure of enterprise applications |
| System Design Thinking  | Designing reliable and maintainable systems  |
| Scalability Concepts    | Handling growth and increased workloads      |

### Enterprise View

**Users → UI Layer → Business Logic → Data Layer → Integrations → Business Outcomes**.
