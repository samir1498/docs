# Create an HTTP trigger

In this unit, we're going to create a function that accepts an HTTP request with a single string. The function returns a string back to the caller to represent success or failure. We'll continue working on the function from the previous exercise.

1. Make sure you're signed into the Azure portal using the same account you activated the sandbox with.
2. On the Azure portal menu or from the Home page, under Azure services, select All resources.
3. Select your function app identified under the Type column. Your Function App pane appears.
4. Select the Functions tab in the center of the screen.
5. Select the Create button at the top of the Functions tab. This action starts the function creation process. The Create function pane appears.
6. In the Select a template section, select HTTP trigger.
7. In the Template details section, in New Function field, enter a name for the function. Scroll down and in the Authorization level dropdown list, select Anonymous, and then select Create. Your newly created Function pane appears.

## Get your function URL

Now that we've created the HTTP trigger, let's get the function URL so we can begin to make a request.

1. On the top menu bar, select Get Function Url. The Get Function Url dialog appears.
2. In the URL field, select the Copy to clipboard icon.

## Issue a GET request to your HTTP trigger

Let's issue a GET request for the URL to see if we get a response.

1. Open a new tab in your web browser.
2. Paste the URL into the address bar.
3. Add a query parameter called name with your name to the URL; for example, https://**your-webapp-name**.azurewebsites.net/api/HttpTrigger1?name=Jesse
4. Press Enter to submit the request.
5. The message, "Hello, Jesse. This HTTP triggered function executed successfully." displays.

## Next unit: Execute an Azure function when a blob is created
