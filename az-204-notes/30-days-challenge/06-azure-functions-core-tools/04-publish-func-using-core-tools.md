# Publish a function to Azure using Core Tools

## Create a function app

1. **Create a function app**:
   - Use Azure management tools (Azure portal, Azure CLI, or Azure PowerShell) to create the required resources in Azure, including the function app and a storage account.
   - Consider the language runtime of the function app, ensuring it matches the language runtime of your local functions project.

## Publish to Azure

2. **Publish your functions project**:
   - Navigate to the functions project folder.
   - Run `func azure functionapp publish <app_name>` to publish your project to the specified function app in Azure.
   - `<app_name>` is the name of the target function app in Azure, not the name of your project folder.

   Example:
   ```bash
   func azure functionapp publish my-function-app
   ```

   - Core Tools access your Azure subscriptions and resources using the session information from Azure CLI or Azure PowerShell. Ensure you are signed in to either of these tools before publishing.

3. **After publishing**:
   - Core Tools don't validate or test your functions code during publishing. Ensure to use `func start` for testing before publishing.
   - Any existing functions in the target app are stopped and deleted before deploying your project.
   - You cannot combine functions from multiple projects into one app by publishing them in sequence. All functions must be in one project.
   - Publishing to Azure doesn't create a relationship between the local project and the target function app.
   - You can publish a single functions project to multiple function apps.
   - Republish your project to the same app repeatedly as you work on your code.

## Things to know

- The invocation URLs displayed after you publish might include a code parameter in the query string.
- You can see it in the screenshot: ?code=4FowT1ywMNoxqa...
- HTTP trigger functions have an authorization level of function, which requires you to pass a secret function key in the request headers or query string.
- Core Tools returns the key in the query string of the displayed URL, for your convenience.
