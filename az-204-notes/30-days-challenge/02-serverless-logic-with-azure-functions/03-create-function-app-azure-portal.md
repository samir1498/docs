# Exercise - Create a Function App in the Azure Portal

## Choose Your Development Language

You're now ready to start implementing the temperature service. In the previous unit, you determined that a serverless solution would best fit your needs. Let's start by creating a function app to hold our Azure Function.

### What is a Function App?

Functions are hosted in an execution context called a function app. You define function apps to logically group and structure your functions and a compute resource in Azure. In our escalator example, you would create a function app to host the escalator drive gear temperature service. There are a few decisions that need to be made to create the function app; you need to choose a service plan and select a compatible storage account.

### Choose a Service Plan

Function apps may use one of the following hosting plans:

- Consumption plan
- Premium plan
- Dedicated (App service) plan

When using the Azure serverless application platform, choose the Consumption plan. This plan provides automatic scaling and bills you only when your functions are running. The Consumption plan comes with a configurable timeout period for executing a function. By default, it's five (5) minutes, but may be configured to have a timeout as long as 10 minutes.

### Storage Account Requirements

When you create a function app, it must be linked to a storage account. You can select an existing account or create a new one. The function app uses this storage account for internal operations, such as logging function executions and managing execution triggers. On the Consumption plan, this storage account is also where the function code and configuration file are stored.

### Create a Function App

1. **Sign in to the Azure portal** using your Azure account.
2. Under **Azure services**, select **Create a resource**.
3. In the menu, select **Compute**, and then search for and select **Function App**. Select the **Create** button.
4. Follow the instructions provided in the **Create Function App** pane, providing necessary details like subscription, resource group, function app name, runtime stack, region, and hosting options and plans.
5. Select **Next: Storage** and provide necessary storage details.
6. Select **Review + create**, and then select **Create**. Deployment takes a few minutes. You receive a notification when deployment is completed.

### Verify Your Azure Function App

1. When deployment completes, select **Go to resource**. The Function App pane for your escalator function appears.
2. In the **Essentials** section, select the **URL link** to open it in a browser. A default Azure web page appears with a message that your Functions app is up and running.
