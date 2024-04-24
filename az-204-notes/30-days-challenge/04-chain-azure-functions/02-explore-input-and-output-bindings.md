# Explore input and output binding types

In Azure Functions, bindings offer a declarative approach to connect to data sources and destinations within your code, simplifying the integration with data streams. There are two main types of bindings:

## Input binding

An input binding connects to a data source, enabling your function to read data from these sources.

## Output binding

An output binding connects to a data destination, allowing your function to write data to these destinations.

Triggers, a special type of input bindings, initiate the execution of a function. For instance, an Azure Event Grid notification can serve as a trigger, causing the function to run when an event occurs.

## Types of supported bindings

Azure Functions support various binding types for both input and output purposes. Some common binding types include:

- Blob Storage
- Azure Service Bus Queues
- Azure Cosmos DB
- Azure Event Hubs
- External files
- External tables
- HTTP endpoints

These are just a few examples, and Azure Functions offer an extensibility model to incorporate additional bindings.

## Binding properties

Bindings in Azure Functions typically require three essential properties, with the possibility of additional properties based on the specific binding type and storage:

1. **Name**: Defines the function parameter used to access the data.
2. **Type**: Identifies the type of binding, indicating the data or service being interacted with.
3. **Direction**: Indicates the direction of data flow, whether it's an input or output binding.

Additionally, most binding types require a fourth property:

- **Connection**: Specifies the name of an app setting key containing the connection string. Connection strings stored in app settings enhance code configurability and security.

## Creating a binding

Bindings are configured in the function's configuration file, typically named `function.json`, located in the same folder as the function code. Here's an example of an input binding in JSON format:

```json
...
{
  "name": "headshotBlob",
  "type": "blob",
  "path": "thumbnail-images/{filename}",
  "connection": "HeadshotStorageConnection",
  "direction": "in"
},
...
```

To create this binding:

1. Define the binding in the `function.json` file.
2. Assign a value to the `name` variable, representing the data (blob data in this example).
3. Specify the storage type (`blob` in this case).
4. Provide the path, indicating the container and item name. Curly braces around the `filename` portion create a binding expression, allowing referencing the blob's name in other bindings or function code.
5. Supply the connection string setting name from the application's settings file, serving as a key to find the connection string for connecting to the storage account.
6. Set the direction to `in` to specify reading data from the blob.

In this example, an input binding is used to connect user images for processing as thumbnails within the function.

---
By leveraging bindings in Azure Functions, you can seamlessly integrate with various data sources and destinations, reducing the complexity of connection logic in your code.
