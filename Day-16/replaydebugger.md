# Salesforce Debugging Notes

## Replay Debugger

**Replay Debugger** is a Salesforce tool that lets developers debug Apex code using existing debug logs in **Visual Studio Code (VS Code)**.

### Features

* Step through Apex code line by line.
* Inspect variable values.
* Analyze execution flow without rerunning code.
* Debug directly from log files.

### Benefits

* Faster troubleshooting.
* No need to reproduce issues repeatedly.
* Works with captured debug logs.

---

## VS Code Debugging

**Visual Studio Code** is commonly used for Salesforce development and debugging.

### Steps

1. Install VS Code.
2. Install the Salesforce Extension Pack.
3. Authorize your Salesforce org.
4. Retrieve project metadata.
5. Open a debug log.
6. Launch Replay Debugger.

### Common Actions

* Step Over
* Step Into
* Step Out
* Continue Execution
* View Variables

---

## Apex Troubleshooting

Troubleshooting helps identify and resolve issues in Apex code.

### Common Errors

* Null Pointer Exception
* SOQL Query Exceptions
* DML Exceptions
* Governor Limit Errors

### Troubleshooting Process

1. Review the error message.
2. Generate or retrieve debug logs.
3. Analyze execution details.
4. Locate the problematic code.
5. Fix and retest.

### Example

If a variable is not initialized before use, Salesforce may throw a **NullPointerException**. Reviewing the debug log helps identify the exact line causing the issue.

---

## Enterprise Debugging Workflow

### Step 1: Identify the Issue

* Gather error details from users.
* Determine affected functionality.

### Step 2: Collect Logs

* Enable debug logs.
* Capture relevant transactions.

### Step 3: Analyze

* Review logs in Developer Console or VS Code.
* Trace execution flow.
* Identify exceptions and failures.

### Step 4: Find Root Cause

* Determine whether the issue is in Apex, Flow, Validation Rules, or Integrations.

### Step 5: Fix and Test

* Implement the solution.
* Perform testing in a Sandbox.
* Validate results.

### Step 6: Deploy

* Move changes to production using the deployment process.
* Monitor logs after deployment.

---

### Quick Summary

**Replay Debugger** → Debug Apex using log files
**VS Code Debugging** → Advanced debugging with Salesforce extensions
**Apex Troubleshooting** → Identify and resolve Apex errors
**Enterprise Debugging Workflow** → Collect logs → Analyze → Fix → Test → Deploy.
