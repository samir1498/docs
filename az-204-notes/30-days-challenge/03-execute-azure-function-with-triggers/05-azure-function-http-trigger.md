# Azure Functions - HTTP Triggers

## Execute an Azure Function with triggers

### What is an HTTP trigger?

An HTTP trigger is a trigger that executes code when it receives an HTTP request. HTTP triggers have many capabilities and customizations.

### What is an HTTP trigger Authorization level?

An HTTP trigger Authorization level is a flag that indicates whether an incoming HTTP request needs an API key for authorization.

There are three Authorization levels, and they are "key" based. To send an HTTP request, you must supply a key for authorization. Here are the three types of keys:

- **Function:** Function keys are specific to a function. They have the most restrictive scope and can only be used to invoke a single function.
- **Admin:** Host keys apply to all functions inside the function app.
  
If your Authorization level is set to Function, you can use either a function or a host key. If your Authorization level is set to Admin, you must supply a host key.

### How to create an HTTP trigger

Just like a timer trigger, you can create an HTTP trigger through the Azure portal. Inside your Azure function, select HTTP trigger from the list of predefined trigger types, then enter the logic that you want to execute and make any customizations, like restricting the use of certain HTTP verbs.

### How to invoke an HTTP trigger

To invoke an HTTP trigger, you send an HTTP request to the URL for your function. To get this URL, go to the code page for your function and select the Get function URL link.

After you have the URL for your function, you can send HTTP requests. If your function receives data, remember that you can either use query-string parameters or supply the data through the request body.

An HTTP trigger executes when it receives an HTTP request to its function URL. HTTP triggers allow you to receive data, execute logic, and optionally return data back to the caller.

### Next unit: Exercise - Create an HTTP trigger
