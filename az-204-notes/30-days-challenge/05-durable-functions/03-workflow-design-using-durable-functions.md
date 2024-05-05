# Workflow Design using Durable Functions

You can use Durable Functions to orchestrate a long-running workflow as a set of activities. Each step in the process can be mapped to a function type, and each task to an activity. Automated processes eliminate the need for manual monitoring or task escalation if they aren't completed in time.

## Description of the Design Approval Process

Our workflow begins when a project design is submitted for approval. The proposal is assigned as an approval task to a manager, who will either approve or reject it. If the approval task isn't completed within a predefined time limit, an escalation task is allocated.

### Workflow Steps

1. **Submitting a Project Design Proposal for Approval**
   - **Durable Function Type:** Client Function

2. **Assigning an Approval Task to Relevant Staff Member**
   - **Durable Function Type:** Orchestration Function

3. **Approval Task**
   - **Durable Function Type:** Activity Function

4. **Escalation Task**
   - **Durable Function Type:** Activity Function

### Representation of Workflow

The orchestration function will manage a rule in the workflow that starts the escalation activity if the approval activity doesn't return within a specified time.

Now that we understand the requirements for our workflow, we can proceed to write the code in the next unit!

Next unit: Exercise - Create a workflow using Durable Functions
