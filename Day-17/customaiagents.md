# Building Custom AI Agents – Agentforce Notes

## Building Custom AI Agents

Custom AI agents are created to automate specific business processes and interact with users using natural language.

### Key Steps

1. Define the business use case.
2. Create an agent.
3. Configure topics and actions.
4. Connect data sources and workflows.
5. Test and deploy the agent.

### Benefits

* Personalized automation.
* Faster business processes.
* Improved user experience.

---

## Agent Builder

**Agent Builder** is the Salesforce tool used to create and configure Agentforce agents.

### Capabilities

* Create and manage agents.
* Define topics.
* Configure actions.
* Test agent responses.
* Monitor agent performance.

### Components

* Agent Instructions
* Topics
* Actions
* Knowledge Sources
* Testing Tools

---

## Prompt-Driven Workflows

Prompt-driven workflows allow agents to use natural language instructions to determine the appropriate action.

### Process

1. User submits a request.
2. Agent interprets the prompt.
3. Agent selects the relevant topic.
4. Agent executes an action.
5. Agent returns the result.

### Example

User Prompt:

> "Create a support case for my login issue."

Agent Actions:

* Detects support request.
* Creates a case record.
* Returns the case number.

### Benefits

* Natural user interactions.
* Reduced manual navigation.
* Intelligent task execution.

---

## Record-Triggered Agent Actions

Record-triggered actions allow agents to respond automatically when Salesforce records are created or updated.

### Common Triggers

* New Case created.
* Opportunity updated.
* Lead assigned.
* Account modified.

### Example

When a high-priority Case is created:

1. Record trigger fires.
2. Agent reviews case details.
3. Agent recommends next steps.
4. Agent notifies the support team.

### Benefits

* Real-time automation.
* Faster response to business events.
* Reduced manual intervention.

---

### Quick Summary

**Building Custom AI Agents** → Create agents for specific business needs
**Agent Builder** → Tool for configuring Agentforce agents
**Prompt-Driven Workflows** → Agents act based on natural language requests
**Record-Triggered Agent Actions** → Agents automatically respond to record changes in Salesforce.
