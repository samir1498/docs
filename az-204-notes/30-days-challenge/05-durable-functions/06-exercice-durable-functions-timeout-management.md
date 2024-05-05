# Exercise: Adding a Durable Timer for Timeout Management

To incorporate an escalation step into our workflow for handling delayed approval of project design proposals, we'll add a durable timer to control the timeout during the execution. Here's a step-by-step guide to completing this exercise:

## 1. Add the `moment` npm Package to Your Function App

- Sign in to the Azure portal.
- Navigate to your function app.
- Open the console.
- Run the following commands to install the required packages:

```bash
npm install typescript
npm install moment
```

## 2. Add an Escalation Activity to Your Function App

- Navigate to your function app.
- Create a new function named `Escalation` using the Durable Functions activity template.
- Replace the existing code in `index.js` with the provided code snippet.
- Save the function.

## 3. Update the Orchestrator Function to Use the Escalation Function

- Navigate to your orchestrator function (`OrchFunction`).
- Add a reference to the `moment` library.
- Replace the body of the function with the provided code snippet.
- Save the function.

## 4. Verify that the Durable Functions Workflow Starts

- Restart your function app.
- Obtain the URL of your `HttpStart` function.
- Use the URL to trigger the orchestrator function.
- Monitor the execution status using the provided endpoints.
- After 20 seconds, the timeout will occur, and the workflow will call the `Escalation` activity.
- Verify the completion status and output of the workflow.

By following these steps, you'll successfully incorporate a durable timer to manage timeout and handle the escalation step in your workflow. This ensures that project design proposals are processed in a timely manner, enhancing the efficiency of your approval process.
