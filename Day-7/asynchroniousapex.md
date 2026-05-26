# Asynchronous Processing and Background Jobs

## Async Processing

* Asynchronous processing means tasks run separately from the main program flow.
* It allows long-running operations to execute without slowing down the system.
* Improves application performance and user experience.
* Common in Salesforce for handling large data operations.
* Examples include Future Methods, Queueable Apex, and Batch Apex.

---

## Background Jobs

* Background jobs are tasks that run automatically in the background.
* They do not require continuous user interaction.
* Used for data processing, email sending, reports, and scheduled tasks.
* Helps manage heavy workloads efficiently.
* In Salesforce, jobs can be monitored through the Apex Jobs page.

---

## Why Systems Need Async Execution

* Prevents system delays during heavy operations.
* Improves speed and responsiveness for users.
* Handles large amounts of data efficiently.
* Allows multiple tasks to run independently.
* Reduces chances of system timeout or performance issues.
* Supports scalable and reliable enterprise applications.
