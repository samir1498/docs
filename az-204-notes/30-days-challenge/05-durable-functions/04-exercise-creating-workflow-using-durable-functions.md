# Exercise - Create a Workflow using Durable Functions

In this exercise, we'll create an approval workflow in the Azure portal using Durable Functions. We'll follow the steps outlined to set up a Function App and create the necessary functions for our workflow.

## 1. Create a Function App

Follow the steps provided to create a Function App in the Azure portal. Ensure you select the appropriate settings, such as the runtime stack (Node.js) and the consumption plan.

## 2. Install the durable-functions npm package

Access the Function App in the Azure portal, and open the App Service Editor. Create a `package.json` file and add the necessary code to install the `durable-functions` package using npm.

## 3. Create the client function for submitting a design proposal

Create an HTTP-triggered function named `HttpStart` using the Durable Functions HTTP starter template. This function will initiate the orchestration process when triggered by an HTTP request.

## 4. Create the orchestrator function

Create an orchestrator function named `OrchFunction` using the Durable Functions orchestrator template. This function will orchestrate the execution of other functions in the workflow.

## 5. Create the activity function

Create an activity function named `Approval` using the Durable Functions activity template. This function will simulate the approval process for the project design proposal.

## 6. Verify that the durable functions workflow starts

Get the URL for the `HttpStart` function and trigger it using a web browser. Monitor the execution of the workflow by accessing the provided status query URL.

## Conclusion

In this exercise, we've created a workflow using Durable Functions in the Azure portal. We've set up the necessary functions and orchestrated their execution to simulate the approval process for project design proposals.

Next unit: Control long-running tasks using timers
