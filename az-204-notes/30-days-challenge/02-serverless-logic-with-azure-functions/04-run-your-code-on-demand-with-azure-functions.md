# Run Your Code On-Demand with Azure Functions

## Triggers

Functions are event driven, which means they run in response to an event. The type of event that starts a function is called a trigger. Each function must be configured with exactly one trigger.

You can trigger function execution by using HTTP requests, a scheduled timer, and events from the following Azure services:

- Blob Storage
- Azure Cosmos DB
- Event Grid
- Event Hubs
- Queue Storage
- Service Bus

## Bindings

A binding is a declarative way to connect data and services to your function. Bindings interact with various data sources, which means you don't have to write the code in your function to connect to data sources and manage connections. Each binding has a direction: Your code reads data from input bindings, and writes data to output bindings. Each function can have zero or more bindings to manage the input and output data processed by the function.

## Define a Sample Binding

Imagine you want to write a new row to Azure Table storage whenever a new message appears in Azure Queue Storage. You can implement this scenario using an Azure Queue Storage trigger and an Azure Table storage output binding. Example:

```json
{
  "bindings": [
    {
      "name": "order",
      "type": "queueTrigger",
      "direction": "in",
      "queueName": "myqueue-items",
      "connection": "MY_STORAGE_ACCT_APP_SETTING"
    },
    {
      "name": "$return",
      "type": "table",
      "direction": "out",
      "tableName": "outTable",
      "connection": "MY_TABLE_STORAGE_ACCT_APP_SETTING"
    }
  ]
}
```

## Create a Function in the Azure Portal

Azure Functions has predefined function templates, which are based on a specific type of trigger. These templates, in your chosen language, make it easy to get started creating your first function.

Selecting a template from the Add function pane provides easy access to the most common development environments, triggers, and dependencies. When you create a function in the Azure portal, you can choose from more than 20 templates. Once created, you can further customize the code.

## Navigate to Your Function and Its Files

You can create or edit functions for your function app by selecting Functions under the Functions category from the Function App menu.

## Test Your Azure Function

After you've created a function in the portal, you'll want to test it. There are two approaches:

### Testing it in the portal

The portal also provides a convenient way to test your functions. When you select Run in this pane, the results automatically appear in the Output tab, and the Logs pane opens to display the status.

### Run function manually

You can start a function by manually triggering the configured trigger. For instance, if you're using an HTTP trigger, you can use a tool, such as Postman or cURL, to initiate an HTTP request to your function endpoint URL, which is available from the function definition (Get function URL).

## Monitoring and Application Insights Dashboard

The ability to monitor your functions is critical during development and in production. The Azure portal provides a monitoring dashboard, which you turn on by enabling Application Insights integration. In the Function App menu, under Settings, select Application Insights, select Turn on Application Insights, and then select Apply. The Application Insights dashboard provides a quick way to view the history of function operations by displaying the timestamp, result code, duration, and operation ID populated by Application Insights.

## Streaming Logs Pane

After you've enabled Application Insights in the Azure portal, you can add logging statements to your function for debugging. The called methods for each language are passed a "logging" object, which can be used to add log information to the Logs pane in the Code + Test pane when running a test.

Write to logs from your code using the log method on the context object, which is passed to the handler. The following example writes to the default log level (information):

```javascript
context.log('Enter your logging statement here');
```

## Errors, failures, warnings, and anomalies

You can use Metrics or options from the Investigate category in the Function menu to monitor performance, diagnose failures, or configure dozens of predefined workbooks to manage your function app. Everything from compilation errors and warnings in the code, to usage statistics by role.
