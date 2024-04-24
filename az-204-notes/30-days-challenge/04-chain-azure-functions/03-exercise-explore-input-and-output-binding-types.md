# Exercise - Explore Input and Output Binding Types

In this exercise, we create a function that runs when it receives an HTTP request and responds to each request by returning a message.

## Step 1: Create a Function App

- Sign in to the Azure portal using the account that you used to activate the sandbox.
- Navigate to the Create a resource menu and select Compute > Function App.
- Fill in the required details such as Subscription, Resource Group, Function App name, Runtime stack, Version, and Region.
- Review your settings and select Create to provision and deploy the function app.

## Step 2: Create a Function

- Navigate to the Functions tab on the Overview page of your newly created function app.
- Select the Create in Azure portal button.
- Choose the HTTP trigger template and configure the settings such as Function name and Authorization level.
- Select Create and wait for the trigger function to propagate to your function app.

## Step 3: Test the Function

- In the command bar, select Get Function Url to obtain the function URL.
- Paste the function URL in a new browser tab and append a query string parameter, e.g., `?name=Joe`.
- Run the request in your browser and observe the response message.

## Step 4: Explore Code and Test Pane

- In the Azure portal, navigate to the Function menu and select Code + Test.
- Review the JavaScript code for your function, which accesses the request payload and sends an HTTP response.
- Explore the `function.json` configuration file to understand the function bindings.

## Step 5: Explore Binding Types

- In the Function menu, select Integration to access the Integration pane for your function.
- Notice the predefined trigger and output binding.
- Review the available input and output binding types, considering their potential use cases in a solution.

Through this exercise, you've learned how to create a function app, add a function with an HTTP trigger, and explore different input and output binding types available in Azure Functions.

Next unit: Read data with input bindings
